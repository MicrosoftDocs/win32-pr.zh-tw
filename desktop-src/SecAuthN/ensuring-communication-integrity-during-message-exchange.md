---
description: 建立安全性內容之後，應用程式就可以使用訊息支援功能來傳輸防篡改的訊息。
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: 確保訊息交換期間的通訊完整性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70545abf11a933cd3bb6d0c32f3312637fcccbe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112689"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a>確保訊息交換期間的通訊完整性

建立 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 之後，應用程式就可以使用 [訊息支援](authentication-functions.md) 功能來傳輸防篡改的訊息。

用戶端或伺服器會將安全性內容和訊息傳遞至 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函式，以產生防止訊息在傳輸時遭到修改的安全簽章。 訊息的接收者會呼叫 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 函數。 **VerifySignature** 會使用簽章中的資訊來確認接收的訊息在傳輸期間未經過修改。 用戶端和伺服器也可以使用 [**EncryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) 和 [**DecryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)來交換加密的訊息。

在已驗證的連線中，伺服器也可以在呼叫 [**ImpersonateSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext)之後，與用戶端名稱中的其他遠端電腦建立連接。

 

 
