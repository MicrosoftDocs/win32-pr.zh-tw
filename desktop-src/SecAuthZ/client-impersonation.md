---
description: 模擬是指執行緒使用與擁有線程的進程不同的安全性資訊來執行的能力。
ms.assetid: a3f74372-bdc9-43eb-b72f-7d00a43e78a8
title: " (授權) 的用戶端模擬"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e72abb17c9f5f6271f55fbfc77da4f6b93ca2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943666"
---
# <a name="client-impersonation-authorization"></a> (授權) 的用戶端模擬

模擬 [*是指*](/windows/desktop/SecGloss/i-gly)執行緒使用與擁有線程的進程不同的安全性資訊來執行的能力。 一般來說，伺服器應用程式中的執行緒會模擬用戶端。 這可讓伺服器執行緒代表該用戶端進行行動，以存取伺服器上的物件，或驗證對用戶端本身物件的存取。

Microsoft Windows API 提供下列功能來開始模擬：

-   DDE 伺服器應用程式可以呼叫 [**DdeImpersonateClient**](/windows/win32/api/ddeml/nf-ddeml-ddeimpersonateclient) 函數來模擬用戶端。
-   具名管道伺服器可以呼叫 [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) 函數。
-   您可以呼叫 [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) 函式，以模擬已登入使用者 [*存取權杖*](/windows/desktop/SecGloss/a-gly)的安全性內容。
-   [**ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself)函式可讓執行緒產生其本身存取權杖的複本。 當應用程式需要變更單一線程的安全性內容時，這非常有用。 例如，有時只有一個進程的執行緒需要啟用 [*許可權*](/windows/desktop/SecGloss/p-gly)。
-   您可以呼叫 [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken) 函式，使目標執行緒在指定之模擬 [*token*](/windows/desktop/SecGloss/i-gly)的安全性內容中執行。
-   Microsoft 遠端程序呼叫 (RPC) server 應用程式可以呼叫 [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) 函數來模擬用戶端。
-   [*安全性封裝*](/windows/desktop/SecGloss/s-gly)或應用程式伺服器可以呼叫 [**ImpersonateSecurityCoNtext**](/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext)函式來模擬用戶端。

在這些模擬中，模擬執行緒可以藉由呼叫 [**RevertToSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) 函式來還原為它自己的安全性內容。 例外狀況是 RPC 模擬，其中 RPC 伺服器應用程式會呼叫 [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) 或 [**RpcRevertToSelfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex) 來還原為其本身的安全性內容。

 

 
