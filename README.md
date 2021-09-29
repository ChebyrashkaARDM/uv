#include <stdio.h>
#include <locale.h>

int main() {
	setlocale(LC_ALL, "Russian");
	int* a;
	int n, min, i, ind = 0;
	printf("Введите количество чисел: ");
	scanf_s("%d", &n);
	a = (int*)calloc(n, sizeof(int));
	printf("Введите числа: ");
	for (i = 0; i < n; i++)
	{
		scanf_s("%d", &a[i]);
	}
	min = a[0];
	for (i = 0; i < n; i++)
	{
		if (a[i] < min)
		{
			min = a[i];
			ind = i;
		}
	}
	printf("Минимальное значение: %d \n", min);
	printf("Индекс минимального значения: %d", ind);
}
