To convert any appropriate  value to decimal, use embedded function "decimal()" 

Examples: 

    decimal(10.5)
    decimal('123.5556')
    decimal('1e-6')
    
    // (1+1)*10/2 = 10
    decimal(1).add(1).mul(10).div(2) 

## Available functions:

### Basic 

**add** returns d + d2.

    decimal(1).add(1) // 2

**sub** returns d - d2.

    decimal(5).sub(2) // 3

**mul** returns d * d2.

    decimal(5).mul(4) // 20

**div** returns d / d2.

    decimal(20).div(4) // 5

**neg** returns -d
    
    decimal(3).neg() // -3

### Comparison

**equal** returns whether the numbers represented by d and d2 are equal.

    decimal('0.002').equal('0.002') // true

**gt** returns true when d is greater than d2.

    decimal('1').gt('0.99') // true

**gte** returns true when d is greater than or equal to d2.

    decimal('1').gt('1.00') // true

**lt** returns true when d is less than d2.

    decimal('1').lt('0.99') // fale
    decimal('1').lt('1.01') // true

**lte** returns true when d is less than or equal to d2.

    decimal('1').lte('1.00') // true


**isPositive**

    decimal('0').isPositive() // false
    decimal('1').isPositive() // true

**isNegative**

    decimal('0').isNegative() // false
    decimal('-1').isNegative() // true

**isZero**

    decimal('0').isZero() // true