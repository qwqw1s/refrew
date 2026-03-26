    ЗАДАЧА 1

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int number;

    cout << "Введите число (1-3): ";
    cin >> number;

    switch (number) {
    case 1:
        cout << "Стой" << endl;
        break;
    case 2:
        cout << "Готовься" << endl;
        break;
    case 3:
        cout << "Иди" << endl;
        break;
    default:
        cout << "Ошибка: нужно ввести 1, 2 или 3" << endl;
    }

    system("pause");
    return 0;
    }




    ЗАДАЧА 2 

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int number;

    cout << "Введите целое число: ";
    cin >> number;

    if (number % 2 == 0) {
        cout << "Сегодня повезёт" << endl;
    }
    else {
        cout << "Лучше не рисковать" << endl;
    }

    system("pause");
    return 0;
    }


      ЗАДАЧА 3 

      #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    double a, b;
    char op;

    cout << "Введите первое число: ";
    cin >> a;
    cout << "Введите операцию (+, -, , /): ";
    cin >> op;
    cout << "Введите второе число: ";
    cin >> b;

    switch (op) {
    case '+':
        cout << "Результат: " << a + b << endl;
        break;
    case '-':
        cout << "Результат: " << a - b << endl;
        break;
    case '':
        cout << "Результат: " << a * b << endl;
        break;
    case '/':
        if (b != 0)
            cout << "Результат: " << a / b << endl;
        else
            cout << "Ошибка: деление на ноль!" << endl;
        break;
    default:
        cout << "Неверная операция" << endl;
    }

    system("pause");
    return 0;
    }



    ЗАДАЧА 4

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int temp;

    cout << "Введите температуру: ";
    cin >> temp;

    if (temp < 0) {
        cout << "Мороз" << endl;
    }
    else if (temp <= 20) {
        cout << "Прохладно" << endl;
    }
    else if (temp <= 30) {
        cout << "Тепло" << endl;
    }
    else {
        cout << "Жара" << endl;
    }

    system("pause");
    return 0;
    }

    ЗАДАЧА 5

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int N, sum = 0;

    cout << "Введите N: ";
    cin >> N;

    for (int i = 1; i <= N; i++) {
        sum += i;
    }

    cout << "Сумма от 1 до " << N << " = " << sum << endl;

    system("pause");
    return 0;
    }

    ЗАДАЧА 6 

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int number;

    cout << "Введите число: ";
    cin >> number;

    for (int i = 1; i <= 10; i++) {
        cout << number << " x " << i << " = " << number * i << endl;
    }

    system("pause");
    return 0;
    }

    ЗАДАЧА 7

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int N;

    cout << "Введите N: ";
    cin >> N;

    while (N >= 1) {
        cout << N << " ";
        N--;
    }
    cout << endl;

    system("pause");
    return 0;
    }

    ЗАДАЧА 8

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int number, count = 0;

    cout << "Введите целое число: ";
    cin >> number;

    if (number == 0) {
        count = 1;
    }
    else {
        if (number < 0) number = -number;
        while (number > 0) {
            count++;
            number /= 10;
        }
    }

    cout << "Количество цифр: " << count << endl;

    system("pause");
    return 0;
    }

    ЗАДАЧА 9 

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int N, sum = 0;

    cout << "Введите N: ";
    cin >> N;

    for (int i = 1; i <= N; i++) {
        if (i % 2 == 0) {
            sum += i;
        }
    }

    cout << "Сумма чётных чисел от 1 до " << N << " = " << sum << endl;

    system("pause");
    return 0;
    }

    ЗАДАЧА 10

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int number, maxNumber;

    cout << "Введите число (0 для завершения): ";
    cin >> number;
    maxNumber = number; 

    while (number != 0) {
        if (number > maxNumber) {
            maxNumber = number;
        }
        cout << "Введите число (0 для завершения): ";
        cin >> number;
    }

    cout << "Максимальное число: " << maxNumber << endl;

    system("pause");
    return 0;
    }

    ЗАДАЧА 11 

    #include <iostream>
    #include <cstdlib>
    #include <ctime>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    srand(time(0));
    int secret = rand() % 100 + 1;
    int guess;

    cout << "Я загадал число от 1 до 100. Угадайте!" << endl;

    do {
        cout << "Ваш вариант: ";
        cin >> guess;

        if (guess > secret) {
            cout << "Меньше!" << endl;
        }
        else if (guess < secret) {
            cout << "Больше!" << endl;
        }
        else {
            cout << "Поздравляю! Вы угадали!" << endl;
        }
    } while (guess != secret);

    system("pause");
    return 0;
    }

    ЗАДАЧА 12

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int number;
    bool isPrime = true;

    cout << "Введите число: ";
    cin >> number;

    if (number <= 1) {
        isPrime = false;
    }
    else {
        for (int i = 2; i * i <= number; i++) {
            if (number % i == 0) {
                isPrime = false;
                break;
            }
        }
    }

    if (isPrime) {
        cout << number << " — простое число" << endl;
    }
    else {
        cout << number << " — не простое число" << endl;
    }

    system("pause");
    return 0;
    }

    ЗАДАЧА 13

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int number, reversed = 0;

    cout << "Введите целое число: ";
    cin >> number;

    int temp = number;
    while (temp != 0) {
        reversed = reversed * 10 + temp % 10;
        temp /= 10;
    }

    cout << "Число в обратном порядке: " << reversed << endl;

    system("pause");
    return 0;
    }

    ЗАДАЧА 14

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int amount;

    cout << "Введите сумму (кратную 10): ";
    cin >> amount;

    if (amount % 10 != 0) {
        cout << "Ошибка: сумма должна быть кратна 10" << endl;
    }
    else {
        int count100 = amount / 100;
        amount %= 100;
        int count50 = amount / 50;
        amount %= 50;
        int count20 = amount / 20;
        amount %= 20;
        int count10 = amount / 10;

        cout << "Необходимые купюры:" << endl;
        if (count100 > 0) cout << "100: " << count100 << " шт." << endl;
        if (count50 > 0) cout << "50: " << count50 << " шт." << endl;
        if (count20 > 0) cout << "20: " << count20 << " шт." << endl;
        if (count10 > 0) cout << "10: " << count10 << " шт." << endl;
    }

    system("pause");
    return 0;
    }

    ЗАДАЧА 15

    #include <iostream>
    using namespace std;

    int main() {
    setlocale(LC_ALL, "ru");
    int N;

    cout << "Введите число N: ";
    cin >> N;

    for (int i = 1; i <= N; i++) {
        for (int j = 1; j <= i; j++) {
            cout << "*";
        }
        cout << endl;
    }

    system("pause");
    return 0;
    }
