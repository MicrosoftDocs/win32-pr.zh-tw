---
description: 說明如何使用 Microsoft Digest 來保護訊息。
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: 使用 Microsoft Digest 保護訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573eafcf66e23188546abd3acd316095ec100187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969417"
---
# <a name="protecting-messages-using-microsoft-digest"></a>使用 Microsoft Digest 保護訊息

## <a name="http-and-sasl"></a>HTTP 和 SASL

用戶端和伺服器會使用 [安全性支援提供者介面](sspi.md) (SSPI) 訊息 [*完整性*](../secgloss/i-gly.md) 函式 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 和 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 來保護訊息，以偵測特定類型的安全性違規。

用戶端會呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函數，以使用其 [*安全性內容*](../secgloss/s-gly.md)來簽署訊息。 伺服器會使用 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 函數來驗證訊息的來源。 除了驗證隨附于訊息 [*的簽*](../secgloss/d-gly.md) 章之外， **VerifySignature** 函式也會檢查 nc 指示詞所指定的 [*nonce*](../secgloss/n-gly.md) 計數 (，) 是否大於針對 nonce 傳送的最後一個計數。 如果不是這種情況， **VerifySignature** 函式會傳回序列錯誤碼中的秒 \_ \_ 數 \_ 。

## <a name="sasl-only"></a>僅限 SASL

[**EncryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-encryptmessage)和 [**DecryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)函式提供在用戶端與伺服器之間交換之後續驗證訊息的機密性。

為了使用訊息機密性函數，伺服器和用戶端必須已使用下列屬性建立 [*安全性內容*](../secgloss/s-gly.md) ：

-   Qop 指示詞所指定的保護品質必須是 "auth"。
-   加密機制必須透過 cipher 指示詞來指定。

 

 
