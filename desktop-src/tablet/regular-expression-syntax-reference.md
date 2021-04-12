---
description: 您可以使用某些 Microsoft 手寫辨識器所瞭解的手寫正則運算式語法，來定義和指派自訂輸入範圍。
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: 正則運算式語法參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195677"
---
# <a name="regular-expression-syntax-reference"></a>正則運算式語法參考

您可以使用某些 Microsoft 手寫辨識器所瞭解的手寫正則運算式語法，來定義和指派自訂輸入範圍。 語法是 .NET Framework 中 [正則運算式語言實](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) 作為的子集。

使用手寫的正則運算式，以及其他類型的正則運算式的使用方式有一些差異。 手寫語法是用來指定將由辨識引擎比對的精確字串，而不是子字串。 For example, the regular expression s(\[a-z\]+)p would return matches for "soup", "stop", "instep", and "esophagus". Whereas, an equivalent handwriting regular expression such as s(!IS\_ONECHAR)+p would match "soup" and "stop", but not "instep" and "esophagus".

手寫的正則運算式不支援正則運算式內的非中斷空格。 也就是說，您無法在手寫的正則運算式內使用 "-" 實體。

下列各節會更詳細地說明語法。

## <a name="valid-operators"></a>有效運算子

下列運算子適用于建立正則運算式來定義手寫辨識器的輸入範圍。



| 運算子      | 描述                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | 後置一元運算子，表示運算元的零次或多次。<br/> |
| +<br/>  | 後置一元運算子，表示運算元的一或多個出現。<br/>  |
| ?<br/>  | 後置一元運算子，表示運算元的零次或一次發生。<br/>   |
| \|<br/> | 二元中綴運算子的意義為 "or"。<br/>                                        |
| ()<br/> | 用來將專案分組。<br/>                                                       |



 

Microsoft 對手寫辨識器的正則運算式執行，允許重複的後置一元運算子應用程式。 例如，a \* \* = (a \*) \* = a \* ，b？？ = (b？ ) ？ = b？。 它們也允許非連續的重複專案，例如： a \* ？ \* = ( (\*) ？ ) \* = (\*) \* = a \* 。 這不同于 .NET Framework 的正則運算式，這種運算式只允許？ 要重複的運算子。

.NET Framework 正則運算式的另一項差異是，手寫的正則運算式不支援以空的括弧配對指定的空白運算式， () 。

> [!Note]  
> 手寫的正則運算式只支援1252字碼頁中的字元。

 

## <a name="using-input-scopes"></a>使用輸入範圍

您也可以在正則運算式中，使用一組定義為 [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) 函式一部分的一般輸入範圍。 例如，Month (數值) 的值是 \_ 日期 \_ 月份。 在正則運算式中指定輸入範圍的語法是在輸入範圍列舉值前面加上左括弧和驚嘆號（ (！），並在結尾處加上右括弧 ) 。 例如：

 (！是 \_ 日期 \_ 月份) 

如果您透過 \_ ORing 任何其他輸入範圍來合併 [是預設輸入範圍]，則其效果是辨識器可以傳回預設語言模型支援的任何單一運算式 (例如，系統字典中的一個單字，或包含或不含標點符號的日期) ，或任何符合要傳入辨識器之正則運算式其餘部分的值。

> [!Note]  
> 正則運算式中不支援下列 [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) 成員： \_ PHRASELIST、 \_ REGULAREXPRESSION、是 \_ SRGS、是否為 \_ XML。

 

## <a name="unsupported-operators"></a>不支援的運算子

建立手寫正則運算式時，不支援下列正則運算式運算子。



| 運算子                                     | 描述                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| .<br/>                                 | 句號字元。<br/>                                        |
| \[\]<br/>                              | 方括弧。 使用括弧來群組專案。<br/>     |
| {}<br/>                                | 大括弧。<br/>                                          |
|  (？ \#批註) 和 \# \[ 批註\]<br/> | 註解。<br/>                                                |
| $<br/>                                 | 貨幣符號字元。<br/>                                   |
| ^<br/>                                 | 插入號字元。<br/>                                         |
| -<br/>                                 | 虛線字元。 必須或 (\|) 所有的專案集合。<br/> |



 

## <a name="escaping-characters"></a>逸出字元

除了下表所示的一般字元之外，也會比對。 也就是說，正則運算式中的 "a" 會指定輸入應符合 "a"。

撰寫手寫正則運算式的另一個顯著差異在於，您只能在正則運算式中，對一組有限的字元進行換用。 下表概述可以進行轉義的允許字元集。 任何其他將字元換用的嘗試都會導致辨識器擲回錯誤。



| 字元       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| \\?<br/>  |
| \\(<br/>  |
| \\)<br/>  |
| \\\|<br/> |
| \\\\<br/> |
| \\!<br/>  |
| \\.<br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| \\{<br/>  |
| \\}<br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 