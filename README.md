# Coding-Solutions

##### Given a list of 'n' students, every student is marked in 'm' subjects. Each student is denoted by an index value. The teacher has to ignore the mark for any 1 subject, and calculate the total marks of each student in the other subjects and then sort the marks in ascending order. The teacher decided to ignore the mask of the same subject for each student. He/ She has to select the subject in which the whole class scored the least (the lowest of the average of all the students in each subject) to ignore.

###### Example
```sh
std: 3
mar: 5
arr: [[48,89,31,10,100], [45,67,89,34,54], [92,73,54,10,90]]

Output: [309, 268, 255]
```
<details>
<summary>Solution</summary>
<p>

```sh
        function findMaxPass(std, mar, arr) {
            let marArr = [];
            for(let i=0; i< mar;i++) {
                let marTotal= 0;
                for(let j=0; j< std; j++) {
                    marTotal += arr[j][i];
                }
                marArr.push(marTotal);
            }
            let markMaxIdx = marArr.indexOf(Math.min.apply(null, marArr));
            let stdMarArr = [];
            for(let i=0; i< std;i++) {
                let stdMarTotal= 0;
                for(let j=0; j< mar; j++) {
                    if(j !== markMaxIdx)
                        stdMarTotal += arr[i][j];
                }
                stdMarArr.push(stdMarTotal);
            }
            return stdMarArr.sort((a, b) => a-b);
        }
```

</p>
</details>  

