# Coding Solutions

> Click :star:if you like the project. Pull Request are highly appreciated. Follow me [@hsajwan7](https://twitter.com/hsajwan7) for technical updates.

---

<div align="center">
    <p>
        <a href="https://www.fullstack.cafe/?utm_source=github&utm_medium=sud">
            <b>Having Tech Interview?</b>
            <br> 3600 Tech Interview Questions. <b>Answered</b>.
            <br>
            <div>
                <img src="https://user-images.githubusercontent.com/13550565/76382460-cc784d80-6393-11ea-8837-2b89265ac853.png" width="260" alt="FullStack.Cafe">
            </div>
        </a>
        <sub><i>Proudly supporting Coding Challenges Solutions</i></sub>
    </p>
</div>

---

## Downloading PDF/Epub formats

You can download the PDF and Epub version of this repository from the latest run on the [actions tab](https://github.com/hsajwan/coding-solutions/actions).

### Table of Contents

| No. | Questions |
|---- | ---------
|1 | [Given a list of 'n' students, every student is marked in 'm' subjects. Each student is denoted by an index value. The teacher has to ignore the mark for any 1 subject, and calculate the total marks of each student in the other subjects and then sort the marks in ascending order. The teacher decided to ignore the mask of the same subject for each student. He/ She has to select the subject in which the whole class scored the least (the lowest of the average of all the students in each subject) to ignore.](#1)|
|2| [In progress](#2)|
|3| [](#)|
|4| [](#)|
|5| [](#)|
|6| [](#)|

1. ### Given a list of 'n' students, every student is marked in 'm' subjects. Each student is denoted by an index value. The teacher has to ignore the mark for any 1 subject, and calculate the total marks of each student in the other subjects and then sort the marks in ascending order. The teacher decided to ignore the mask of the same subject for each student. He/ She has to select the subject in which the whole class scored the least (the lowest of the average of all the students in each subject) to ignore. <a name="1"></a>

    ##### Example
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

**[⬆ Go to Top](#table-of-contents)**

2. ### In progress {#2}

//add smooth scrolling when clicking any anchor link
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        document.querySelector(this.getAttribute('href')).scrollIntoView({
            behavior: 'smooth'
        });
    });
});
//<a href="#someOtherElementID"> Go to Other Element Smoothly </a>
