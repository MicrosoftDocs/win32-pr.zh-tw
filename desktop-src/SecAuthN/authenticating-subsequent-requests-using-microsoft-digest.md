---
description: 伺服器會使用摘要式挑戰的不透明指示詞，將其共用安全性內容的參考傳送給用戶端。
ms.assetid: 543c4bed-b224-4da7-9746-12c9993a40af
title: 使用 Microsoft Digest 驗證後續要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eecccc3be68fb541994e63cdfc5035187e04aa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694240"
---
# <a name="authenticating-subsequent-requests-with-microsoft-digest"></a>使用 Microsoft Digest 驗證後續要求

伺服器會使用摘要式挑戰的不透明指示詞，將其共用 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 的參考傳送給用戶端。 成功驗證之後，用戶端必須在對目標伺服器的後續要求中指定此值。 將不透明的值包含在可使用現有安全性內容存取的資源要求中，就不需要在網域控制站重新進行驗證。 這類要求會在伺服器上重新驗證，使用初始驗證後所快取的摘要 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly) 。

下圖說明用戶端和伺服器在後續要求受存取保護的資源時，所採取的步驟。

![使用 microsoft 摘要式驗證後續要求](images/digest2.png)

若要在成功驗證之後要求其他資源，用戶端會呼叫 Microsoft Digest [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函數來產生摘要挑戰回應。 不透明的值會包含在以授權標頭形式傳送至伺服器之挑戰回應的不透明指示詞中， (顯示為 HTTP 要求) 。

伺服器會呼叫 [**AcceptSecurityCoNtext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函數來判斷用戶端是否有現有的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 。 找到現有的內容時，此函式會傳回 \_ \_ 完成 \_ 所需的 SEC E，指出伺服器必須接著呼叫 [**CompleteAuthToken**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken) 函數。 此函式會使用 [初始驗證](initial-authentication-using-microsoft-digest.md)期間快取的摘要 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly)來執行用戶端驗證，而不是在網域控制站重新驗證。

 

 
