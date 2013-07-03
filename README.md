This program will ask for the number of months to run the simluation, and how long rabbits are alive in months.
*Rabbits are listed in pairs, so 1 will reproduce (to, always, 1 new pair).
*After 1 month, rabbits are in their reproductive cycle which takes another month. Therefore, the start of their 
3rd month alive will also see 1 newborn pair.
*Rabbits still give birth in the month when they die. (e.g. rabbits live 3 months, they will reproduce in their 3rd month AND 4th month, when they die)
***There are simpler, more intuitive ways of solving this. However: Upon drawing out the tree to a very large number, I noticed a recurrence
relation for this problem that noone else seems to have mentioned. I tried it, and it works with the implemented base case***

**An alternative way of doing this is to follow the fib function all the way through, but from the first months of deaths onward,
subtract (e.g. for n = months rabbits live) currentMonth-n-1's rabbits. The one exception here is if currentMonth == n, you subtract 1
to avoide going out of bounds. I can post that code upon request, but it is simple to infer from the above instruction.

I have not compared the two different programs timing for very large inputs, but this will solve large inputs very quickly none-the-less.