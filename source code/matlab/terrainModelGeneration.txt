% clear everything and closes all previous files
clear;
close;

%add the desired point cloud input data file to the searchpath in Matlab
addpath(genpath('C:\Users\ngarg5\Downloads\Point_cloud_tools_for_Matlab-master'));
pc = pointCloud('pointCloudData.xyz');
pc.plot;

%finding minimum of Latitude and longitude coordinates
minX=min(pc.X);
latMin=minX(1);
lonMin=minX(2);

%finding maximum of Latitude and longitude coordinates
maxX=max(pc.X);
latMax=maxX(1);
lonMax=maxX(2);


modeValue=mode(pc.X);
avg=rms(pc.X);
diff=abs(modeValue-avg);

%finding out the desired range of altitude coordinates
altMin=modeValue-diff;
altMax=avg+diff;

snapnow;
close; 

%  Plot only selected points
%Applying the Limit Function and Plotting the filtered Point cloud data
pc.select('Limits', [latMin latMax; lonMin lonMax; altMin(3) altMax(3)]);



%plots the final point cloud data
pc.plot;

