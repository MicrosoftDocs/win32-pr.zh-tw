---
description: LocalSystem 帳戶是服務控制管理員所使用的預先定義本機帳戶。
ms.assetid: 692bceb6-f5bd-4b83-ab3b-ef8099dc84e1
title: LocalSystem 帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0132e70044aec7886ce6875239a6bedb502fec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943314"
---
# <a name="localsystem-account"></a>LocalSystem 帳戶

LocalSystem 帳戶是服務控制管理員所使用的預先定義本機帳戶。 安全性子系統無法辨識此帳戶，因此您無法在 [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) 函式的呼叫中指定其名稱。 它在本機電腦上具有廣泛的許可權，並且會作為網路上的電腦。 它的權杖包含 NT 授權單位 \\ 系統和內建系統 \\ 管理員 sid; 這些帳戶可以存取大部分的系統物件。 所有地區設定中的帳戶名稱為。 \\LocalSystem. 您也可以使用名稱、LocalSystem 或 *ComputerName* \\ localsystem。 此帳戶沒有密碼。 如果您在 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 或 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 函式的呼叫中指定 LocalSystem 帳戶，則會忽略您提供的任何密碼資訊。

在 LocalSystem 帳戶內容中執行的服務，會繼承 SCM 的安全性內容。 系統會從 **安全性 \_ 本機 \_ 系統 \_ RID** 值建立使用者 SID。 此帳戶未與任何已登入的使用者帳戶相關聯。 這有下列幾個含意：

-   登錄機碼 **HKEY \_ 目前 \_ 使用者** 與預設使用者相關聯，而不是目前的使用者。 若要存取其他使用者的設定檔，請模擬使用者，然後存取 **HKEY \_ 目前的 \_ 使用者**。
-   服務可以開啟登錄機碼 **HKEY \_ 本機 \_ 電腦 \\ 安全性**。
-   服務會向遠端伺服器顯示電腦的認證。
-   如果服務開啟命令視窗並執行批次檔，則使用者可以按 CTRL + C 來終止批次檔，並取得具有 LocalSystem 許可權的命令視窗的存取權。

LocalSystem 帳戶具有下列許可權：

-   **SE \_ASSIGNPRIMARYTOKEN \_ 名稱** (停用) 
-   **SE \_ (啟用審核 \_ 名稱**) 
-   **SE \_ (\_** 停用的備份名稱) 
-   **SE \_ (啟用變更 \_ 通知 \_ 名稱**) 
-   **SE \_ (啟用 [建立 \_ 全域 \_ 名稱** ]) 
-   **SE \_ (啟用) 建立 \_ 分頁檔 \_ 名稱**
-   **SE \_ (啟用) 建立 \_ 永久 \_ 名稱**
-   **SE \_ (停用) 建立 \_ 權杖 \_ 名稱**
-   **SE \_ (啟用的 DEBUG \_ 名稱**) 
-   **SE \_ (\_** 啟用模擬名稱) 
-   **SE \_啟用 (的 INC. \_ 基礎 \_ 優先順序 \_ 名稱**) 
-   **SE \_ (停用) 增加 \_ 配額 \_ 名稱**
-   **SE \_ (停用載入 \_ 驅動程式 \_ 名稱**) 
-   **SE \_ (啟用鎖定 \_ 記憶體 \_ 名稱**) 
-   **SE \_ (停用) 管理 \_ 磁片區 \_ 名稱**
-   **SE \_獲 \_ 單一 \_ 進程 \_ 名稱** (已啟用) 
-   **SE \_ (\_** 停用的還原名稱) 
-   **SE \_ (\_** 停用的安全性名稱) 
-   **SE \_停用的關機 \_ 名稱** () 
-   **SE \_ (停用系統 \_ 環境 \_ 名稱**) 
-   **SE \_SYSTEMTIME \_ 名稱** (停用) 
-   **SE \_取得 \_ 擁有權 \_ 名稱** (停用) 
-   **SE \_ (啟用 TCB \_ 名稱**) 
-   **SE \_停用移除 \_ 名稱** (停用) 

大部分的服務都不需要這類高許可權層級。 如果您的服務不需要這些許可權，而且不是互動式服務，請考慮使用 [LocalService 帳戶](localservice-account.md) 或 [NetworkService 帳戶](networkservice-account.md)。 如需詳細資訊，請參閱 [服務安全性和存取權限](service-security-and-access-rights.md)。

 

 
