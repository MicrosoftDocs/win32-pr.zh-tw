---
description: LocalService 帳戶是服務控制管理員所使用的預先定義本機帳戶。
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: LocalService 帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513905"
---
# <a name="localservice-account"></a>LocalService 帳戶

LocalService 帳戶是服務控制管理員所使用的預先定義本機帳戶。 它在本機電腦上具有最低許可權，並在網路上呈現匿名認證。

您可以在 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 和 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 函數的呼叫中指定這個帳戶。 請注意，此帳戶沒有密碼，因此會忽略您在此呼叫中提供的任何密碼資訊。 雖然安全性子系統會當地語系化此帳戶名稱，但 SCM 不支援當地語系化的名稱。 因此，您會從 [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) 函式接收此帳戶的當地語系化名稱，但 \\ 當您呼叫 **CreateService** 或 **ChangeServiceConfig** 時，帳戶的名稱必須是 NT 授權單位 LocalService，無論地區設定為何，或可能發生非預期的結果。

使用者 SID 是從 **安全性 \_ 本地 \_ 服務 \_ RID** 值建立。

LocalService 帳戶在 **HKEY \_ USERS** 登錄機碼底下有自己的子機碼。 因此， **HKEY \_ CURRENT \_ USER** 登錄機碼與 LocalService 帳戶相關聯。

LocalService 帳戶具有下列許可權：

-   **SE \_ASSIGNPRIMARYTOKEN \_ 名稱** (停用) 
-   **SE \_ (\_** 停用的審核名稱) 
-   **SE \_ (啟用變更 \_ 通知 \_ 名稱**) 
-   **SE \_ (啟用 [建立 \_ 全域 \_ 名稱** ]) 
-   **SE \_ (\_** 啟用模擬名稱) 
-   **SE \_ (停用) 增加 \_ 配額 \_ 名稱**
-   **SE \_停用的關機 \_ 名稱** () 
-   **SE \_停用移除 \_ 名稱** (停用) 
-   指派給使用者和已驗證使用者的任何許可權

如需詳細資訊，請參閱 [服務安全性和存取權限](service-security-and-access-rights.md)。

 

 
