#include <iostream>
#include <set>

int main() {
    const int x = 3;
    const int y = 3;
    const int z = 3;

    int array[x][y][z] = {
        {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        },
        {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        },
        {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        }
    };

    std::set<int> uniqueNumbers;

    for (int i = 0; i < x; ++i) {
        for (int j = 0; j < y; ++j) {
            for (int k = 0; k < z; ++k) {
                uniqueNumbers.insert(array[i][j][k]);
            }
        }
    }

    std::cout << "Количество различных чисел в массиве: " << uniqueNumbers.size() << std::endl;

    return 0;
}
