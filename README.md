# Склонение числа цифр для онлайн-магазинов
// single = 1 Товар, few = 4 Товара, many = 5 Товаров

    function getEnding(number, single, few, many) {
        var ending, i;

        number % 100;
        if (number >= 11 && number <= 19) {
            ending = many;
        } else {
            number %= 10;
            switch (number) {
                case (1):
                    ending = single;break;
                case (2):
                case (3):
                case (4):
                    ending = few;break;
                default:
                    ending = many;
            }
        }
        return ending;
    }
    
console.log('В корзине ' + getEnding (4, 'Товар', 'Товара', 'Товаров'));
