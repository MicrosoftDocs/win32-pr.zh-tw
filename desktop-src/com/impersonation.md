---
title: 模擬
description: 模擬是指執行緒在安全性內容中執行的能力，與擁有線程的進程內容不同。
ms.assetid: b33ca3b0-0423-4338-b3d6-4bb3db3d3e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a735fa12e175ecec5dc2a7ed741843d713532e19
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024169"
---
# <a name="impersonation"></a>模擬

模擬是指執行緒在安全性內容中執行的能力，與擁有線程的進程內容不同。 在用戶端的安全性內容中執行時，伺服器「是」用戶端的程度。 伺服器執行緒會使用代表用戶端認證的存取權杖，來取得用戶端可存取之物件的存取權。

模擬的主要原因是要針對用戶端的身分識別來執行存取檢查。 使用用戶端的身分識別來進行存取檢查，可能會因為用戶端有許可權的不同，而導致存取受限或展開。 例如，假設檔案伺服器的檔案包含機密資訊，而且每個檔案都受到 ACL 的保護。 為了協助防止用戶端取得這些檔案中資訊的未經授權存取，伺服器可以在存取檔案之前模擬用戶端。

## <a name="access-tokens-for-impersonation"></a>存取模擬的權杖

存取權杖是描述進程或執行緒之安全性內容的物件。 它們提供的資訊包括使用者帳戶的身分識別，以及使用者帳戶可用的許可權子集。 每個進程都有 *主要存取權杖* ，可描述與進程相關聯之使用者帳戶的安全性內容。 根據預設，當進程的執行緒與安全物件互動時，系統會使用主要權杖。 但是，當執行緒模擬用戶端時，模擬執行緒同時具有主要存取權杖和模擬 *權杖*。 模擬權杖代表用戶端的安全性內容，而此存取權杖是在模擬期間用於存取檢查的權杖。 當模擬結束時，執行緒會還原為只使用主要存取權杖。

您可以使用 [**OpenProcessToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) 函式來取得處理常式主要權杖的控制碼。 您可以使用 [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) 函式來取得執行緒模擬權杖的控制碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[存取權杖](/windows/desktop/SecAuthZ/access-tokens)
</dt> <dt>

[委派和模擬](delegation-and-impersonation.md)
</dt> </dl>

 

 