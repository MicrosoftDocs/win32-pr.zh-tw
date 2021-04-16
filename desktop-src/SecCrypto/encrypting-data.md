---
description: 說明使用基底密碼編譯功能來加密訊息時所要採取的步驟。
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: 加密資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44db44db08268241e399107d8af4088dac3c0c2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553709"
---
# <a name="encrypting-data"></a><span data-ttu-id="c5b18-103">加密資料</span><span class="sxs-lookup"><span data-stu-id="c5b18-103">Encrypting Data</span></span>

<span data-ttu-id="c5b18-104">下列程式說明使用基底密碼編譯功能來加密訊息時所要採取的步驟。</span><span class="sxs-lookup"><span data-stu-id="c5b18-104">The following procedure describes steps to take to encrypt a message with the Base Cryptography Functions.</span></span> <span data-ttu-id="c5b18-105">若要使用 PKCS 7 標準來加密訊息 \# ，請參閱 [低層級訊息函數](cryptography-functions.md) 和 [簡化的訊息](cryptography-functions.md)函式。</span><span class="sxs-lookup"><span data-stu-id="c5b18-105">To encrypt messages using PKCS \#7 standards, see [Low-level Message Functions](cryptography-functions.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="c5b18-106">**加密訊息**</span><span class="sxs-lookup"><span data-stu-id="c5b18-106">**To encrypt a message**</span></span>

1.  <span data-ttu-id="c5b18-107">使用 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 函數來產生工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5b18-107">Generate a session key by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>

    <span data-ttu-id="c5b18-108">進行此呼叫會產生隨機索引鍵並傳回控制碼，因此可以使用金鑰來加密和解密資料。</span><span class="sxs-lookup"><span data-stu-id="c5b18-108">Making this call generates a random key and returns a handle so the key can be used to encrypt and decrypt data.</span></span> <span data-ttu-id="c5b18-109">此時也會指定要使用的加密演算法。</span><span class="sxs-lookup"><span data-stu-id="c5b18-109">The encryption algorithm to use is also specified at this point.</span></span> <span data-ttu-id="c5b18-110">由於 CryptoAPI 不允許應用程式使用公開金鑰演算法來加密大量資料，因此請使用 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 呼叫指定對稱演算法，例如 RC2 或 RC4。</span><span class="sxs-lookup"><span data-stu-id="c5b18-110">Because CryptoAPI does not permit applications to use public key algorithms to encrypt bulk data, specify a symmetric algorithm such as RC2 or RC4 with the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) call.</span></span>

2.  <span data-ttu-id="c5b18-111">或者，您也可以使用 [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) 函式，將密碼轉換成適合加密的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5b18-111">Alternatively, use the [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) function to transform a password into a key suitable for encryption.</span></span>

    <span data-ttu-id="c5b18-112">如果應用程式需要加密訊息，讓具有指定密碼的任何人都可以解密資料，請使用 [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) 將密碼轉換成適合加密的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5b18-112">If an application needs to encrypt the message so that anyone with a specified password can decrypt the data, use [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) to transform the password into a key suitable for encryption.</span></span>

    > [!Note]  
    > <span data-ttu-id="c5b18-113">在此情況下，會呼叫這個函式，而不是 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 函式，而且不需要後續的 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="c5b18-113">In this case, this function is called instead of the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function and the subsequent [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls are not needed.</span></span>

     

3.  <span data-ttu-id="c5b18-114">如有必要，請使用 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) 函式來設定金鑰的額外密碼編譯屬性</span><span class="sxs-lookup"><span data-stu-id="c5b18-114">If necessary, set extra cryptographic properties of the key by using the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function</span></span>

    <span data-ttu-id="c5b18-115">產生金鑰之後，可以使用 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)函式來設定金鑰的額外密碼編譯屬性。</span><span class="sxs-lookup"><span data-stu-id="c5b18-115">After the key has been generated, extra cryptographic properties of the key can be set with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)function.</span></span> <span data-ttu-id="c5b18-116">此函式可讓您使用不同的金鑰 salts 來加密檔案的不同區段，並提供方法來變更金鑰的加密模式或初始化向量。</span><span class="sxs-lookup"><span data-stu-id="c5b18-116">This function allows different sections of the file to be encrypted with different key salts and provides a way to change the cipher mode or initialization vector of the key.</span></span> <span data-ttu-id="c5b18-117">這些參數可以用來讓加密符合特定的資料加密標準。</span><span class="sxs-lookup"><span data-stu-id="c5b18-117">These parameters can be used to make the encryption conform with a particular data encryption standard.</span></span>

4.  <span data-ttu-id="c5b18-118">使用 [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) 函數加密檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="c5b18-118">Encrypt the data in the file with the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function.</span></span>

    <span data-ttu-id="c5b18-119">[**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt)函式會使用在上一個步驟中產生的工作階段金鑰，並加密資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c5b18-119">The [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function takes the session key that was generated in the previous step and encrypts a buffer of data.</span></span>

    > [!Note]  
    > <span data-ttu-id="c5b18-120">當資料經過加密時，加密演算法可能會稍微擴展資料。</span><span class="sxs-lookup"><span data-stu-id="c5b18-120">As the data is encrypted, the data may be slightly expanded by the encryption algorithm.</span></span> <span data-ttu-id="c5b18-121">應用程式會負責記住加密資料的長度，以便稍後可以為 [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) 函數指定適當的長度。</span><span class="sxs-lookup"><span data-stu-id="c5b18-121">The application is responsible for remembering the length of the encrypted data so the proper length can later be specified for the [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span>

     

5.  <span data-ttu-id="c5b18-122">（選擇性）使用 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) 函式，允許目前的使用者在未來解密資料。</span><span class="sxs-lookup"><span data-stu-id="c5b18-122">Optionally, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function to allow the current user to decrypt the data in the future.</span></span>

    <span data-ttu-id="c5b18-123">為了讓目前的使用者能夠在未來將資料解密， [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) 函式會用來將解密金鑰儲存為加密格式， (只能以使用者的私密金鑰解密的金鑰 BLOB) 。</span><span class="sxs-lookup"><span data-stu-id="c5b18-123">To allow the current user to decrypt the data in the future, the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function is used to save the decryption key in an encrypted form (a key BLOB) that can only be decrypted with the user's private key.</span></span> <span data-ttu-id="c5b18-124">此函式需要使用者的金鑰交換公開金鑰才能達成此目的，您可以使用 [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) 函數來取得此公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5b18-124">This function requires the user's key exchange public key for this purpose, which can be obtained by using the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function.</span></span> <span data-ttu-id="c5b18-125">**CryptExportKey** 函式會傳回必須由應用程式儲存以用於解密檔案的金鑰 BLOB</span><span class="sxs-lookup"><span data-stu-id="c5b18-125">The **CryptExportKey** function will return a key BLOB that must be stored by the application for use in decrypting the file</span></span>

> [!Note]  
> <span data-ttu-id="c5b18-126">如果應用程式的憑證 (或公開金鑰) 供其他使用者使用，則可讓其他使用者針對應該接收存取權的每個使用者執行 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) 呼叫，以將檔案解密。</span><span class="sxs-lookup"><span data-stu-id="c5b18-126">If the application has certificates (or public keys) for other users, it can permit other users to decrypt the file by performing [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls for each user who should receive access.</span></span> <span data-ttu-id="c5b18-127">傳回的金鑰 Blob 必須由應用程式儲存（如步驟5所示）。</span><span class="sxs-lookup"><span data-stu-id="c5b18-127">The returned key BLOBs must be stored by the application, as in step 5.</span></span>

 

## <a name="creating-an-encrypted-message"></a><span data-ttu-id="c5b18-128">建立加密的訊息</span><span class="sxs-lookup"><span data-stu-id="c5b18-128">Creating an Encrypted Message</span></span>

<span data-ttu-id="c5b18-129">簡化的訊息函數可讓您更輕鬆地加密和解密資料。</span><span class="sxs-lookup"><span data-stu-id="c5b18-129">The simplified message functions make it easier to encrypt and decrypt data.</span></span> <span data-ttu-id="c5b18-130">下圖描述必須完成才能加密訊息的個別工作。</span><span class="sxs-lookup"><span data-stu-id="c5b18-130">The following illustration depicts the individual tasks that must be accomplished to encrypt a message.</span></span> <span data-ttu-id="c5b18-131">下列清單將描述這些步驟。</span><span class="sxs-lookup"><span data-stu-id="c5b18-131">The steps are described in the following list.</span></span>

![加密訊息](images/encmsg.png)

<span data-ttu-id="c5b18-133">**加密訊息**</span><span class="sxs-lookup"><span data-stu-id="c5b18-133">**To encrypt a message**</span></span>

1.  <span data-ttu-id="c5b18-134">取得純文字訊息的指標。</span><span class="sxs-lookup"><span data-stu-id="c5b18-134">Get a pointer to the plaintext message.</span></span>
2.  <span data-ttu-id="c5b18-135">產生對稱 (會話) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5b18-135">Generate a symmetric (session) key.</span></span>
3.  <span data-ttu-id="c5b18-136">使用對稱金鑰和指定的加密演算法，加密訊息資料。</span><span class="sxs-lookup"><span data-stu-id="c5b18-136">Using the symmetric key and specified encryption algorithm, encrypt the message data.</span></span>
4.  <span data-ttu-id="c5b18-137">開啟憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="c5b18-137">Open a certificate store.</span></span>
5.  <span data-ttu-id="c5b18-138">取得收件者的憑證。</span><span class="sxs-lookup"><span data-stu-id="c5b18-138">Get the recipient's certificate.</span></span>
6.  <span data-ttu-id="c5b18-139">從收件者的憑證取得公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5b18-139">Get the public key from the recipient's certificate.</span></span>
7.  <span data-ttu-id="c5b18-140">使用收件者的公開金鑰加密對稱金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5b18-140">Using the recipient's public key, encrypt the symmetric key.</span></span>
8.  <span data-ttu-id="c5b18-141">從收件者的憑證取得收件者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5b18-141">Get the recipient's identifier from the recipient's certificate.</span></span>
9.  <span data-ttu-id="c5b18-142">在數位封包訊息中包含下列內容：資料加密演算法、加密的資料、加密的對稱金鑰，以及收件者識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5b18-142">Include the following in the digitally enveloped message: the data encryption algorithm, the encrypted data, the encrypted symmetric key, and the recipient identifier.</span></span>

 

 



