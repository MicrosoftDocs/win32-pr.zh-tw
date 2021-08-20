---
title: ADO LDAP 範圍方言
description: 使用 ActiveX Directory 物件 (使用 LDAP 方言的 ADO) 時，屬性和範圍規範不需要引號。
ms.assetid: adda9cf7-6588-48ee-85e2-fddbaf28807b
ms.tgt_platform: multiple
keywords:
- ADO LDAP 範圍方言的 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15dba9b7a701b792321ef327d7b5f9893ef3daa0a5eaad80ea151c2b2c90cad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023986"
---
# <a name="ado-ldap-ranging-dialect"></a>ADO LDAP 範圍方言

使用 ActiveX Directory 物件 (使用 LDAP 方言的 ADO) 時，屬性和範圍規範不需要引號。

以下是 ADO LDAP 方言的範例。


```C++
Command.Text = "<LDAP://CN=NewGroup,DC=Fabrikam,DC=Com>;(objectCategory=group);name,member;Range=51-*;base"
```



 

 




