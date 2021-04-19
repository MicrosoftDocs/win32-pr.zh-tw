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
# <a name="verifying-a-signed-message"></a><span data-ttu-id="d5b27-103">驗證已簽署的訊息</span><span class="sxs-lookup"><span data-stu-id="d5b27-103">Verifying a Signed Message</span></span>

<span data-ttu-id="d5b27-104">這些步驟會驗證已簽署資料的簽章。</span><span class="sxs-lookup"><span data-stu-id="d5b27-104">These steps verify the signature of signed data.</span></span> <span data-ttu-id="d5b27-105">下圖說明必須完成的個別工作，如其後的清單所示。</span><span class="sxs-lookup"><span data-stu-id="d5b27-105">The following illustration depicts the individual tasks that must be accomplished, as shown in the list that follows it.</span></span>

![驗證已簽署的訊息](images/verifmsg.png)

<span data-ttu-id="d5b27-107">**驗證已簽署訊息的簽章**</span><span class="sxs-lookup"><span data-stu-id="d5b27-107">**To verify the signature of a signed message**</span></span>

1.  <span data-ttu-id="d5b27-108">取得已簽署訊息的指標。</span><span class="sxs-lookup"><span data-stu-id="d5b27-108">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="d5b27-109">開啟 [*憑證存放區*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="d5b27-109">Open a [*certificate store*](../secgloss/c-gly.md).</span></span>
3.  <span data-ttu-id="d5b27-110">使用訊息中包含的簽署者識別碼，取得寄件者的憑證，並取得其 [*公開金鑰*](../secgloss/p-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d5b27-110">Using the signer ID contained in the message, get the sender's certificate and get a handle to its [*public key*](../secgloss/p-gly.md).</span></span>

    <span data-ttu-id="d5b27-111">除了步驟2和3，您也可以使用訊息中包含的憑證來取得簽署者的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="d5b27-111">As an alternative to steps 2 and 3, you can use the certificate contained in the message to retrieve the signer's public key.</span></span>

4.  <span data-ttu-id="d5b27-112">使用簽署人的公開金鑰，將數位簽章解密，以產生訊息中的原始資料摘要。</span><span class="sxs-lookup"><span data-stu-id="d5b27-112">Using the signer's public key, decrypt the digital signature, producing the original digest of the data in the message.</span></span>
5.  <span data-ttu-id="d5b27-113">使用訊息中包含的雜湊演算法， [*雜湊*](../secgloss/h-gly.md) 訊息中包含的資料，產生新的摘要。</span><span class="sxs-lookup"><span data-stu-id="d5b27-113">Using the hash algorithm contained in the message, [*hash*](../secgloss/h-gly.md) the data contained in the message, yielding a new digest.</span></span>
6.  <span data-ttu-id="d5b27-114">將從訊息中取出的摘要，與剛建立的新摘要進行比較。</span><span class="sxs-lookup"><span data-stu-id="d5b27-114">Compare the digest retrieved from the message with the new digest just created.</span></span>
7.  <span data-ttu-id="d5b27-115">如果這兩個摘要相符，就會驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="d5b27-115">If the two digests match, the signature is verified.</span></span> <span data-ttu-id="d5b27-116">這表示用來簽署資料的 [*私密金鑰*](../secgloss/p-gly.md) 會符合單純用來解密簽章的公開金鑰，而且資料在簽署之後也不會變更。</span><span class="sxs-lookup"><span data-stu-id="d5b27-116">This means that the [*private key*](../secgloss/p-gly.md) that was used to sign the data matches the public key just used to decrypt the signature, and that the data has not changed since the data was signed.</span></span>

    <span data-ttu-id="d5b27-117">如果這兩個摘要不符，則不會驗證簽章，而且私用/公開金鑰不相符，或是資料在簽署之後或兩者皆已變更。</span><span class="sxs-lookup"><span data-stu-id="d5b27-117">If the two digests do not match, the signature is not verified, and either the private/public keys do not match, or the data has been changed since the data was signed, or both.</span></span>

<span data-ttu-id="d5b27-118">單一函式 [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)可以用來驗證簽章，如下列程式所示。</span><span class="sxs-lookup"><span data-stu-id="d5b27-118">A single function, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), can be used to verify a signature, as shown in the following procedure.</span></span>

<span data-ttu-id="d5b27-119">**驗證已簽署的訊息**</span><span class="sxs-lookup"><span data-stu-id="d5b27-119">**To verify a signed message**</span></span>

1.  <span data-ttu-id="d5b27-120">取得已簽署訊息的指標。</span><span class="sxs-lookup"><span data-stu-id="d5b27-120">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="d5b27-121">取得已簽署訊息的大小。</span><span class="sxs-lookup"><span data-stu-id="d5b27-121">Get the size of the signed message.</span></span>
3.  <span data-ttu-id="d5b27-122">取得密碼編譯提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d5b27-122">Get a handle on a cryptographic provider.</span></span>
4.  <span data-ttu-id="d5b27-123">將 [**CRYPT \_ 驗證訊息 \_ 的 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) 結構初始化。</span><span class="sxs-lookup"><span data-stu-id="d5b27-123">Initialize the [**CRYPT\_VERIFY\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) structure.</span></span>
5.  <span data-ttu-id="d5b27-124">呼叫 [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) 來驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="d5b27-124">Call [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) to verify the signature.</span></span>

<span data-ttu-id="d5b27-125">範例 C 程式中包含了可 [執行此程式的程式碼：簽署訊息和驗證訊息簽](example-c-program-signing-a-message-and-verifying-a-message-signature.md)章。</span><span class="sxs-lookup"><span data-stu-id="d5b27-125">Code that implements this procedure is included in [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
