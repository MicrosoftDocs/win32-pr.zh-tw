---
description: 您可以控制進程存取安全物件或執行系統管理工作的能力。
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: 從 INF 檔案指定安全描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52267f443bf20fe8a9b71a64e2422ac43688d7a54bca2692f1b61ad891fda8cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964834"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a>從 INF 檔案指定安全描述項

您可以控制進程存取安全物件或執行系統管理工作的能力。 安全物件是可以有安全描述項的物件。 所有命名物件都是安全的。 某些未命名的物件（例如處理常式和執行緒物件）也可以有安全描述項。 如需控制安全物件存取的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)。

[安全描述項](/windows/desktop/SecAuthZ/security-descriptors) 包含與安全物件相關聯的安全性資訊。 對於大部分的安全物件而言，您可以在建立物件的函式呼叫中指定物件的安全描述項。 例如，您可以在 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 和 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數中指定安全描述項。

若要從 INF 檔案設定安全描述項，請在安裝檔案、登錄機碼或元件的區段之後，立即新增 [INF 寫入器撰寫的安全性] 區段。 [安全性] 區段應該包含一行，其中包含使用 [安全描述項字串](/windows/desktop/SecAuthZ/security-descriptor-strings)的格式寫入的字串安全描述項。 該行也應以引號括住 ( ") 。

例如，下列 INF 檔案程式碼片段會建立只有系統管理員和系統可存取的登錄機碼。 請注意，此範例需要系統管理許可權。

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

在此情況下，字串的意義是系統管理員有完全控制、系統具有完整控制權，而且存取權可繼承至所有子機碼。 如需詳細資訊，請參閱 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language)。

 

 
