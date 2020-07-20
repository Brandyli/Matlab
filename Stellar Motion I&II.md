Stellar Motion I

```
load starData
nObs = size(spectra,1)
lambdaStart = 630.02
lambdaDelta = 0.14

Task 1
lambdaEnd = lambdaStart + (nObs-1)*lambdaDelta
lambda = (lambdaStart:lambdaDelta:lambdaEnd)'

Task 2 & 7
s = spectra(:,6)

Task 3
loglog(lambda,s,".-")
xlabel("Wavelength")
ylabel("Intensity")
Task 4
[sHa,idx] = min(s)
lambdaHa = lambda(idx)
Task 5
hold on
loglog(lambdaHa,sHa,"rs","MarkerSize",8)
hold off

Task 6
z = lambdaHa/656.28 - 1
speed = z*299792.458
```
#### Instead of changing the index value, try using a slider to select any column in spectra.
<img width="1000" alt="Screen Shot 2020-07-20 at 7 53 58 AM" src="https://user-images.githubusercontent.com/46945617/87942873-3c49c380-ca6b-11ea-8b7c-d86e18a851b0.png">



## Stellar Motion II


In the previous project, you determined if one star's spectrum was redshifted or blueshifted, 
and calculated the star’s speed relative to the Earth. In this project, you will calculate all the stars' speed at once. 
Then you'll create the plot below.

```
load starData

Task 1
% You could repeat the calculations in a for loop, 
% but it is more efficient to use array operations instead.
[sHa,idx] = min(spectra);
lambdaHa = lambda(idx);
z = lambdaHa/656.28 - 1;
speed = z*299792.458

Tasks 2 - 4
% Since the plot command won't be the same for every star, 
% it's convenient to use a for loop
for v = 1:7
    s = spectra(:,v);

    if speed(v) <= 0
        % plot the blueshifted spectra using dashed lines.
        loglog(lambda,s,"--")
    else
        % plot the redshifted spectra using a thick line
       loglog(lambda,s,"LineWidth",3) 
    end
    hold on
end
hold off
Task 5
% Add a legend to the plot using the array starnames
legend(starnames)
```
Task 6
%Use logical indexing to find elements that match a condition.
movaway = starnames(speed>0)
```
<img width="959" alt="Screen Shot 2020-07-20 at 8 23 25 AM" src="https://user-images.githubusercontent.com/46945617/87943079-87fc6d00-ca6b-11ea-8b40-06cd93cf83a9.png">
<img width="1007" alt="Screen Shot 2020-07-20 at 8 23 46 AM" src="https://user-images.githubusercontent.com/46945617/87943082-87fc6d00-ca6b-11ea-89a6-7e2253c74a34.png">
