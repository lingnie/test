<table>
<thead>
<tr>
<th><strong>Test Name</strong></th>
<th><strong>Test Level</strong></th>
<th><strong>Purpose</strong></th>
<th><strong>Steps</strong></th>
<th><strong>Expected Result</strong></th>
<th><strong>Actual Result</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><code>test get weighted sum</code></td>
<td><code>unit</code></td>
<td>Tests the calculation of the weighted score calculation for a job with various inputs</td>
<td>- Create a JobOption object and initialize with valid values. <br>- Verify that the calculated value for getWeightedSum is correct based on JobOption attributes. <br><a href="../JobCompare6300\app\src\test\java\edu\gatech\seclass\jobcompare6300\test_get_weighted_sum.java">Link to automated code</a></td>
<td>The weighted sum should be calculated correctly for each set of inputs.</td>
<td>Values calculated by JobOption for weighted sum are accurate.</td>
</tr>
<tr>
<td><code>test get adjusted bonus</code></td>
<td><code>unit</code></td>
<td>Tests the calculation of the adjusted bonus for a given job with various parameters for that job</td>
<td>- Create a JobOption object and initialize with valid values. <br>- Verify that the calculated value for getAdjustedBonus is correct based on JobOption attributes. <br><a href="./main.txt">Link to automated code</a></td>
<td>The adjusted bonus should be calculated correctly for each set of inputs.</td>
<td>Values calculated by JobOption for adjusted bonus are accurate.</td>
</tr>
<tr>
<td><code>test get adjusted salary</code></td>
<td><code>unit</code></td>
<td>Tests the calculation of the adjusted salary for a given job with various parameters for that job</td>
<td>- Create a JobOption object and initialize with valid values. <br>- Verify that the calculated value for getAdjustedsalary is correct based on JobOption attributes. <br><a href="./main.txt">Link to automated code</a></td>
<td>The adjusted salary should be calculated correctly for each set of inputs.</td>
<td>Values calculated by JobOption for adjusted salary are accurate.</td>
</tr>
<tr>
<td><code>test  sort  job  list</code></td>
<td><code>integration</code></td>
<td>Tests the sorting of the job list with various list contents (empty, duplicate jobs, normal list, etc.)</td>
<td>Assuming there are already multiple distinct JobOffer instances of data in the database, tap &quot;Enter Job Offers&quot;. At the bottom of the screen, view the list of jobs to see if they are properly sorted.</td>
<td>The list should be sorted by descending score value.</td>
<td>The list of job offers is properly sorted in descending score value.</td>
</tr>
<tr>
<td><code>test  edit  weight</code></td>
<td><code>integration</code></td>
<td>Tests the ability to edit the weight parameters for calculating a job score with various weights</td>
<td>On the main activity page, tap &quot;Adjust The Comparison Settings&quot; button. A screen, verify the default weights, and then test changing them to the following values in each field: (-1.0, 0.0, 0.5, 1.0, 5.0). After changing a weight, exit back to the main menu and then return to the edit menu to ensure the changes are saved.</td>
<td>A view should pop up allowing the score calculation weights to be edited and saved. Negative weights should not be allowed. Any other weight values should be allowed and saved.</td>
<td>The view pops up as expected, negative weights are not allowed to be entered as expected, decimal numbers are not allowed as expected. Whole positive integers are allowed as expected. Any valid changed values are saved when re-entering the screen as expected.</td>
</tr>
<tr>
<td><code>test compare two offers</code></td>
<td><code>integration</code></td>
<td>Tests the comparison of two job offers with various types of jobs</td>
<td>Assuming there is already appropriate input data present in the app, on the main menu, tap the &quot;Compare Job Offers&quot; button. Select two job offers from the list and tap the &quot;Confirm&quot; button.</td>
<td>A separate view should pop up, comparing the two job offers side by side, along with their respective details.</td>
<td>A comparison view pops up, showing the two selected job offers side by side as expected.</td>
</tr>
<tr>
<td><code>test enter current job</code></td>
<td><code>integration</code></td>
<td>Tests the ability to add a new current job to the database with various types of job inputs</td>
<td>On the main menu, tap &quot;RESET&quot; and hit &quot;yes&quot;, then tap the &quot;ENTER OR EDIT CURRENT JOB DETAILS&quot; button, then, fill in all of the appropriate data fields, then tap the &quot;Save&quot; button to save the information and return to main menu. Finally, tap the &quot;ENTER OR EDIT CURRENT JOB DETAILS&quot; button, view the current job field. This test is automated by this script: <a href="../JobCompare6300/app/src/androidTest/java/edu/gatech/seclass/jobcompare6300/test_enter_current_job.java">link</a></td>
<td>The new current job should be present.</td>
<td>The app pass the test and show expected results</td>
</tr>
<tr>
<td><code>test enter current job persistence</code></td>
<td><code>integration</code></td>
<td>Tests the ability to add a new current job to the database with various types of job inputs, and have the data persist through an app restart.</td>
<td>On the main menu, tap &quot;RESET&quot; and hit &quot;yes&quot;, then tap the &quot;ENTER OR EDIT CURRENT JOB DETAILS&quot; button, then, fill in all of the appropriate data fields, then tap the &quot;SAVE&quot; button. Then, force close the app and finally, reopen it and view the current job field.</td>
<td>The new current job should be present after the closing/reopening of the app. This is a manual test.</td>
<td>The app pass the test and show expected results</td>
</tr>
<tr>
<td><code>test edit current job</code></td>
<td><code>integration</code></td>
<td>Tests the ability to edit an current job in the database with various types of job inputs</td>
<td>On the main menu, tap &quot;RESET&quot; and hit &quot;yes&quot;, then tap the &quot;ENTER OR EDIT CURRENT JOB DETAILS&quot; button, then, fill in all of the appropriate data fields, then tap the &quot;SAVE&quot; button to save and return to main menu. After that,tap the &quot;ENTER OR EDIT CURRENT JOB DETAILS&quot; button, then start editing each field that is available. Tap the &quot;SAVE&quot; button. Then tap &quot;ENTER OR EDIT CURRENT JOB DETAILS&quot; button to view the changed information. This test is automated by this script: <a href="../JobCompare6300/app/src/androidTest/java/edu/gatech/seclass/jobcompare6300/test_edit_current_job.java">link</a></td>
<td>The app should open a new view with editable fields and allow the user to change them.</td>
<td>The app pass the test and show expected results</td>
</tr>
<tr>
<td><code>test enter offer</code></td>
<td><code>integration</code></td>
<td>Tests the ability to add a new offer to the database with various types of job offers</td>
<td>On the main menu, tap &quot;RESET&quot; and hit &quot;yes&quot;, then tap the &quot;ENTER JOB OFFER&quot; button. Then, enter data for all of the available fields. Then, hit the &quot;SAVE&quot; button, tap the &quot;MAIN MENU&quot;, then tap the &quot;COMPARE JOB OFFERS&quot; to view the job offer list. This test is automated by this script: <a href="../JobCompare6300/app/src/androidTest/java/edu/gatech/seclass/jobcompare6300/test_enter_offer.java">link</a></td>
<td>The new job offer should be present in the list.</td>
<td>The app pass the test and show expected results</td>
</tr>
<tr>
<td><code>test enter offer persistence</code></td>
<td><code>integration</code></td>
<td>Tests the ability to add a new job offer to the database with various types of job inputs, and have the data persist through an app restart.</td>
<td>On the main menu, tap the &quot;Add Offer&quot; button, then, fill in all of the appropriate data fields, then tap the &quot;Confirm&quot; button. Then, force close the app and finally, reopen it and view the job offer list.</td>
<td>The new job offer should be present after the closing/reopening of the app.</td>
<td>TBD</td>
</tr>
<tr>
<td><code>test compare offer with current job</code></td>
<td><code>integration</code></td>
<td>Tests the comparison of a job offer with the current job with various inputs for both the offer and current job</td>
<td>On the main menu, tap the &quot;Compare Jobs&quot; button. Then, select your current job, as well as one other job offer from the list.</td>
<td>A view should pop up showing a comparison between your current job and the selected job offer.</td>
<td>TBD</td>
</tr>
<tr>
<td><code>test compare offer with current job no current job</code></td>
<td><code>integration</code></td>
<td>Tests the comparison of a job offer with the current job when there is no current job.</td>
<td>On the main menu, tap the &quot;Compare Jobs&quot; button. Then, select one job offer from th e list. Finally, hit &quot;Confirm&quot;</td>
<td>A comparison view should be shown, showing the job offer compared to &quot;nothing&quot; (e.g., your unemployment) and all of the benefits you would get from taking any offer.</td>
<td>TBD</td>
</tr>
<tr>
<td><code>test compare offer with current job no offers</code></td>
<td><code>integration</code></td>
<td>Tests the comparison of a job offer with the current job with various inputs for both the offer and current job</td>
<td>On the main menu, tap the &quot;Compare Jobs&quot; button.</td>
<td>An error should be shown that there are no current job offers to compare.</td>
<td>TBD</td>
</tr>
</tbody>
</table>
