---
title: 建立和執行視圖
description: 您可以建立從 Active Directory 取得的資料檢視。 請注意，只有 view 定義會儲存在 SQL Server 中，而不是儲存在實際的結果集。 因此，當您稍後叫用 view 時，可能會得到不同的結果。
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c4676154ea32dd06e39498e9f943b55d8dbf39694ab9c1005e942cad85f7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082722"
---
# <a name="creating-and-executing-a-view"></a>建立和執行視圖

您可以建立從 Active Directory 取得的資料檢視。 請注意，只有 view 定義會儲存在 SQL Server 中，而不是儲存在實際的結果集。 因此，當您稍後叫用 view 時，可能會得到不同的結果。

下列程式碼範例示範如何建立視圖。


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



使用下列程式碼來叫用 view。


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 SQL Server 和 Active Directory 之間建立異類聯結](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




