# Reliable Lotteries

**Ricardo de Souza Julião**  
ricardo.sj.trabalho@gmail.com  
Vitória, ES, Brazil  
10/02/2024  

---

## Introduction:
Lotteries are held daily for various purposes, from recreational activities to the distribution of legal cases. The methods used to conduct these lotteries are often outdated and prone to errors, which is why auditing the process is necessary to increase trust. In this document, I present a method for conducting lotteries that doesn't rely on auditing, due to its nature, which guarantees correct and secure results.

I will describe a simplified lottery process for two people, followed by one for an arbitrary number of people, and conclude with a version that allows for multiple winners.

---

## Simplified Lottery Process for Two People:
Suppose João and Maria want to hold a lottery for R$100. We create a list of participants: `[João, Maria]`, where the order of the list represents the order in which they signed up.

Using a computer, both João and Maria create a text file with any integer number. The file is named after the individual, e.g., João.txt and Maria.txt.

Next, both participants must compress their file with a secure password containing at least three letters, three numbers, and three symbols. This results in João.zip and Maria.zip.

João sends his compressed file (João.zip) to Maria via email, and Maria does the same with her file (Maria.zip) to João.

At this point, both participants have each other's files but cannot open them because they are password protected. They confirm via email that both parties have received the files.

Now, it's time to share the passwords. Maria sends her password to João, and João sends his password to Maria. This allows both to open the files.

Suppose the content of Maria's file is 2, and João's file is 3. They sum the contents, resulting in 5.

With the result of 5 and the list of participants `[João, Maria]`, we start a circular count: João is the 1st, Maria is the 2nd, and the count wraps around, making João the 3rd, Maria the 4th, and João the 5th. Since João is the 5th in this circular count, João is the winner.

---

## Simplified Lottery Process for Multiple People:
Each participant signs up for the lottery, creating a public list of participants. Let's name the first person P1, the second P2, and so on, until PN. The list looks like: `[P1, P2, P3, ..., PN]`.

Each participant creates a text file containing their name and a positive integer, then compresses the file with a secure password. For example, Participant 1 creates `P1.zip`.

Each participant sends their compressed file to all other participants, and once all files are received, they confirm via email.

Once everyone confirms receipt, they send the passwords used to compress the files, allowing everyone to open and see the contents. They sum the values from all files.

Let “N” be the sum of all values, and the list of participants be `[P1, P2, P3, ..., PN]`. Now, count through the list circularly until the sum is reached. Mathematically, the winner is determined by the remainder of the division of N by the total number of participants. This identifies the selected participant.

---

## Lottery Process with Multiple Possible Winners:
In a traditional lottery, players choose six different numbers, and after a draw, if the chosen numbers match the drawn numbers, they win. Multiple winners are possible.

### Adjustments:
1. The text file should contain six different numbers, separated by commas, ranging from 01 to 60.
2. After passwords are shared, sum the first numbers of each file, then the second, and so on, until all six numbers are summed. The results are divided by 60, and the remainders give the final lottery numbers.

For example, if the sums are `(65478, 6542, 5187654, 31584, 31987, 99582)`, dividing each by 60 and adding 1 to avoid zero gives: `(19, 3, 55, 25, 8, 43)`. Everyone can see the results and identify the winners.

