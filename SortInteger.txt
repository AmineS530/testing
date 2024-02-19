package Atest

import (
	"fmt"
)

func FindMax(table []int, Size int) int{
	max := 0
	for i := 0 ; i < Size ; i++{
		if table[i] > table[max]{
			max = i
		}
	}
	return(max)
}

func SortIntegerTable(table []int) {
	i := len(table)
	var tmp int
	for i > 0 {
		MaxIndex := FindMax(table, i)
		tmp = table[i - 1]
		table[i - 1] = table[MaxIndex]
		table[MaxIndex] = tmp
		i--
	}
}
