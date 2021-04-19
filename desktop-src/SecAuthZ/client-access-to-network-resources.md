---
description: 說明用來存取網路資源的策略。
ms.assetid: d55b3204-430d-4fa4-b7a7-1e279beed8e3
title: 用戶端對網路資源的存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0873a10c708f9aab2e9c250375a63e8a2167873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977184"
---
# <a name="client-access-to-network-resources"></a>用戶端對網路資源的存取

伺服器可以使用下列策略來存取網路資源：

-   如果伺服器具有用戶端的帳戶名稱和密碼，則可以使用用戶端的 [*認證*](/windows/desktop/SecGloss/c-gly)來呼叫 [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ，以將本機磁碟機號對應到網路共用。
-   使用用戶端認證呼叫 [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) 之後，伺服器可以呼叫 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函式來 [建立用戶端的進程](processes-in-the-client-security-context.md)。 這個新的用戶端進程可以使用用戶端的 [*安全性內容*](/windows/desktop/SecGloss/s-gly)來存取網路資源。 例如，程式可以呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函數來開啟遠端電腦上的檔案。 系統會使用用戶端的 [*主要權杖*](/windows/desktop/SecGloss/p-gly) 來檢查用戶端進程的存取嘗試。
-   伺服器可以使用 null 認證來呼叫 [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ，以建立具有伺服器存取權或預設連線的網路資源連接。 如果伺服器是以 LocalSystem 帳戶執行，則會向網域伺服器的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 下的網路資源進行驗證。 如果伺服器是在服務帳戶下執行，則會以該帳戶進行驗證。 如需詳細資訊，請參閱 [LocalSystem 帳戶](/windows/desktop/Services/localsystem-account)。

如需保護密碼的相關資訊，請參閱 [處理密碼](/windows/desktop/SecBP/handling-passwords)。 如需取得認證的詳細資訊，請參閱 [要求使用者提供認證](/windows/desktop/SecBP/asking-the-user-for-credentials)。

 

 
