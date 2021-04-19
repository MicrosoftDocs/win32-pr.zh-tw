---
description: 顯示這些函式參數之間的關聯性，這些參數會指向結構或陣列與其初始化的資料。
ms.assetid: 89caf4d3-727f-472b-9a09-e81b4ff4d127
title: 簽署資料的程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba289928ab39c690e1c44bdbf65c77c18b7edab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001722"
---
# <a name="procedure-for-signing-data"></a>簽署資料的程式

單一函式 [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)會執行 [建立簽署訊息](creating-a-signed-message.md)中列出的所有工作。 不過，仍需要初始化結構和其他資料。 下圖顯示這些函式參數之間的關聯性，這些參數會指向結構或陣列與其初始化的資料。 下圖只會顯示衍生自其他結構或函數的函式參數和結構成員。 其餘的參數都是直接初始化。

![呼叫 cryptsignmessage 的初始化對應](images/crypsign.png)

**使用 CryptSignMessage 簽署資料**

1.  取得要簽署之資料的指標。
2.  將資料指標指派給「要簽署的資料」陣列中的索引零。
3.  取得密碼編譯提供者的控制碼。
4.  開啟包含簽署者憑證的 [*憑證存放區*](../secgloss/c-gly.md) 。
5.  取得簽署者憑證的位址。
6.  將憑證的位址指派給 *MsgCert* 陣列的零索引。
7.  指派要包含在 *MsgCert* 陣列中之訊息的任何其他憑證位址。
8.  初始化 [**CRYPT \_ 演算法 \_ 識別碼**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) 結構，並適當地將 **pszObjId** 成員初始化為所需的雜湊演算法和其他成員。
9.  初始化 [**CRYPT \_ 簽署訊息 \_ 的 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para)結構、將 pSigningCert 成員初始化為簽署人的憑證位址 **、將** 成員初始化為簽署人的憑證、其他憑證的位址、 **HashAlgorithm** 成員與 [**CRYPT \_ 演算法 \_ 識別碼**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)結構的位址，以及其他成員適當的成員。
10. 呼叫 [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)函式，傳遞 *PSignPara* 參數的 [**CRYPT \_ 簽署 \_ 訊息 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para)結構、 *rgpbToBeSigned* 參數的「要簽署的資料」陣列位址、 *pbSignedBlob* 輸出參數的位址，以及適用于其他參數的值。

 

 
