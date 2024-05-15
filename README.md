# Unit 3 Summative Assessment<!-- omit in toc -->

###### ICS3U - Mr. Brash 🐿️<!-- omit in toc -->

This assessment has five tasks. Completing them will provide a "level" for you. For example, if you complete only "Task 3", you will receive a Level 1. But if you complete the first _and_ third, that's a Level 2, etc. Try them in the order presented.

- Collaboration is encouraged in terms of helping each other LEARN. Cheating (copying each other) is not.
- Remember - proper formatting, variable names, and commenting is strongly encouraged!
- You are **not** permitted to use the following built-in functions of JavaScript: `.reverse()`, `.split()`, `.join()`, `.min()`, `.max()`, `.includes()`, `.sort()`, `map()`, `filter()`, `reduce()`, etc...
- Tests might be provided at a later date, if possible. You should test your own code!

Jump to:
- [Task 1](#task-1)
- [Task 2](#task-2)
- [Task 3](#task-3)
- [Task 4](#task-4)
- [Task 5](#task-5)


## Task 1

💵 You have a side-hustle selling friendship bracelets on Mattsy, the St. Matt's Etsy site. Each friendship bracelet costs you $2.00 to make but you sell them for $10.00 each. You want to know how much money you made (profit) after a year of selling these bracelets online.

Write the function `bracelets(sales)` that works as follows:
- The `sales` will come in as a String of `+` for a _sale_ ($10.00 for the sale but $2.00 cost in materials) and `-` for a _refund_ (someone wants their money back). 
  - **For example:** if `sales` is "+++-++" you made and sold 6 ($60) bracelets but someone wants their $10.00 back. That means $12 in costs but $50 in sales. You made $38 in profit!
- Calculate and _return_ the overall profit for the year based on the string `sales`. Just return a _Number_, not a String with a dollar sign.
  <br>**Examples:**
  ```JS
  let profit = bracelets("+++-+-+-++-++++");
  // profit is equal to 80
  let proft2 = bracelets("+----")
  // profit2 is equal to 0
  ```

## Task 2

🎸 You work as a bouncer (door person) for a local music venue. During your shift, people arrive (`+`), arrive and tip you (`T`), and people leave (`-`).

Write the function `tickets(night)` which works as follows:
- `night` is a string of `+`, `T`, and `-` representing guests arriving, _tipping_, and leaving.
  - Whenever a guest arrives (`+`) they have to buy a ticket for $15.75
  - If a guest tips you (`T`) they pay $17.75. $15.75 for the ticket and you get the $2.00 tip (nice!).
  - If a guest leaves (`-`) you wish them a good night
- As part of your agreement with the venue, you must place 25% of your tips into the register, along with all ticket sales.
- Calculate and _return_ the amount you must hand-in to the register by the end of your shift. Only return a _Number_, not a String with a dollar sign.
  <br>**Examples:**
  ```JS
  let night1 = tickets("++T+T+-+-");
  // Here you sold 7 tickets and were tipped twice. You must place $111.25 in the register
  // The variable "night1" is equal to 111.25

  let night2 = tickets("TTTTTTT--T-+");
  // You had a good night! You sold 9 tickets and were tipped 8 times.
  // "night2" is equal to 145.75
  ```


## Task 3

🎸 You still work as the bouncer (door person) but now there's a maximum number of people allowed in. **The venue holds a total of 350 guests**. When you arrive for your shift, there's already `guests` number of people inside where 0 ≤ `guests` ≤ 350. During your shift, people arrive (`+`) and people leave (`-`). If the venue ever fills up (350), people arriving will have to wait in line outside the door and can only go in when the venue has less than 350 people inside.

Write the function `bouncer(guests, night)` which works as follows:
- `guests` is the number of guests already in venue when you start your shift.
  - { 0 ≤ `guests` ≤ 350 }
- `night` is a string of `+` and `-` representing guests arriving and leaving.
- Guests are not permitted to tip you... so sad.
- Guests only pay $15.75 for entry _if they go into the venue_. People waiting in line have not paid yet.
- If someone is waiting in line and a guest leaves the venue (`-`), the person in line pays and enters.
- If nobody is in line when someone leaves, nothing happens.
- Calculate and _Return_ the amount you owe to the register at the end of your shift.
  <br>**Examples:**
  ```JS
  let amount_owed = bouncer(348, "+++++-+----+-");
  /* The first two people enter but the next 3 have to wait in line.
     A person leaves, so the line now has 2 people in it and someone enters.
     Another person shows up but has to wait in line.
     Four people leave, allowing everyone in line to enter.
     A person arrives and is let in.
     A person leaves.

     amount_owed = 110.25
  */ 

  amount_owed = bouncer(200, "++++++-+-++-+");
  // amount_owed = 157.5

  amount_owed = bouncer(350, "++++++-+-++-+");
  // amount_owed = 47.25
  ```


## Task 4

🐿️ Mr. Squirrel needs to do his groceries. He's not particularly happy, because groceries are _really_ expensive these days. He's also pretty lazy. He decided to use the local delivery company Nuts 'n Bolts for his purchase. They charge $5.55 for delivery but it's just so convenient!

You are a freelance developer who landed a job with Nuts 'n Bolts to program their receipt printer. They need you to write the function `receipt(items, prices)` that takes _two_ arrays as parameters:
- `items` is an array of Strings _describing_ the items purchased (ie. "Cereal")
- `prices` is an array that is _the same length as `items`_ which gives the pre-tax price of each item.

**The index of each price aligns with the index of each item.**

Print what looks like a receipt to the screen.
- It should start with the String `NUTS 'N BOLTS CLIENT RECEIPT`.
- Then print each item with the price (separating by the tab character `\t` might look nicer).
- Then give a subtotal.
- Calculate and list the Rodent Sales Tax (RST) at 9%.
- Finally, give an overall cost.
  <br>**Example:**
```JS
receipt(["Chips", "Cookies", "Gum"], [22.97, 14.95, 2.85])
```
  
Would print this:
```TXT
NUTS 'N BOLTS CLIENT RECEIPT
Chips           $22.97
Cookies         $14.95
Gum             $2.85
---
Subtotal:       $40.77
Rodent Tax:     $3.67
Delivery:       $5.55
---
Total Due:      $49.99
```

**Note:** The prices might not align perfectly, depending on the data. That's ok!

## Task 5

🐿️ Mr. Squirrel is cleaning [his drey](https://www.massaudubon.org/news/latest/squirrel-dreys) for spring. It's a mess. One of his favourite toys is a large box of capital letters of the English alphabet but it has spilled everywhere. He needs your help to clean it up.

The first part of cleaning up the letters is determining how many of each letter he has.

Write the function `letter_count(str)` that works like this:
  - `str` is a String of length > 0 containing _**only**_ capital letters. For example: "AJDNGUEBKKIEOTIVNWBBWDIVHBRKDPSPOWIFM"
  - The function will count how many of each letter of the alphabet exist in the given `str`
  - It will generate and return an _Array_ of length 26 where index 0 represents the quantity of "A" in the string and index 25 is the quantity of "Z" in the string.

**For Example:**
```JS
let letters = letter_count("AJDNGUEBKKIEOTIVNWBBWDIVHBRKDPSPOWIFM");

// letters is the array: [1, 4, 0, 3, 2, 1, 1, 1, 4, 1, 3, 0, 1, 2, 2, 2, 0, 1, 1, 1, 1, 2, 3, 0, 0, 0]
```

Keep in mind that the function _returns_ the array, it does not _print_ it.

<br><br>

---

Did you finish early? Are you looking for a challenge and want to reach that Level 4++? See Mr. brash.

🐿️
