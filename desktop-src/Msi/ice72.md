---
description: ICE72 會確認 AdvtExecuteSequence 資料表中不會使用非內建的自訂動作。
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f931e705dbca734348f62ba4b1ca106b43bb80a52c50f0e94ecab7139c624da2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946575"
---
# <a name="ice72"></a>ICE72

ICE72 會確認 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)中不會使用非內建的自訂動作。 具體而言，AdvtExecuteSequence 資料表中只允許類型19、type 35 和 type 51 自訂動作。 如果使用其他自訂動作，則公告可能無法如預期般運作。

## <a name="result"></a>結果

如果 AdvExecuteSequence 資料表使用類型35、類型51和類型19以外的自訂動作，ICE72 會傳回錯誤。

## <a name="example"></a>範例

ICE72 會針對所顯示的範例報告下列錯誤：

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

若要修正錯誤，請從 AdvtExecuteSequence 資料表中移除 ' CA1 '。

[AdvtExecuteSequence 資料表](advtexecutesequence-table.md) (部分) 



| 動作 |
|--------|
| CA1    |
| CA35   |



 

[CustomAction 資料表](customaction-table.md) (部分) 



| 動作 | 類型 |
|--------|------|
| CA1    | 1    |
| CA35   | 35   |



 

## <a name="tables-used-during-execution"></a>執行期間所使用的資料表

[AdvtExecuteSequence 資料表](advtexecutesequence-table.md)

[CustomAction 資料表](customaction-table.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂動作類型19](custom-action-type-19.md)
</dt> <dt>

[自訂動作類型35](custom-action-type-35.md)
</dt> <dt>

[自訂動作類型51](custom-action-type-51.md)
</dt> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



