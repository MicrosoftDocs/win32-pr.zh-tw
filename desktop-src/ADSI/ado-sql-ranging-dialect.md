---
title: ADO SQL 範圍方言
description: 使用 (ADO) 的 ActiveX 目錄物件時，您必須在屬性和範圍規範周圍使用 ( ' ) 的單引號）。
ms.assetid: 0453aa9e-ed35-45ff-a728-e854bf0bb353
ms.tgt_platform: multiple
keywords:
- ADO SQL 範圍方言 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f7b846cd3517613dd8ea914f53a7b31c30f8651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968821"
---
# <a name="ado-sql-ranging-dialect"></a>ADO SQL 範圍方言

使用 (ADO) 的 ActiveX 目錄物件時，您必須在屬性和範圍規範周圍使用 ( ' ) 的單引號）。 以下是 ADO SQL 方言的範例。


```sql
Command.CommandText = "select Name, 'member;Range=0-50' from 'LDAP://CN=Group1,DC=Fabrikam,DC=Com' where objectCategory='group'"
```



 

 




