---
description: 模擬是執行緒在安全性內容中執行的能力，與擁有線程的進程不同。
ms.assetid: 1bde4d4d-958e-45f4-8cdb-0572adcaa3ac
title: 模擬具名管道用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586de99ae24ba9bab8b65ba4cb1a3a91922aa9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971162"
---
# <a name="impersonating-a-named-pipe-client"></a>模擬具名管道用戶端

模擬 *是執行緒* 在安全性內容中執行的能力，與擁有線程的進程不同。 模擬可讓伺服器執行緒代表用戶端執行動作，但在用戶端的安全性內容限制內。 用戶端通常會有較低層級的存取權限。 如需詳細資訊， [請參閱模擬](/windows/desktop/SecAuthZ/client-impersonation)。

具名管道伺服器執行緒可以呼叫 [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) 函式，以為連接到管道用戶端的使用者存取權杖。 例如，具名管道伺服器可以提供資料庫或檔案系統的存取權，讓管道伺服器具有特殊許可權的存取權。 當管道用戶端將要求傳送到伺服器時，伺服器會模擬用戶端，並嘗試存取受保護的資料庫。 系統接著會根據用戶端的安全性層級，授與或拒絕伺服器的存取權。 當伺服器完成時，它會使用 [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) 函數來還原其原始安全性權杖。

模擬 [層級](/windows/desktop/SecAuthZ/impersonation-levels) 會決定伺服器在模擬用戶端時可執行檔作業。 根據預設，伺服器會在 SecurityImpersonation 模擬層級進行模擬。 但是，當用戶端呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來開啟管道用戶端的控制碼時，用戶端可以使用安全性 \_ SQOS 目前的旗標 \_ 來控制伺服器的模擬層級。

 

 
