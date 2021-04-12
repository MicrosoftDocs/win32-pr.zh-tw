---
description: 為了減少網域控制站的流量並改善效能，Microsoft Digest 的用戶端會快取伺服器驗證成功後所接收的資訊。
ms.assetid: cd928266-889a-494c-a94b-4ea7b1dcc241
title: 維護連接間的安全性內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb450dde789f17f46397cb56fe74b94adcf8ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319835"
---
# <a name="maintaining-the-security-context-between-connections"></a>維護連接間的安全性內容

為了減少網域控制站的流量並改善效能，Microsoft Digest 的用戶端會快取伺服器驗證成功後所接收的資訊。 用戶端應用程式只需要將控制碼快取到已建立的 [*安全性內容*](../secgloss/s-gly.md) 。 下表說明安全性封裝所快取的資訊。



| 資訊                                                       | 描述                                                                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 伺服器名稱                                                       | 已成功建立使用者安全性內容的伺服器。                                                                           |
| 領域/網域                                                      | 成功驗證時所使用的功能變數名稱。                                                                                              |
| [*Nonce*](../secgloss/n-gly.md) | 與成功驗證相關聯的伺服器 nonce。                                                                               |
| Nonce 計數                                                       | 用戶端在伺服器要求中包含 nonce 的次數。 這是用於重新執行偵測。                                 |
| 不透明的值                                                      | 驗證成功之後，針對不透明指示詞傳回的值。 此值包含使用者安全性內容的參考。 |



 

當用戶端將訊息傳送到伺服器時，伺服器必須判斷用戶端是否有現有的安全性內容。 若要這樣做，伺服器會將每個用戶端要求傳遞給 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函數。 此函式會從要求中解壓縮不透明指示詞的值（如果有的話），並使用它來查閱用戶端的安全性內容。 如果找到安全性內容，則會將內容控制碼傳回給伺服器。 如需相關資訊，請參閱 [驗證後續要求](authenticating-subsequent-requests-using-microsoft-digest.md)。

作為偵測詐騙和重新執行攻擊的方法，用戶端會呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函式，該函式會使用安全性內容來簽署訊息。 當使用 **MakeSignature** 函數來保護訊息時，伺服器會使用 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 函式搭配快取的內容，以驗證訊息的來源和 [*完整性*](../secgloss/i-gly.md)。 如需詳細資訊，請參閱 [保護訊息](protecting-messages-using-microsoft-digest.md)。

 

 
