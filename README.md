Втора лабораториска вежба по Софтверско инженерство  
--------------------------------------------------------------------------
Елза Аџија 223120
--------------------------------------------------------------------------
------->Kликнете Raw за подобра прегледност.

3. Цикломатска комплексност=10.
Формула= број на ребра - број на јазли + 2. Или со броење на ограничени региони.

4.TEST CASES for every branch method

*На местото на Х во текстот може да стои која било вредност.

Test case 1: allItems=null, payment=X (exception)

Test case 2: 
             Oбјект од класата Item каде што:
             item.name=null или item.name=''
             item.barcode==null (exception)
             
Test case 3: 
            Oбјект од класата Item каде што:
            item.name!=null 
            item.barcode!=null, но невалидна вредност на баркод (exception)
                 Item i1=new Item("item1", "!@738dn", 200, 20)
                 payment=X
            
Test case 4: 
            Треба да се задоволени следниве критериуми:
            item.name!=null 
            item.barcode!=null
            item.discount!=0
            item.price>300
            item.barcode.charAt(0)='0'
            sum<=payment 
                 Item i2=new Item("item2","028291", 400, 20)
                 payment=10000
            
            
Test case 5: 
            Треба да се задоволени следниве критериуми:
            item.name!=null 
            item.barcode!=null
            item.discount=0
            item.price<=300
            item.barcode.charAt(0)!='0'
            sum>payment
                 Item i3=new Item("item3","282951", 200, 0)
                 payment=-2

5.  if (item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0)== '0')
T--->true , F--->false, X-whatever

                Primer                                                             Vistinitost
TTT             item.price=400, item.discount=10, item.barcode="028287281"         TRUE    
ТТF             item.price=400, item.discount=10, item.barcode="28287281"          FALSE
TFX             item.price=400, item.discount=0                                    FALSE
FXX             item.price=100                                                     FALSE
