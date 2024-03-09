hat You're Aiming For

Implementation of Insertion Sort using JavaScript:

Insertion sort is a simple sorting algorithm that works the way we sort playing cards in our hands. Each time we take a new card we put it in the right place in our hand.


Instructions

Each time work only with the first i-1 element from of the array
Pick element arr[i] and insert it into sorted sequence in the array from 0 to i-1.



What We're Looking For

Use of 2 counters

GitHub repository with Readme file filled

Documentation & Clarity of the code




Insertion.Algo 




PROCEDURE insertion_sort(VAR arr : ARRAY_OF INTEGER)
VAR
    i,j,current : INTEGER;
BEGIN
    FOR i FROM 1 TO arr.length-1 DO
        current := arr [i];
        j := i-1;
        WHILE (j >= 0 AND arr[j] > current) DO
            arr[j+1] := arr[j];
            j := j-1;
        END_WHILE
        arr[j+1] = current;
    END_FOR
END







Main.js




function insertionSort(array) {
    for(let i = 1; i < array.length; i++) {
        let key = array[i];
        let j = i - 1;
        while (j >= 0 && array[j] > key) {
            array[j + 1] = array[j];
            j = j - 1;
        }
        array[j + 1] = key;
    }
    return array;
}








my_array = [64, 34, 25, 12, 22, 11, 90, 5]

n = len(my_array)
for i in range(1,n):
    insert_index = i
    current_value = my_array.pop(i)
    for j in range(i-1, -1, -1):
        if my_array[j] > current_value:
            insert_index = j
    my_array.insert(insert_index, current_value)

print("Sorted array:", my_array)