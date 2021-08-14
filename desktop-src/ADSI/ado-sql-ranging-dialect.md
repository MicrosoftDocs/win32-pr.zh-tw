---
title: ADO SQL 範圍方言
description: 使用 SQL 方言 (ADO) 的 ActiveX Directory 物件時，必須在屬性和範圍規範周圍使用單引號 ( ' ) 。
ms.assetid: 0453aa9e-ed35-45ff-a728-e854bf0bb353
ms.tgt_platform: multiple
keywords:
- ADO SQL 範圍方言 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ad714a514bb926239ebb521391d40d097e7f4ee6ccf50208aaed4bba54d8af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181141"
---
# <a name="ado-sql-ranging-dialect"></a>ADO SQL 範圍方言

使用 SQL 方言 (ADO) 的 ActiveX Directory 物件時，必須在屬性和範圍規範周圍使用單引號 ( ' ) 。 以下是 ADO SQL 方言的範例。


```sql
Command.CommandText = "select Name, 'member;Range=0-50' from 'LDAP://CN=Group1,DC=Fabrikam,DC=Com' where objectCategory='group'"
```



 

 




