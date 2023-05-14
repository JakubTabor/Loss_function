# Loss_function
# I prepare 2 "arrays" as "y_pred and y_true" 
# Now I create function "mean_absolute_value" and I put into "y_true, y_pred"
# This function will be calculate absolute difference between my true value and predicted value
# First i define "total_error", then I make for loop with comperhented list with (y_true, y_pred) using "zip" It will give one value from this two arrays 
# To my "total_error" will be added "absolute difference" between "yt - yp" "total_error += abs(yt - yp)"
# And this value will be printed "print("Total error", total_error)" 
# And then it will return "mean of my value" "total_error / len(y_true)", I also print it " print("Mae", mean_absolute_value)"
# Now I put to my function "mean_absolute_value" this 2 arrays "y_pred, y_true)" and get values 
# Here is how I get absolute difference using numpy "np.abs(y_pred - y_true)"
# And here is "mean absolute value" with numpy "np.mean(np.abs(y_pred - y_true))" and "total error" "np.sum(np.abs(y_pred - y_true))"
# Now I define "epsilon" "epsilon = 1e-15" its value very close to zero but not zero np. (0.0000001), log(0) is undefined so we need to use epsilon
# I need to get my values from 0 to 1 using "epsilon" "[max(i,epsilon)for i in y_pred]", here will by my (0) value 
# My value before transformation "y_pred = np.array([1,1,0,0,1])" my value after transformation "[1, 1, 1e-15, 1e-15, 1]" 
# And now transformation of my (1) value "[min(i,1-eplison)for i in y_pred_new]", before "([1,1,0,0,1])" after "[0.9999, 0.9999, 1e-15, 1e-15, 0.9999]"
# Now I put them into "array" "np.array(y_pred_new)" and I use "log" function to check how they look like "np.log(y_pred_new)"
# I fill values from pattern to binary cross entropy "-np.mean(y_true*np.log(y_pred_new)+(1-y_true)*np.log(1-y_pred_new))"
