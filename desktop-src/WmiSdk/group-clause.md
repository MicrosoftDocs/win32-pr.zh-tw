---
description: GROUP 子句會讓 WMI 產生單一通知，以代表事件群組。
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: GROUP 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4f5f796c563376853896213c5418039ac0104d04437ec7c9e0b444db6692e60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993178"
---
# <a name="group-clause"></a>GROUP 子句

GROUP 子句會讓 WMI 產生單一通知，以代表事件群組。 代表通知是 [**\_ \_ AggregateEvent**](--aggregateevent.md)系統類別的實例。 **\_ \_ AggregateEvent** 系統類別包含兩個屬性：**代表** 和 **NumberOfEvents**。 **代表** 屬性是一個内嵌物件，其中包含在 in [子句](within-clause.md)中指定的分組間隔期間所收到的其中一個實例。 例如，如果產生匯總事件以通知實例修改事件，表示 **代表** 包含一個 [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md)類別的實例。 **NumberOfEvents** 屬性包含在群組間隔期間收到的事件數目。 [群組間隔] 會指定在接收到初始事件之後，WMI 應該收集類似事件的時間週期。

GROUP 子句必須包含內的子句來指定群組間隔，而且可以包含 BY 或 HAVING 關鍵字，或兩者都包含。 GROUP 子句位於 WHERE 子句之後，如下所示：

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

*EventClass* 值是事件所屬的事件類別，而 *值* 則是需要通知之屬性的值。 間隔是不帶正負號的整數，表示在接收到第一個事件之後的分組間隔。 不帶正負號的整數是秒數。 屬性清單是事件類別中所包含的一或多個屬性的逗號分隔清單; *運算子* 是任何關係運算子;和 *整數* 是一個不帶正負號的32位整數，表示多個事件。

使用 GROUP 子句時，WHERE、BY 和 HAVING 子句是選擇性的。

GROUP 子句的基本用法可能會在收到第一個事件時啟動的時間間隔內要求群組事件。 例如，下列查詢會將在5分鐘內傳送的所有電子郵件事件分組。 當收到新電子郵件時，永久取用者可能會使用此查詢來通知使用者，只有在過去5分鐘內收到新電子郵件時，才會將使用者分頁。


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



如果需要更詳細的資訊，事件可以依事件類別的一或多個屬性分組。 下列查詢會要求電子郵件事件與 **寄件者** 屬性中具有相同值的其他事件結合：


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



您可以藉由加入 WHERE 子句來達成更高的詳細程度。 例如，下列查詢會通知使用者來自過去10分鐘內抵達的特定寄件者的新電子郵件，並與 [ **重要性** ] 屬性中具有相同值的其他事件結合：


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



