---
description: ICE70 會確認登錄專案的整數值已正確指定。
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616592a772dec6f95d81b92f03f0bffea6ce7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985474"
---
# <a name="ice70"></a>ICE70

ICE70 會確認登錄專案的整數值已正確指定。 \# \# 不會驗證表單 str、 \# % 未展開 str 的值。 \#系統會驗證表單 xhex、 \# xhex、 \# 整數和 \# \[ 屬性 \] 的值。 下表提供簡短的總覽。



| 值                 | 驗證                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| \#\#Str               | 有效                                                                         |
| \#% 未展開的 str     | 有效                                                                         |
| \#xHex、 \# xHex         | 驗證有效的十六進位字元 (0-9、a-f、a-f) 。 這裡允許屬性。 |
| \#+ int、 \# -int、 \# int |  (0-9) 驗證有效的數位字元。 這裡允許屬性。     |



 

要在登錄中輸入的整數值語法是整數， \# 其中整數是數值。

## <a name="result"></a>結果

如果未正確指定登錄專案的整數值，ICE70 會報告錯誤。

## <a name="example"></a>範例

ICE70 會報告給定範例的下列錯誤。

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

若要修正這個錯誤：若要將值設為數值，請將值變更為使用所有數位字元。 如果您想要將值設為字串，其前面必須有兩個 ' \# (\# \#) ，而不是只有一個。

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

若要修正這個錯誤：有效的十六進位字元是0-9、A-f 和 a-f。 只有這些字元可以跟隨 \# x (或 \# x) 。

登錄[表](registry-table.md) (部分) 



| 登錄 | 值    |
|----------|----------|
| Reg1     | \#12xz34 |
| Reg2     | \#xz34   |



 

## <a name="remarks"></a>備註

-   \#\[myproperty \] 是有效的。
-   \#\[myproperty 無效 (遺漏結尾括弧) 。
-   \#\[myprop1 \] \[ myprop2 有效。  (即使最後一個遺漏結尾的括弧，myprop1 仍會評估為 str， \# 如此您就會有 \# \# str \[ myprop2，這是有效的
-   \#\]myproperty \[ 無效
-   值字串中的任何內嵌屬性都不能是 \[ $compkey \] 、 \[ \# filekey \] 或 \[ ！ filekey \] 形式，因為它們不是數值。 不過，有一個例外狀況， \# \[ myproperty \] \[ $compkey \] (或 \[ \# filekey \] 或 \[ ！ filekey \]) 有效，因為如同上述， \[ myproperty \] 可以評估為 \# str。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



