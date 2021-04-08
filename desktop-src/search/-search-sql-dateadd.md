---
description: DATEADD 函數會針對具有日期類型的相符屬性，執行時間和日期計算。 使用 DATEADD 函數，取得目前的指定時間量內的日期和時間。
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: DATEADD 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112433"
---
# <a name="dateadd-function"></a>DATEADD 函數

DATEADD 函數會針對具有日期類型的相符屬性，執行時間和日期計算。 使用 DATEADD 函數，取得目前的指定時間量內的日期和時間。

## <a name="syntax"></a>語法


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a>引數

*DateTimeUnits*

指定 *日期時間* 參數的單位：年、季、月、周、日、小時、分鐘或秒。 此值會區分大小寫，而且參數周圍不需要引號。

*OffsetValue*

使用 *DateTimeUnits* 參數所指定的單位來指定時間位移。 **OffsetValue** 必須是負整數。 不支援負值。

*DateTime*

指定要從中計算位移的時間戳記。 這不可以是日期常值。 它必須是 GETGMTDATE 或另一個 DATEADD 函數的結果。

## <a name="remarks"></a>備註

DATEADD 函數只能用在常值比較中，而且只能在比較運算子的右邊使用。

GETGMTDATE 函式會傳回目前的日期和時間，以格林尼治平均時間 (GMT) 。 請記住，這個值可能不會與您電腦的當地時間相同。

請勿使用 equals (=) 比較運算子，因為內部時程表示可能會產生會導致非預期比對結果的舍入錯誤。

您可以使用多個 DATEADD 函數來合併位移單位。

### <a name="examples"></a>範例

下列範例 WHERE 子句符合過去五天內修改過的檔：


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



下列範例 WHERE 子句符合過去兩天內修改過的檔和四個小時：


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[常值比較](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[多重值 (陣列) 比較](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**概念**
</dt> <dt>

[全文檢索述詞](-search-sql-fulltextpredicates.md)
</dt> <dt>

[非全文檢索述詞](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



