https://github.com/s26mehta/DataStructures/blob/master/real_questions.py

### PlanGrid

Radio question. You are given a function :


strength(long frequency)


This returns the signal strength given a radio frequency which is a long. You are tasked to return the 10 strongest frequencues.

Frequencies can be between 88.1 - 102.1 and increment by 0.2. Ex[88.1,88.3,88.5]


Answ: Loop through the frequencies and maintain a Min or Max heap



### Inkling 

Implement breadth first tree traversal

What is a DNS?



### Bloomberg

Return the first character in a string that occurs only once

"aabbcddeefgg" = c

"Saif Ali Khan" = S


Given a sorted array of positive and negative intergers, square each element and return a sorted list


Ex [-5,-2,0,1,2,4] = [0, 1 ,4 ,4 ,16, 25]


You can solve this by putting the negative numbers in a sorted array and the positive numbers in a sorted array then merging the two sorted arrrays (2n)


### Microsoft

Implement a stack with an Arraylist

Implement a Queue with a stack in n complexity
`    class Stack {

        ArrayList<Integer> contents = new ArrayList<>();

        public void push(int x) {
            contents.add(x);
        }

        public int pop() {
            if(contents.isEmpty()) {
                return 0;
            }

            int val = contents.get(0);
            contents.remove(0);
            return val;
        }

        public boolean isEmpty() {
            return contents.isEmpty();
        }
    }

    class Queue {

        Stack first = new Stack();
        Stack second = new Stack();

        public void push(int x) {
            first.push(x);
        }

        public int pop() {
            if(first.isEmpty() && second.isEmpty()) {
                return 0;
            }

            if(second.isEmpty()) {
                while(!first.isEmpty()) {
                    second.push(first.pop());
                }
            }
            return second.pop();
        }
    }
`   
Given a sorted array of all ints from 0-51, return a shuffled array


Find the # of islands in a matrix of 1s and 0s where 1 represents land and 0 is water
Ex  

0 1 1 0 0 1

0 0 0 0 0 0

0 1 0 0 0 1

0 1 1 0 0 1 

That contains 4 islands

### Splunk

How many ways can you get to the integer n if you can take 1 or 2 steps every time
4 = 1111, 22 , 112, 221, 122 
3 = 111, 12, 21
2 = 2 ,11
1 = 1

Answer is fibonachi 

### Uber

Implement a quad tree which is populated by an 2n x 2n input matrix.

### Facebook
in an array of integers move all the zeros to the right in n time and n space complexity
[2,3,0,1,0,0,23] -> [2,3,1,23,0,0,0]

Implement a queue using a byte array of static size in n space and constant time complexity. 

### Carrot

Given a binary tree create a hashmap that allows you to look up if a node is an ancestor of another node in constant time. Answer includes depth first pre order traversal.

### Stripe 

Code an isAllowed function that allows users to process a theoretical task twice every 5 seconds and denys if they request more than that. 
