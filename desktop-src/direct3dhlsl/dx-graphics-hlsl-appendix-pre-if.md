---
title: " if、elif、else 和 endif 指示詞"
description: 控制原始程式檔部分編譯的預處理器指示詞。
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- if、elif、else 和 endif 指示詞 HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb5f4716509905d4ce800abbe4cb11b85d116d7a5afd5a56301b1ecb5ce0724b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726448"
---
# <a name="if-elif-else-and-endif-directives"></a>\#if、 \# elif、 \# else 和 \# endif 指示詞

控制原始程式檔部分編譯的預處理器指示詞。



| \#如果 *ifCondition* .。。         |
|--------------------------------|
| \[\#elif *elifCondition* .。。\] |
| \[\#還。。。\]                 |
| \#endif                        |



 

## <a name="parameters"></a>參數



| 項目                                                                                                                                                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*<br/>                                                                                   | 要評估的主要條件。 如果此參數評估為非零值，則此 if 指示詞 \# 和下一個 elif、else 或 endif 的實例之間的所有文字 \# \# \# 都會保留在轉譯單位中，否則不會保留後續的原始程式碼。 <br/> 條件可以使用定義的預處理器運算子來判斷是否已定義特定的預處理器常數或宏;此使用方式相當於使用[ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)指示詞。 <br/> 如需 *ifCondition* 參數值的限制，請參閱「備註」一節。 <br/>                                                                                        |
| <span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[選\] <br/> | 要評估的其他條件。 如果 *ifCondition* 參數和所有先前的 \# elif 指示詞都評估為零，且此參數評估為非零值，則此 \# elif 指示詞和下一個 \# elif、else 或 endif 實例之間的所有文字 \# \# 都會保留在轉譯單位中; 否則，將不會保留後續的原始程式碼。 <br/> 條件可以使用定義的預處理器運算子來判斷是否已定義特定的預處理器常數或宏;此使用方式相當於使用[ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)指示詞。 <br/> 如需 *elifCondition* 參數值的限制，請參閱「備註」一節。 <br/> |



 

## <a name="remarks"></a>備註

來源檔案中的每個 if 指示詞都 \# 必須與結尾的 endif 指示詞相符 \# 。 \#If 和 endif 指示詞之間可以出現任何數目的 elif 指示詞 \# \# ，但最多隻允許一個 else 指示詞 \# 。 Else 指示詞 \# （如果有的話）必須是 endif 之前的最後一個指示詞 \# 。 Include 檔案中包含的條件式編譯指示詞必須滿足相同的條件。

\#If、 \# elif、 \# else 和 endif 指示詞 \# 可以嵌套在其他 if 指示詞的文字部分中 \# 。 每個 nested \# 的 else、 \# elif 或 endif 指示詞都 \# 屬於最接近的前置 \# if 指示詞。

如果沒有任何條件評估為非零值，預處理器會選取 else 指示詞之後的文字區塊 \# 。 如果 \# 省略 else 子句，而且沒有任何條件評估為非零值，則不會選取任何文字區塊。

*IfCondition* 和 *elifCondition* 參數非常符合下列需求：

-   條件式編譯運算式會視為 [**帶正負**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) 號的 long 值，而且這些運算式會使用與 c + + 中的運算式相同的規則來評估。
-   運算式必須是整數類型，而且只能包含整數常數、字元常數和 defined 運算子。
-   運算式不能使用 **sizeof** 或類型轉換運算子。
-   目標環境可能無法表示所有範圍的整數。
-   轉譯代表類型 [**int**](/windows/desktop/WinProg/windows-data-types) 和 **long** 類型相同，而不 [**帶正負**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) 號的 int 則與不 **帶正負** 號的 long 相同。
-   轉譯器可以將字元常數轉譯為一組與目標環境的一組程式碼值不同的程式碼值。 若要判斷目標環境的屬性，請於針對目標環境建置之應用程式的 LIMITS.H 中檢查巨集的值。
-   運算式不得執行任何環境查詢，並且必須與目標電腦上的實作詳細資料保持隔離。

## <a name="examples"></a>範例

本節包含示範如何使用條件式編譯預處理器指示詞的範例。

### <a name="use-of-the-defined-operator"></a>使用已定義的運算子

下列範例示範如何使用已定義的運算子。 如果定義了識別碼點數，則會編譯對 **點數** 函式的呼叫。 如果定義了識別碼的付款，則會編譯對 **借方** 函式的呼叫。 如果未定義任何識別碼，則會編譯 **printerror** 函數的呼叫。 請注意，「點數」和「點數」是 C 和 c + + 中的相異識別碼，因為它們的案例不同。


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a>使用 nested if 指示詞 \#

下列範例示範如何將 if 指示詞嵌套 \# 。 這個範例假設先前已定義名為 DLEVEL 的符號常數。 \#Elif 和 \# else 指示詞會根據 DLEVEL 的值，用來建立四個選項的其中之一。 常數堆疊設定為0、100或200，視 DLEVEL 的定義而定。 如果 DLEVEL 大於5，則不會定義 STACK。


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a>用於包含標頭檔

條件式編譯的常見用途是防止多次包含相同的標頭檔。 在 c + + 中，類別通常定義在標頭檔中，而條件式編譯結構可以用來防止多個定義。 下列範例會判斷是否已定義符號常數範例 \_ H。 如果是，就已包含該檔案，而且不需要重新處理;如果沒有，則 \_ 會定義常數範例 H 來指出該範例。H 已經處理。


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的預處理器指示詞 ](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

