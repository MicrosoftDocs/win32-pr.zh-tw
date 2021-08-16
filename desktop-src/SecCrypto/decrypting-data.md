---
description: 提供解密加密訊息的步驟。
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: 解密資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600903d7a3060c83cd7cd0a85e92f96efe4fb0cfa30c2936c5546f71138b6854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875688"
---
# <a name="decrypting-data"></a>解密資料

本節提供解密加密訊息的步驟。

**解密加密的訊息**

1.  取得數位封包訊息的指標。
2.  開啟憑證存放區。
3.  從訊息中，取出 (My ID) 的收件者識別碼。
4.  使用收件者識別碼來取得憑證。
5.  取得憑證的私密金鑰。
6.  使用私密金鑰來解密對稱式 (會話) 金鑰。
7.  從訊息中取出加密演算法。
8.  使用解密的工作階段金鑰和加密演算法，解密資料。

[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) 會進行解密訊息的所有工作;不過，仍需要初始化結構和其他資料。

**使用 CryptDecryptMessage 解密資料**

1.  取得加密 BLOB 的指標。
2.  開啟憑證存放區。
3.  建立憑證存放區陣列。
4.  將 [**CRYPT \_ 解密訊息 \_ 的 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) 結構初始化。
5.  呼叫 [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) 來解密訊息中包含的資料。

[範例 C 程式：使用 CryptEncryptMessage 和 CryptDecryptMessage 會執行](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) 剛剛呈現的程式。 批註會顯示哪些程式碼元素完成程式中的每個步驟。 如需有關函數的詳細資訊，請參閱 [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)，如需有關資料結構的詳細資訊，請參閱 [**CRYPT \_ 解密 \_ 訊息 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para)。

 

 



