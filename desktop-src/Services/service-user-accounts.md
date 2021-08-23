---
description: 每個服務都會在使用者帳戶的安全性內容中執行。
ms.assetid: a0e48918-6957-4288-a188-d65198b38c16
title: 服務使用者帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6053a4f870b2a49923d802f7cb5f2a45b786d63314d1010773c3e8f58627bec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888545"
---
# <a name="service-user-accounts"></a>服務使用者帳戶

每個服務都會在使用者帳戶的安全性內容中執行。 安裝服務時， [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函式會指定帳戶的使用者名稱和密碼。 您可以使用 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 函數來變更使用者名稱和密碼。 您可以使用 [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) 函式來取得使用者名稱 (但不是與服務物件相關聯的密碼) 。 服務控制管理員 (SCM) 會自動載入使用者設定檔。

啟動服務時，SCM 會登入與服務相關聯的帳戶。 如果登入成功，系統會產生存取權杖，並將其附加至新的服務進程。 此權杖會在與安全物件的所有後續互動中識別服務程式， (具有與其相關聯之安全描述項的物件) 。 例如，如果服務嘗試開啟管道的控制碼，則系統會先將服務的存取權杖與管線的安全描述項進行比較，再授與存取權。

SCM 不會維護服務使用者帳戶的密碼。 如果密碼已過期，登入將會失敗，且服務無法啟動。 將帳戶指派給服務的系統管理員可以建立密碼永遠不會過期的帳戶。 系統管理員也可以使用 [服務設定程式](service-configuration-programs.md) 定期變更密碼，來管理具有過期密碼的帳戶。

如果服務需要在共用其資訊之前辨識另一項服務，則第二個服務可以使用與第一個服務相同的帳戶，也可以在屬於第一個服務所能辨識之別名的帳戶中執行。 需要在網路上以分散方式執行的服務應該在全網域帳戶中執行。

您可以指定下列其中一個特殊帳戶，而不是指定服務的使用者帳戶：

-   [LocalService](localservice-account.md)
-   [NetworkService](networkservice-account.md)
-   [LocalSystem](localsystem-account.md)

 

 



