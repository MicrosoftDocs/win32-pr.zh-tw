---
description: ICE72 會確認 AdvtExecuteSequence 資料表中不會使用非內建的自訂動作。
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994464"
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

 

 



