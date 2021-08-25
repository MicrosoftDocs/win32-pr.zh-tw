---
description: 說明使用基底密碼編譯功能來加密訊息時所要採取的步驟。
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: 加密資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7d2a7fde500397959f0a2352b3f8ddb4fa662209afb251ddceaa8774048f9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874450"
---
# <a name="encrypting-data"></a>加密資料

下列程式說明使用基底密碼編譯功能來加密訊息時所要採取的步驟。 若要使用 PKCS 7 標準來加密訊息 \# ，請參閱 [低層級訊息函數](cryptography-functions.md) 和 [簡化的訊息](cryptography-functions.md)函式。

**加密訊息**

1.  使用 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 函數來產生工作階段金鑰。

    進行此呼叫會產生隨機索引鍵並傳回控制碼，因此可以使用金鑰來加密和解密資料。 此時也會指定要使用的加密演算法。 由於 CryptoAPI 不允許應用程式使用公開金鑰演算法來加密大量資料，因此請使用 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 呼叫指定對稱演算法，例如 RC2 或 RC4。

2.  或者，您也可以使用 [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) 函式，將密碼轉換成適合加密的金鑰。

    如果應用程式需要加密訊息，讓具有指定密碼的任何人都可以解密資料，請使用 [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) 將密碼轉換成適合加密的金鑰。

    > [!Note]  
    > 在此情況下，會呼叫這個函式，而不是 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 函式，而且不需要後續的 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) 呼叫。

     

3.  如有必要，請使用 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) 函式來設定金鑰的額外密碼編譯屬性

    產生金鑰之後，可以使用 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)函式來設定金鑰的額外密碼編譯屬性。 此函式可讓您使用不同的金鑰 salts 來加密檔案的不同區段，並提供方法來變更金鑰的加密模式或初始化向量。 這些參數可以用來讓加密符合特定的資料加密標準。

4.  使用 [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) 函數加密檔案中的資料。

    [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt)函式會使用在上一個步驟中產生的工作階段金鑰，並加密資料的緩衝區。

    > [!Note]  
    > 當資料經過加密時，加密演算法可能會稍微擴展資料。 應用程式會負責記住加密資料的長度，以便稍後可以為 [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) 函數指定適當的長度。

     

5.  （選擇性）使用 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) 函式，允許目前的使用者在未來解密資料。

    為了讓目前的使用者能夠在未來將資料解密， [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) 函式會用來將解密金鑰儲存為加密格式， (只能以使用者的私密金鑰解密的金鑰 BLOB) 。 此函式需要使用者的金鑰交換公開金鑰才能達成此目的，您可以使用 [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) 函數來取得此公開金鑰。 **CryptExportKey** 函式會傳回必須由應用程式儲存以用於解密檔案的金鑰 BLOB

> [!Note]  
> 如果應用程式的憑證 (或公開金鑰) 供其他使用者使用，則可讓其他使用者針對應該接收存取權的每個使用者執行 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) 呼叫，以將檔案解密。 傳回的金鑰 Blob 必須由應用程式儲存（如步驟5所示）。

 

## <a name="creating-an-encrypted-message"></a>建立加密的訊息

簡化的訊息函數可讓您更輕鬆地加密和解密資料。 下圖描述必須完成才能加密訊息的個別工作。 下列清單將描述這些步驟。

![加密訊息](images/encmsg.png)

**加密訊息**

1.  取得純文字訊息的指標。
2.  產生對稱 (會話) 金鑰。
3.  使用對稱金鑰和指定的加密演算法，加密訊息資料。
4.  開啟憑證存放區。
5.  取得收件者的憑證。
6.  從收件者的憑證取得公開金鑰。
7.  使用收件者的公開金鑰加密對稱金鑰。
8.  從收件者的憑證取得收件者的識別碼。
9.  在數位封包訊息中包含下列內容：資料加密演算法、加密的資料、加密的對稱金鑰，以及收件者識別碼。

 

 



