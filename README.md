# Udacity - Project1: Test a Perceptual Phenomenon

## Background Information

In a Stroop task, participants are presented with a list of words, with
each word displayed in a color of ink. The participant’s task is to say
out loud the color of the ink in which the word is printed. The task has
two conditions: a congruent words condition, and an incongruent words
condition. In the congruent words condition, the words being displayed are
color words whose names match the colors in which they are printed. In the
incongruent words condition, the words displayed are color words whose
names do not match the colors in which they are printed. In each case, we
measure the time it takes to name the ink colors in equally-sized lists.
Each participant will go through and record a time from each condition.

## Analysis

1. __What is our independent variable? What is our dependent variable?__

   The independent variable is the task condition, that is,
   incongruent words condition or congruent words condition.  The
   dependent variable is the time it takes to name the color of the ink
   in equally sized lists.

2. __What is an appropriate set of hypotheses for this task? What kind of
   statistical test do you expect to perform? Justify your choices. Now
   it’s your chance to try out the Stroop task for yourself. Go to this
   [link](https://www.google.com/url?q=https://faculty.washington.edu/chudler/java/ready.html&sa=D&ust=1486444448807000&usg=AFQjCNFLU18h8eRFpG0OOXUcLEXEfEjpMA),
   which has a Java-based applet for performing the Stroop task.  Record
   the times that you received on the task. Now, download [this
   dataset](https://www.google.com/url?q=https://drive.google.com/file/d/0B9Yf01UaIbUgQXpYb2NhZ29yX1U/view?usp%3Dsharing&sa=D&ust=1486444448808000&usg=AFQjCNELbDtuR43EZqvPOlNMmHFY7UyMdQ)
   which contains results from a number of participants in the task.  Each
   row of the dataset contains the performance for one participant, with
   the first number their results on the congruent task and the second
   number their performance on the incongruent task.__

   The time it took me for the Stroop task on the given link: __8s__
   (congruent), __31.86s__ (incongruent)

   The hypothesis for this study could be as under:
    - _Null Hypothesis_: The task condition (congruent or incongruent words
    condition) has no effect on the time it takes to name the color of the
    ink in equally sized lists.
    - _Alternative Hypothesis_: The time taken to name the color of the ink in
    equally sized lists is greater in incongruent words condition.

   The research publication by John Ridley Stroop (1935) and related
   websites on the Stroop effect suggest that it would take longer to
   read the name the colors in incongruent words condition, hence the
   alternative hypothesis.
    - H0, null hypothesis: __µc = µi__, __µc - µi = 0__
    - Ha, alternative hypothesis: __µc < µi__
    - µc – The population mean for the average time taken by the participants to name the color of the ink in a word list in case of congruent words condition
    - µi – The population mean for the average time taken by the participants to name the color of the ink in incongruent words in a word list in case of condition

  I would conduct a paired t-test since the datasets are dependent (reaction time of same participant). Based on the alternative hypothesis, I would do one-tailed t-test in the positive direction).

3. __Report some descriptive statistics regarding this dataset. Include at
   least one measure of central tendency and at least one measure of
   variability.__

   Congruent Dataset:
   - Mean = 14.05
   - Median = 14.36
   - Sample Standard Deviation = 3.56

   Incongruent Dataset:
   - Mean = 22.02
   - Median = 21.02
   - Sample Standard Deviation = 4.79

   Differences between the two sample dataset:
   - Mean = 7.96
   - Standard Deviation of differences = 4.86

4. __Provide one or two visualizations that show the distribution of the
   sample data. Write one or two sentences noting what you observe about
   the plot or plots.__

   The boxplot for the congruent and incongruent conditions shows
   the distribution and the median values for the reaction time (in
   seconds) for the two task conditions.

5.  __Now, perform the statistical test and report your results.  What is
   your confidence level and your critical statistic value?  Do you
   reject the null hypothesis or fail to reject it?  Come to a conclusion
   in terms of the experiment task.  Did the results match up with your
   expectations?__

   This is a dependent samples study and repeated measures design
   (same participant is given two different conditions).  Based on the
   alternative hypothesis, since we predict that the incongruent words
   condition might increase the reaction time, we will conduct one-tailed
   test in the positive direction.  Let us choose
    - α-level = 0.001 (0.1%)
    - Number of samples, n = 24
    - Degrees of freedom, dof = 23
    - t-critical = 3.485 for α-level = 0.001, dof = 23
    - Difference between means of the dataset, MD = 7.96
    - Standard deviation of the differences, SD = 4.86
    - t-statistic = 8.01

   __t-statistic > t-critical__ which implies __p < α__ or __p < 0.001__

   A calculation online for __t = 8.01__ and __dof = 23__ did not give the
   exact p-value but gave the result as __p-value < 0.0001__.  We reject
   the null hypothesis.  This implies that the alternative hypothesis
   holds, i.e.  time taken to name the color of the ink in equally sized
   lists is greater in incongruent words condition.  The confidence level
   is __99.8%__ and the critical statistic value is __t-critical = 3.485__

   The results match up with my prediction that incongruent words
   condition might interfere with the participant’s ability to name the
   color resulting in greater reaction time.

6. __Optional: What do you think is responsible for the effects observed?
   Can you think of an alternative or similar task that would result in a
   similar effect?  Some research about the problem will be helpful for
   thinking about these two questions.__

   In congruent words condition, the difference in the color of the ink
   and what the word says creates an interference or conflict in the
   participant’s mind, resulting in delayed reaction or incorrect
   response.

   Any other task which might create an interference might result in a
   similar effect.  For example, if the words are printed from right to
   left as shown below, it might inhibit the participants ability to read
   the words as fast as they would if the words were printed as usual
   (left to right).

   - First Condition
    - `ESROH TAOG NOIL TORRAP TNAHPELE`
   - Second Condition
    - `HORSE GOAT LION PARROT ELEPHANT`

## List of Resources

1.  Stroop, John Ridley (1935). "Studies of interference in serial verbal reactions". Journal of Experimental Psychology. 18 (6): 643–662. doi:10.1037/h0054651.

2.  https://support.microsoft.com/en-us/help/214269/how-to-use-the-histogram-tool-in-excel

3.  http://onlinestatbook.com/2/summarizing_distributions/variance_sum_law.html

4.  https://graphpad.com/quickcalcs/PValue1.cfm

5.  https://faculty.washington.edu/chudler/words.html
