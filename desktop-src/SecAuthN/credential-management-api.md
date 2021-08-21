---
description: 認證管理 API
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: 認證管理 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a290cf9d7e5a2d527368c2fd7350fa1bb9549af862c7da7c3845ceae9efc8aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008836"
---
# <a name="credential-management-api"></a>認證管理 API

認證管理函式會組成認證管理員必須執行的一組功能。 這些警告是：

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)，這是 MPR 在使用者登入時所呼叫的事件處理常式函數。
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)，這是 MPR 在帳戶密碼變更時所呼叫的事件處理常式函數。

認證管理函式一律會在系統內容中呼叫 (LocalSystem) 而不是使用者內容。

如需有關如何建立和註冊認證管理員應用程式的詳細資訊，請參閱 [執行認證管理員](implementing-a-credential-manager.md) 以及 [註冊網路提供者和認證管理員](registering-network-providers-and-credential-managers.md)。

 

 



