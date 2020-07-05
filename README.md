# Recommendation-system

As it is a private company dataset . Dataset cann't be provided .  
# Preprocessing Steps

1.Basic Statistics :- 

While seeing the  Basic statistics the mean of NumberOfItemsPurchased is 28.65675 with std of 65.42432 . Mostly they buy 29 items with an average item price of  9.498798 with std 23.081. Basically average user buys for amount is 29*10 = 290 . 

2.Cleaning Data:-

1 . I started with keeping only one duplicate value and droping out the other observation .
Before removing duplicates = (1083818, 8)
After removing duplicates = (536572, 8)
2. There was 1454 missing values in ItemDescription only . So i filled that with ItemCode .yet there was 92 missing values whose ItemCode was unique . So i removed the 92 observation .
3. Extracted Date,Day,Time,Month,Year separately from the TransactionDay atrribute
3.There was a wrong information saying item purchased on 2028 . Taken the transactionid on 2028 and checked with some other year . In one case it was transacted on 2018 . It may be buyed in 2018 and wrongly entered  . so changed to 2018 .
4. Number of Items are negative which is not possible . so converted the negative once to positive.

3.EDA:-

1.Usually most items are brought on Wed than Sun is little surprising . Least number of items are brought in Fri .
2.But even on wed the buy more Item . The total amout collectioned in one day is high on Mon . Means the buy costly items usualy on Mon .
3.Most Transaction are done in Tue Especially in 2018 . In 2019 we have a transaction only for Jan , Feb month .
4. We have a constant items purchased from May to Nov but in Aug there is lesser number of items purchased . But on Dec the max amount of items are purchased due to festival seasson . same as for CostPerItem .  

# Insights of Different customers


List Of Segments Identified and UserId belonged :-
1 . Active User = who shoped regularly in whole year and has  transaction equal to  134912.0 almost double more than the next user is UserId = -1 and top 100 are [-1, 267708, 274869, 296016, 297276, 306726, 310149, 313131, 354984, 374661]

2. User who shop all 12 Months = Customer who shops all 12 irrespective of any suituation are [-1, 374661, 313131, 267708, 306726, 321531, 307566, 274869, 300258, 315819, 297276, 315105, 336693, 367731, 305067, 374031, 372897, 371175, 287574, 266322, 325458, 281568, 279699, 339381, 363615, 261954, 316638, 289758, 269661, 289107, 344862, 282618, 274638, 366450, 365988, 319074, 308280, 353094, 272391, 282828, 382683, 353619, 358428, 336609, 377181, 297780, 365169, 295071, 295260, 347025, 382158, 336273, 285096, 290934, 365001] 

4. Users shop start of the Month = User purchase as soon as salary credited are [-1, 374661, 313131, 296016, 306726, 267708, 274869, 297276, 310149, 354984]

5. Family Shopers = who shop all 12 months and buy the same product all months are mostly the family or regular purchasers they are [-1, 374661, 313131, 296016, 306726, 267708, 274869, 297276, 310149,354984,261954,266322,267708,269661,272391]

6. One Time shoppers = Once who purchased only once or twice in a month but brought items more than 1k are
[315084,352800,378462,302022,266448,259497,324744,340662,315126,330120,259938,343140,285516,338541,334299,352548,267603,328965,284508,333312]

7. Often Purchaser = Instead of Buying in one day the purchase items as there need are [-1,313131,267708,374661,306726,321531,274869,272391,305067,281568,307566,336609,344862,297276,289758,380142,287574,366450,316281,336273]

8.Night Time Users = There is no Users according to the dataset who purchased after 17:00 . 
9. Early Morning User = User buys stuff before 6 am are mostly another shop owners are [380478     -1 321321 364308 364266 344253 291753 355383]

10. User migrated from one coutry to another = User shifted from one country to another are [-1,259770,261009,261051,260757,261597,261555,260274,260862] 

