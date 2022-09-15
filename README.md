# Consistent-trend
This repository contains a notebook of the code I used along with an explanation of the method I chose.  
In general, the idea was to start from the consistent data we have which is the monthly one, and then step by step make the weekly data consistent (instead of just yearly consistent) to finally reach hourly consistent data. 
==> Assumption: we overlook overlapping dates and count them as estimation error 
Math:
let X_1 be the trend in the first month in the monthly data
let Y_1 = (a_1 + b_1 + c_1 + d_1) be the cumulative trends of the 4 weeks of the same first month, where a,b,c, and d represent the trend of the 4 weeks of the months in the weekly data!
then X_1 = alpha * Y_1 where the alpha is the scaling coeff used by google trends
-- alpha should be the same for the whole year since the weekly data is yearly consistent
==> the first goal was to calculate alpha for each year and then rescale the weekly data using that
Once this step is done we redo the previous steps while dealing with the newly consistent weekly data as a baseline to transform the hourly data
