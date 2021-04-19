---
description: 這些步驟會驗證已簽署資料的簽章。
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: 驗證已簽署的訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f85a5bcde56df7bb41bb92276123bcd26024e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975894"
---
# <a name="verifying-a-signed-message"></a>驗證已簽署的訊息

這些步驟會驗證已簽署資料的簽章。 下圖說明必須完成的個別工作，如其後的清單所示。

![驗證已簽署的訊息](images/verifmsg.png)

**驗證已簽署訊息的簽章**

1.  取得已簽署訊息的指標。
2.  開啟 [*憑證存放區*](../secgloss/c-gly.md)。
3.  使用訊息中包含的簽署者識別碼，取得寄件者的憑證，並取得其 [*公開金鑰*](../secgloss/p-gly.md)的控制碼。

    除了步驟2和3，您也可以使用訊息中包含的憑證來取得簽署者的公開金鑰。

4.  使用簽署人的公開金鑰，將數位簽章解密，以產生訊息中的原始資料摘要。
5.  使用訊息中包含的雜湊演算法， [*雜湊*](../secgloss/h-gly.md) 訊息中包含的資料，產生新的摘要。
6.  將從訊息中取出的摘要，與剛建立的新摘要進行比較。
7.  如果這兩個摘要相符，就會驗證簽章。 這表示用來簽署資料的 [*私密金鑰*](../secgloss/p-gly.md) 會符合單純用來解密簽章的公開金鑰，而且資料在簽署之後也不會變更。

    如果這兩個摘要不符，則不會驗證簽章，而且私用/公開金鑰不相符，或是資料在簽署之後或兩者皆已變更。

單一函式 [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)可以用來驗證簽章，如下列程式所示。

**驗證已簽署的訊息**

1.  取得已簽署訊息的指標。
2.  取得已簽署訊息的大小。
3.  取得密碼編譯提供者的控制碼。
4.  將 [**CRYPT \_ 驗證訊息 \_ 的 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) 結構初始化。
5.  呼叫 [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) 來驗證簽章。

範例 C 程式中包含了可 [執行此程式的程式碼：簽署訊息和驗證訊息簽](example-c-program-signing-a-message-and-verifying-a-message-signature.md)章。

 

 
