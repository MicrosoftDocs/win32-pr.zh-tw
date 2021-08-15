---
description: HAVING 子句可用來篩選在 in 子句中指定的分組間隔期間所收到的事件。
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: HAVING 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2662ea337c5664130eb9973c049431daedefe3c947c45eb397a950522fea6bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993158"
---
# <a name="having-clause"></a>HAVING 子句

HAVING 子句可用來篩選在 in [子句](within-clause.md)中指定的分組間隔期間所收到的事件。 例如，您可以建立一個 SELECT 語句，讓它不會傳回任何內容，除非過去30秒的間隔內至少有5個事件。

In 子句緊接在[group](group-clause.md)子句之後的[SELECT 語句](select-statement-for-event-queries.md)中。 HAVING 子句會在 [**\_ \_ AggregateEvent**](--aggregateevent.md)系統類別的 **NumberOfEvents** 屬性上運作，而 group 子句所建立的群組是成員。 HAVING 子句可以使用所有標準關係運算子。

語法如下：

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

*EventClass* 值是事件所屬的事件類別，而 *值* 則是需要通知之屬性的值。 間隔是一種不帶正負號的整數，表示在接收到第一個事件之後 (的分組間隔（以秒) 為單位）。 屬性清單是事件類別中包含的一或多個屬性的逗號分隔清單。 運算子是任何關係運算子。 常數值是任何不帶正負號的32位整數，表示用於篩選的事件數目。

使用 HAVING 子句時，WHERE 和 BY 子句是選擇性的。

下列事件查詢要求 **EmailEvent** 類別的通知會在 WMI 收到的第一個事件之後分組為一個事件300秒。 此外，只有當 WMI 在300秒內收到五個以上的電子郵件事件時，查詢才會要求 [**\_ \_ AggregateEvent**](--aggregateevent.md)實例傳遞。


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



下列範例會將600秒內收到的所有事件分組 (也就是 **TargetInstance**) 10 分鐘。未通過 **的屬性。** 在此範例中，只有在從相同來源收到的 [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) 事件數目超過25時，才會傳遞匯總事件。 請記住，ISA 運算子會讓 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)系統類別的 **TargetInstance** 屬性代表 **Win32 \_ NTLogEvent** 類別的實例。


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
