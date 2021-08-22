---
title: " (WinNT 提供者的物件 SID) "
description: 您可以使用 objectSID 屬性來抓取使用者安全識別碼 (SID) 。 ObjectSID 會以形成 SID 字串的變異字元陣列形式傳回。
ms.assetid: 15845e6d-ea30-4d6c-9f35-b2abc1a564ba
ms.tgt_platform: multiple
keywords:
- WinNT 提供者 ADSI、使用者管理範例、物件 SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331d1214e97ec6c751171f77e625a40395283b14d941ac1bb0775ea0c9efe27a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391818"
---
# <a name="object-sid-winnt-provider"></a> (WinNT 提供者的物件 SID) 

您可以使用 **objectSID** 屬性來抓取使用者安全識別碼 (SID) 。 **ObjectSID** 會以形成 SID 字串的 **變異** 字元陣列形式傳回。

## <a name="example-code"></a>範例程式碼


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




