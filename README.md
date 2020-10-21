# Coding-Solutions

## In a class of n students having m subjects, Teacher has to remove the marks of a subject for all the students doing which the max number of students get pass.

### Example
```sh
std: 3
mar: 5
arr: [[48,89,31,10,100], [45,67,89,34,54], [92,73,54,10,90]]

Output: [309, 268, 255]
```
<details>
<summary>

### Solution

</summary>
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
            return stdMarArr.sort((a, b) => b-a);
        }
```

</p>
</details>  

