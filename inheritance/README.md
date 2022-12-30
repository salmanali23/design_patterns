### In Company ABC, there are two types of workers: permanent and contract.

There are rules that apply to all workers, and some only apply to specific types.

Rules that apply to permanent workers, these workers get a salary and a fixed allowance based on their group. There are 3 groups within this type:

- Group D: Salary = $4.000 with a 1.000 fixed allowance.
- In Group E, the salary is $5.000 and the fixed allowance is $2.500.
- Group F: $6.000 salary plus $3.500 fixed allowance

Rules that apply to contract workers are that workers get a salary and a positional allowance based on their group. There are 3 groups within this type:

- In Group A, the salary is $1,000 and the positional allowance is $700.
- In Group B, the salary is $2,000, and the positional allowance is $800.
- In Group C, the salary is $3000, and the positional allowance is $900.
The rules that apply to all workers: if a worker has a child, then each child will get 50, but a maximum of only 3 children.


### Solution with inheritance

- Within the Worker class, we declared attributes and behaviors that are used by all types workers.
- Within the PermanentWorker class, we defined class-specific attributes (fixed_allowances) and behaviors (count_fixed_allowance).
- Within the ContractWorker class, we defined class-specific attributes (positional_allowance) and behaviors (count_positional_allowance).