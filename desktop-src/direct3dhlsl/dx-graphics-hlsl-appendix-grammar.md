---
title: 文法
description: HLSL 語句會使用下列文法規則來建立。
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b77f1050beaee2b269d12e69704018e3c5abee6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129846"
---
# <a name="grammar"></a>文法

HLSL 語句會使用下列文法規則來建立。

-   [空白](#whitespace)
-   [浮點數](#floating-point-numbers)
-   [整數數字](#integer-numbers)
-   [Characters](#characters)
-   [字串](#strings)
-   [識別碼](#identifiers)
-   [運算子](#operators)
-   [相關主題](#related-topics)

## <a name="whitespace"></a>空白

下列字元會被辨識為空白字元。

- SPACE
- TAB
- Eol
- C 樣式批註 (/ \* \* /) 
- C + + 樣式批註 (//) 

## <a name="floating-point-numbers"></a>浮點數

浮點數會以 HLSL 表示，如下所示：

-   小數常數指數-部分 (opt) 浮動尾碼 (opt) 

    數位序列指數-部分浮動尾碼 (opt) 

-   小數常數：

    數位序列 (opt) 。 數位順序

    數位順序。

-   指數-部分：

    e sign (opt) 數位順序

    E sign (opt) 數位順序

-   sign：下列其中一個

    \+ -

-   數位順序：

    digit

    digit-sequence digit

-   floating-suffix：下列其中一個

    h H f F l L

    使用 "L" 尾碼來指定完整的64位有效位數浮點數常值。 32位的 float 常值是預設值。

    例如，編譯器會將下列常值識別為32位精確度浮點數常值，並忽略較低的位：

    ```
    double x = -0.6473313946860445;
    ```

    

    編譯器會將下列常值辨識為64位精確度浮點數常值：

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a>整數數字

整數會以 HLSL 表示，如下所示：

-   整數常數整數-尾碼 (opt) 
-   整數常數：下列其中一個

    \# (十進位數) 

    0 \# (八進位數位) 

    0x \# (hex 數位) 

-   整數尾碼可以是下列其中一項：

    u U l l

## <a name="characters"></a>Characters

字元會以 HLSL 表示，如下所示：



| 字元                                          | 描述                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| 交流                                       |  (字元)                                                      |
| ' \\ a ' ' \\ b ' ' \\ f ' ' \\ b ' ' \\ r ' ' \\ t ' ' \\ v ' |  (的 esc)                                                        |
| '\\\#\#\#'                                |  (八進位 escape，每個 \# 都是八進位數位)                        |
| ' \\ x \# '                                   |  (hex escape， \# 是十六進位數位，任何數目的數位)             |
| ' \\ c '                                     |  (c 是其他字元，包括反斜線和引號)  |



 

預處理器運算式中不支援 esc。

## <a name="strings"></a>字串

字串以 HLSL 表示，如下所示：

"s" (s 是具有 esc) 的任何字串。

## <a name="identifiers"></a>識別碼

識別碼會以 HLSL 表示，如下所示：


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a>運算子


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



另外還有任何其他不符合其他規則的單一字元。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[附錄 (DirectX HLSL) ](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




