---
description: 密碼編譯訊息語法可以用來編碼封包訊息。
ms.assetid: f35aacda-6827-42e9-b7ac-58dc007fc697
title: 編碼封包資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dc20fc7483ba1ef364d8b59824d26bd14d458d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556585"
---
# <a name="encoding-enveloped-data"></a><span data-ttu-id="de109-103">編碼封包資料</span><span class="sxs-lookup"><span data-stu-id="de109-103">Encoding Enveloped Data</span></span>

<span data-ttu-id="de109-104">封包資料包含一或多個收件者之任何類型和加密內容加密工作階段金鑰的加密內容。</span><span class="sxs-lookup"><span data-stu-id="de109-104">Enveloped data consists of encrypted content of any type and encrypted content-encryption session keys for one or more recipients.</span></span> <span data-ttu-id="de109-105">封包訊息會保留訊息秘密的內容，並只允許指定的人員或實體取得內容。</span><span class="sxs-lookup"><span data-stu-id="de109-105">Enveloped messages keep the contents of the message secret and allow only specified persons or entities to retrieve the contents.</span></span>

<span data-ttu-id="de109-106"> (CMS) 的密碼編譯訊息語法可以用來編碼封包訊息。</span><span class="sxs-lookup"><span data-stu-id="de109-106">Cryptographic message syntax (CMS) can be used to encode enveloped messages.</span></span> <span data-ttu-id="de109-107">CMS 支援三種金鑰管理技術：金鑰傳輸、金鑰協定和先前散發的對稱金鑰加密金鑰 (KEK) 。</span><span class="sxs-lookup"><span data-stu-id="de109-107">CMS supports three key management techniques: key transport, key agreement, and previously distributed symmetric key-encryption keys (KEK).</span></span> <span data-ttu-id="de109-108">先前散發的對稱 KEK 也稱為「郵寄清單金鑰散發」。</span><span class="sxs-lookup"><span data-stu-id="de109-108">Previously distributed symmetric KEK are also known as mailing list key distribution.</span></span>

<span data-ttu-id="de109-109">在這三種技術中，會產生單一工作階段金鑰來加密封包訊息。</span><span class="sxs-lookup"><span data-stu-id="de109-109">In each of these three techniques, a single session key is generated to encrypt the enveloped message.</span></span> <span data-ttu-id="de109-110">金鑰管理問題會處理寄件者加密工作階段金鑰的方式，並由接收者解密。</span><span class="sxs-lookup"><span data-stu-id="de109-110">Key management issues deal with the way that session key is encrypted by the sender and decrypted by a receiver.</span></span> <span data-ttu-id="de109-111">您可以使用混合的金鑰管理技術，將單一加密的訊息散發給許多收件者。</span><span class="sxs-lookup"><span data-stu-id="de109-111">A single encrypted message can be distributed to many recipients using a mixture of the key management techniques.</span></span>

<span data-ttu-id="de109-112">金鑰傳輸金鑰管理使用預定接收者的公開金鑰來加密工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="de109-112">Key transport key management uses an intended receiver's public key to encrypt the session key.</span></span> <span data-ttu-id="de109-113">接收者會使用與用來加密的公開金鑰相關聯的私密金鑰來解密工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="de109-113">The receiver decrypts the session key using the private key associated with the public key that was used to encrypt.</span></span> <span data-ttu-id="de109-114">然後接收者會使用解密的工作階段金鑰來解密封包資料。</span><span class="sxs-lookup"><span data-stu-id="de109-114">The receiver then uses the decrypted session key to decrypt the enveloped data.</span></span> <span data-ttu-id="de109-115">使用金鑰傳輸時，接收者尚未確認傳送端身分識別的資訊。</span><span class="sxs-lookup"><span data-stu-id="de109-115">When key transport is used, the receiver has not confirmed information on the identity of the sender.</span></span>

<span data-ttu-id="de109-116">在金鑰協定管理中，會產生暫時的暫時 Diffie-Hellman 私密金鑰，並使用此金鑰來加密工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="de109-116">In key agreement management, a temporary, ephemeral Diffie-Hellman private key is generated and used to encrypt the session key.</span></span> <span data-ttu-id="de109-117">與暫時私密金鑰對應的公開金鑰會包含在郵件的收件者資訊中。</span><span class="sxs-lookup"><span data-stu-id="de109-117">The public key corresponding to the ephemeral private key is included as part of the message's recipient information.</span></span> <span data-ttu-id="de109-118">收件者會使用收到的暫時金鑰來解密工作階段金鑰，並使用此解密的工作階段金鑰來解密封包訊息。</span><span class="sxs-lookup"><span data-stu-id="de109-118">The recipient decrypts the session key using the received ephemeral key and uses this decrypted session key to decrypt the enveloped message.</span></span> <span data-ttu-id="de109-119">使用暫時金鑰協定搭配接收者的私密金鑰時，訊息接收者會在傳送者的身分識別上確認資訊。</span><span class="sxs-lookup"><span data-stu-id="de109-119">Using ephemeral key agreement in conjunction with the receiver's private key, the message receiver does have confirmed information on the identity of the sender.</span></span>

<span data-ttu-id="de109-120">針對使用先前分散式 [*對稱金鑰*](../secgloss/s-gly.md)的金鑰管理，每個訊息都包含以先前分散式金鑰加密金鑰加密的內容加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="de109-120">For key management using previously distributed [*symmetric keys*](../secgloss/s-gly.md), each message includes the content-encryption key that has been encrypted with a previously distributed key-encryption key.</span></span> <span data-ttu-id="de109-121">接收者會使用先前散發的金鑰加密金鑰來解密內容加密金鑰，然後使用解密的內容加密金鑰來解密封包訊息。</span><span class="sxs-lookup"><span data-stu-id="de109-121">Receivers use the previously distributed key-encryption key to decrypt the content encryption key, then use the decrypted content-encryption key to decrypt the enveloped message.</span></span>

<span data-ttu-id="de109-122">下圖顯示用於編碼封包資料的一般 CMS 事件序列。</span><span class="sxs-lookup"><span data-stu-id="de109-122">A typical CMS sequence of events for encoding enveloped data, is shown in the following illustration.</span></span>

![編碼封包資料](images/envelmsg.png)

-   <span data-ttu-id="de109-124">將會取出 [*純文字*](../secgloss/p-gly.md) 訊息的指標。</span><span class="sxs-lookup"><span data-stu-id="de109-124">A pointer to the [*plaintext*](../secgloss/p-gly.md) message is retrieved.</span></span>
-   <span data-ttu-id="de109-125">產生對稱 ([*會話*](../secgloss/s-gly.md)) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="de109-125">A symmetric ([*session*](../secgloss/s-gly.md)) key is generated.</span></span>
-   <span data-ttu-id="de109-126">[*對稱金鑰*](../secgloss/s-gly.md)和指定的加密演算法會用來加密訊息資料。</span><span class="sxs-lookup"><span data-stu-id="de109-126">The [*symmetric key*](../secgloss/s-gly.md) and specified encryption algorithm are used to encrypt the message data.</span></span>
-   <span data-ttu-id="de109-127">即會開啟 [*憑證存放區*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="de109-127">A [*certificate store*](../secgloss/c-gly.md) is opened.</span></span>
-   <span data-ttu-id="de109-128">收件者的憑證會從存放區中取出。</span><span class="sxs-lookup"><span data-stu-id="de109-128">The recipient's certificate is retrieved from the store.</span></span>
-   <span data-ttu-id="de109-129">從收件者的憑證中取出 [*公開金鑰*](../secgloss/p-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="de109-129">The [*public key*](../secgloss/p-gly.md) is retrieved from the recipient's certificate.</span></span>
-   <span data-ttu-id="de109-130">使用收件者的公開金鑰，對稱金鑰會加密。</span><span class="sxs-lookup"><span data-stu-id="de109-130">Using the recipient's public key, the symmetric key is encrypted.</span></span>
-   <span data-ttu-id="de109-131">從收件者的憑證中，會取出收件者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="de109-131">From the recipient's certificate, the recipient's ID is retrieved.</span></span>
-   <span data-ttu-id="de109-132">數位封包訊息中包含下列資訊：資料加密演算法、加密的資料、加密的對稱金鑰，以及收件者資訊結構。</span><span class="sxs-lookup"><span data-stu-id="de109-132">The following information is included in the digitally enveloped message: the data encryption algorithm, the encrypted data, the encrypted symmetric key, and the recipient information structure.</span></span>

<span data-ttu-id="de109-133">若要使用低層級的訊息函數來完成剛剛列出的一般工作，請使用下列程式。</span><span class="sxs-lookup"><span data-stu-id="de109-133">To use low-level message functions to accomplish the typical tasks just listed, use the following procedure.</span></span>

<span data-ttu-id="de109-134">**編碼封包訊息**</span><span class="sxs-lookup"><span data-stu-id="de109-134">**To encode an enveloped message**</span></span>

1.  <span data-ttu-id="de109-135">建立或抓取內容。</span><span class="sxs-lookup"><span data-stu-id="de109-135">Create or retrieve the content.</span></span>
2.  <span data-ttu-id="de109-136">取得密碼編譯提供者。</span><span class="sxs-lookup"><span data-stu-id="de109-136">Get a cryptographic provider.</span></span>
3.  <span data-ttu-id="de109-137">取得收件者憑證。</span><span class="sxs-lookup"><span data-stu-id="de109-137">Get a recipient certificate.</span></span>
4.  <span data-ttu-id="de109-138">將 [**CMSG 的 \_ 封裝 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) 結構初始化。</span><span class="sxs-lookup"><span data-stu-id="de109-138">Initialize the [**CMSG\_ENVELOPED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) structure.</span></span>
5.  <span data-ttu-id="de109-139">呼叫 [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) 以取得編碼訊息 BLOB 的大小。</span><span class="sxs-lookup"><span data-stu-id="de109-139">Call [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) to get the size of the encoded message BLOB.</span></span> <span data-ttu-id="de109-140">為它配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="de109-140">Allocate memory for it.</span></span>
6.  <span data-ttu-id="de109-141">呼叫 [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)，傳入 CMSG \_ 的 *dwMsgType* 封包，以及 [**CMSG \_ 封包 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) 的指標以進行 *pvMsgEncodeInfo*。</span><span class="sxs-lookup"><span data-stu-id="de109-141">Call [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passing in CMSG\_ENVELOPED for *dwMsgType* and a pointer to [**CMSG\_ENVELOPED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) for *pvMsgEncodeInfo*.</span></span> <span data-ttu-id="de109-142">由於這個呼叫，您將會取得已開啟之訊息的控制碼。</span><span class="sxs-lookup"><span data-stu-id="de109-142">As a result of this call, you will get a handle to the opened message.</span></span>
7.  <span data-ttu-id="de109-143">呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)，傳入步驟6中抓取的控制碼，以及要加密、封裝和編碼的資料指標。</span><span class="sxs-lookup"><span data-stu-id="de109-143">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), passing in the handle retrieved in step 6 and a pointer to the data that is to be encrypted, enveloped, and encoded.</span></span> <span data-ttu-id="de109-144">您可以視需要多次呼叫這個函式，以完成編碼程式。</span><span class="sxs-lookup"><span data-stu-id="de109-144">This function can be called as many times as necessary to complete the encoding process.</span></span>
8.  <span data-ttu-id="de109-145">呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入步驟6中取出的控制碼和適當的參數類型，以存取所需的編碼資料。</span><span class="sxs-lookup"><span data-stu-id="de109-145">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 6 and the appropriate parameter types to access the desired, encoded data.</span></span> <span data-ttu-id="de109-146">例如，傳入 CMSG \_ CONTENT \_ PARAM 以取得整個 PKCS \# 7 訊息的指標。</span><span class="sxs-lookup"><span data-stu-id="de109-146">For example, pass in CMSG\_CONTENT\_PARAM to get a pointer to the entire PKCS \#7 message.</span></span>

    <span data-ttu-id="de109-147">如果此編碼的結果是當做另一個編碼訊息的 [*內部資料*](../secgloss/i-gly.md) 使用，例如封包訊息，則 \_ 必須傳遞 CMSG 的 BARE \_ 內容 \_ 參數參數。</span><span class="sxs-lookup"><span data-stu-id="de109-147">If the result of this encoding is to be used as the [*inner data*](../secgloss/i-gly.md) for another encoded message, such as an enveloped message, the CMSG\_BARE\_CONTENT\_PARAM parameter must be passed.</span></span> <span data-ttu-id="de109-148">如需範例，請參閱 [編碼封包訊息的替代程式碼](alternate-code-for-encoding-an-enveloped-message.md)。</span><span class="sxs-lookup"><span data-stu-id="de109-148">For an example, see [Alternate Code for Encoding an Enveloped Message](alternate-code-for-encoding-an-enveloped-message.md).</span></span>

9.  <span data-ttu-id="de109-149">藉由呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)來關閉訊息。</span><span class="sxs-lookup"><span data-stu-id="de109-149">Close the message by calling [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).</span></span>

<span data-ttu-id="de109-150">此程式的結果是編碼的訊息，其中包含加密的資料、以收件者公開金鑰加密的 [*對稱金鑰*](../secgloss/s-gly.md) ，以及收件者資訊資料結構。</span><span class="sxs-lookup"><span data-stu-id="de109-150">The result of this procedure is an encoded message that contains the encrypted data, the [*symmetric key*](../secgloss/s-gly.md) that is encrypted with the recipient's public keys, and the recipient information data structures.</span></span> <span data-ttu-id="de109-151">加密內容和收件者加密對稱金鑰的組合是該收件者的 [*數位信封*](../secgloss/d-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="de109-151">The combination of encrypted content and an encrypted symmetric key for a recipient is a [*digital envelope*](../secgloss/d-gly.md) for that recipient.</span></span> <span data-ttu-id="de109-152">您可以針對多個收件者將任何類型的內容封包。</span><span class="sxs-lookup"><span data-stu-id="de109-152">Any type of content can be enveloped for multiple recipients.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de109-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="de109-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de109-154">範例 C 程式：編碼封包、簽署的訊息</span><span class="sxs-lookup"><span data-stu-id="de109-154">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
