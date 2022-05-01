## Software Design Principles DRY and KISS

**The DRY Principle: Don't Repeat Yourself**

Dry is refering to don't repeat yourself and the objective of this principle is reducing the repetition of information.

**Violations of DRY**

We are wasting everyone's time when we write the same code or the same logic again and again.

**How to Achieve DRY**

You have to divide your code into small units and do them reusable.

**DRY Benefits**

When we optimize our code, it saves time and effort, it's easy to maintain, and it's easier to find any bugs.

**KISS: Keep It Simple, Stupid**

Our code should be readable for any person and we should make each method to solve a single problem.

**Violations of KISS**

Here we have an example of it:
```
public String weekday1(int day) {
    switch (day) {
        case 1:
            return "Monday";
        case 2:
            return "Tuesday";
        case 3:
            return "Wednesday";
        case 4:
            return "Thursday";
        case 5:
            return "Friday";
        case 6:
            return "Saturday";
        case 7:
            return "Sunday";
        default:
            throw new InvalidOperationException("day must be in range 1 to 7");
    }
}

public String weekday2(int day) {
    if ((day < 1) || (day > 7)) throw new InvalidOperationException("day must be in range 1 to 7");

    string[] days = {
        "Monday",
        "Tuesday",
        "Wednesday",
        "Thursday",
        "Friday",
        "Saturday",
        "Sunday"
    };

    return days[day - 1];
}
```
We have a method that is doing the same thing twice, it's a waste of time and effort and we should optimize it.

**How to Achieve KISS**

To avoid it, we should think the best solution to our problem and use it making simple code.

**Benefit of KISS**

The benefit is that if the code is simple, anyone can understand it, use it and modify it as they want.

