---
description: 描述編碼已簽署訊息的程式。
ms.assetid: 40d1c417-6d88-4421-920f-8b40d88d28ce
title: 編碼簽署的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4a542fe0890a6ee9d51ebc1a5ee6b98bab4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194177"
---
# <a name="encoding-signed-data"></a><span data-ttu-id="7a93f-103">編碼簽署的資料</span><span class="sxs-lookup"><span data-stu-id="7a93f-103">Encoding Signed Data</span></span>

<span data-ttu-id="7a93f-104">[*帶正負*](../secgloss/s-gly.md) 號的資料是由零個或更多個簽署者之內容的任何類型和加密訊息 [*雜湊*](../secgloss/h-gly.md) 的內容所組成。</span><span class="sxs-lookup"><span data-stu-id="7a93f-104">[*Signed data*](../secgloss/s-gly.md) consists of content of any type and encrypted message [*hashes*](../secgloss/h-gly.md) of the content by zero or more signers.</span></span> <span data-ttu-id="7a93f-105">產生的雜湊可以確認原始訊息在簽署後未經過修改，且該特定人員或實體已簽署資料。</span><span class="sxs-lookup"><span data-stu-id="7a93f-105">The resulting hash can confirm that the original message has not been modified since signing and that particular persons or entities signed the data.</span></span>

<span data-ttu-id="7a93f-106">下圖描述編碼已簽署訊息的程式。</span><span class="sxs-lookup"><span data-stu-id="7a93f-106">The following illustration depicts the procedure for encoding a signed message.</span></span> <span data-ttu-id="7a93f-107">下圖中的清單描述這些步驟。</span><span class="sxs-lookup"><span data-stu-id="7a93f-107">The list following the illustration describes the steps.</span></span>

<span data-ttu-id="7a93f-108">訊息可能會有多個「簽署者」、「雜湊演算法」和「憑證」。</span><span class="sxs-lookup"><span data-stu-id="7a93f-108">A message may have multiple signers, hashing algorithms, and certificates.</span></span> <span data-ttu-id="7a93f-109">雖然圖例只顯示憑證、 [*crl*](../secgloss/c-gly.md)和 [*ctl*](../secgloss/c-gly.md) 都可以使用相同的進程。</span><span class="sxs-lookup"><span data-stu-id="7a93f-109">While the illustration shows only certificates, [*CRLs*](../secgloss/c-gly.md), and [*CTLs*](../secgloss/c-gly.md) can use the same process.</span></span> <span data-ttu-id="7a93f-110">它們可放在顯示憑證的任何位置。</span><span class="sxs-lookup"><span data-stu-id="7a93f-110">They would fit into the illustration wherever certificates are shown.</span></span>

![編碼已簽署的訊息](images/signmsg2.png)

<span data-ttu-id="7a93f-112">編碼 [*簽署資料*](../secgloss/s-gly.md) 的一般程式如下所示。</span><span class="sxs-lookup"><span data-stu-id="7a93f-112">The general process for encoding [*Signed data*](../secgloss/s-gly.md) is as follows.</span></span>

<span data-ttu-id="7a93f-113">**編碼簽署的資料**</span><span class="sxs-lookup"><span data-stu-id="7a93f-113">**To encode signed data**</span></span>

1.  <span data-ttu-id="7a93f-114">必要時，會 (建立資料) ，並抓取其指標。</span><span class="sxs-lookup"><span data-stu-id="7a93f-114">The data is created (if necessary), and a pointer to it is retrieved.</span></span>
2.  <span data-ttu-id="7a93f-115">開啟的 [*憑證存放區*](../secgloss/c-gly.md) 包含簽署者的憑證。</span><span class="sxs-lookup"><span data-stu-id="7a93f-115">A [*certificate store*](../secgloss/c-gly.md) is opened that contains the signer's certificate.</span></span>
3.  <span data-ttu-id="7a93f-116">取得憑證的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="7a93f-116">The private key for the certificate is retrieved.</span></span> <span data-ttu-id="7a93f-117">在使用憑證之前，必須在憑證上設定兩個屬性。</span><span class="sxs-lookup"><span data-stu-id="7a93f-117">There are two properties that must be set on the certificate before using it.</span></span> <span data-ttu-id="7a93f-118">一個是用來將憑證系結至特定的 CSP，並在該 CSP 內系結至特定的私密金鑰 [*容器*](../secgloss/k-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="7a93f-118">One is used to tie a certificate to a particular CSP and, within that CSP, to a particular private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="7a93f-119">另一個用來指出呼叫 [*雜湊*](../secgloss/h-gly.md) 作業時要使用的雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7a93f-119">The other is used to indicate which hashing algorithm is to be used when a [*hash*](../secgloss/h-gly.md) operation is called.</span></span> <span data-ttu-id="7a93f-120">這些只需要設定一次。</span><span class="sxs-lookup"><span data-stu-id="7a93f-120">These need only be set once.</span></span>
4.  <span data-ttu-id="7a93f-121">憑證的屬性會決定雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7a93f-121">A certificate's property determines the hash algorithm.</span></span>
5.  <span data-ttu-id="7a93f-122">透過雜湊函數傳送資料，即可建立資料的雜湊。</span><span class="sxs-lookup"><span data-stu-id="7a93f-122">A hash of the data is created by sending the data through the hashing function.</span></span>
6.  <span data-ttu-id="7a93f-123">簽章是使用私密金鑰（透過憑證上的屬性取得）的加密雜湊所建立。</span><span class="sxs-lookup"><span data-stu-id="7a93f-123">The signature is created by encrypting the hash using the private key, obtained through a property on the certificate.</span></span>
7.  <span data-ttu-id="7a93f-124">已完成、已簽署的訊息中包含下列資料：</span><span class="sxs-lookup"><span data-stu-id="7a93f-124">The following data is included in the finished, signed message:</span></span>
    -   <span data-ttu-id="7a93f-125">要簽署的原始資料</span><span class="sxs-lookup"><span data-stu-id="7a93f-125">The original data to be signed</span></span>
    -   <span data-ttu-id="7a93f-126">雜湊演算法</span><span class="sxs-lookup"><span data-stu-id="7a93f-126">The hash algorithms</span></span>
    -   <span data-ttu-id="7a93f-127">簽章</span><span class="sxs-lookup"><span data-stu-id="7a93f-127">The signatures</span></span>
    -   <span data-ttu-id="7a93f-128">簽署者資訊結構，其中包括簽署者識別碼 (憑證簽發者和序號) </span><span class="sxs-lookup"><span data-stu-id="7a93f-128">The signer info structures, which includes the signer identifier (certificate issuer and serial number)</span></span>
    -   <span data-ttu-id="7a93f-129">簽署者的憑證 (選用) </span><span class="sxs-lookup"><span data-stu-id="7a93f-129">The signer's certificates (optional)</span></span>

<span data-ttu-id="7a93f-130">此程式說明簡單的案例。</span><span class="sxs-lookup"><span data-stu-id="7a93f-130">This procedure illustrates a simple case.</span></span> <span data-ttu-id="7a93f-131">更複雜的案例牽涉到訊息中包含已驗證的屬性。</span><span class="sxs-lookup"><span data-stu-id="7a93f-131">More complex cases involve authenticated attributes included in the message.</span></span> <span data-ttu-id="7a93f-132">當內容類型是除了 **位元組** 字串的任何內容，或至少有一個已驗證的屬性與任何資料類型時，需要兩個標準的已驗證屬性：內容 (資料) 類型，以及內容的雜湊。</span><span class="sxs-lookup"><span data-stu-id="7a93f-132">When the content type is anything but a **BYTE** string, or there is at least one authenticated attribute along with any data type, there are two standard authenticated attributes required: the content (data) type, and the hash of the content.</span></span> <span data-ttu-id="7a93f-133">在這些情況下， [*CryptoAPI*](../secgloss/c-gly.md) 會自動提供這兩個必要的屬性。</span><span class="sxs-lookup"><span data-stu-id="7a93f-133">Under these circumstances, the [*CryptoAPI*](../secgloss/c-gly.md) automatically provides these two required attributes.</span></span> <span data-ttu-id="7a93f-134">低層級訊息函式會將已驗證的屬性雜湊、使用私密金鑰來加密雜湊，並將其提供為簽章。</span><span class="sxs-lookup"><span data-stu-id="7a93f-134">The low-level message functions hash the authenticated attributes, encrypt the hash with the private key, and provide this as the signature.</span></span>

<span data-ttu-id="7a93f-135">使用下列程式，使用低層級的訊息函式來完成剛剛列出的工作。</span><span class="sxs-lookup"><span data-stu-id="7a93f-135">Use the low-level message functions to accomplish the tasks just listed, by using the following procedure.</span></span>

<span data-ttu-id="7a93f-136">**編碼已簽署的訊息**</span><span class="sxs-lookup"><span data-stu-id="7a93f-136">**To encode a signed message**</span></span>

1.  <span data-ttu-id="7a93f-137">建立或抓取內容。</span><span class="sxs-lookup"><span data-stu-id="7a93f-137">Create or retrieve the content.</span></span>
2.  <span data-ttu-id="7a93f-138">取得密碼編譯提供者。</span><span class="sxs-lookup"><span data-stu-id="7a93f-138">Get a cryptographic provider.</span></span>
3.  <span data-ttu-id="7a93f-139">取得簽署者憑證。</span><span class="sxs-lookup"><span data-stu-id="7a93f-139">Get the signer certificates.</span></span>
4.  <span data-ttu-id="7a93f-140">將 [**CMSG \_ 簽署者 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) 結構初始化。</span><span class="sxs-lookup"><span data-stu-id="7a93f-140">Initialize the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure.</span></span>
5.  <span data-ttu-id="7a93f-141">將 [**CMSG \_ 簽署的 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) 結構初始化。</span><span class="sxs-lookup"><span data-stu-id="7a93f-141">Initialize the [**CMSG\_SIGNED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) structure.</span></span>
6.  <span data-ttu-id="7a93f-142">呼叫 [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) 以取得編碼訊息 BLOB 的大小。</span><span class="sxs-lookup"><span data-stu-id="7a93f-142">Call [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) to get the size of the encoded message BLOB.</span></span> <span data-ttu-id="7a93f-143">為它配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="7a93f-143">Allocate memory for it.</span></span>
7.  <span data-ttu-id="7a93f-144">呼叫 [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)，傳入 CMSG \_ 帶正負號 *的 dwMsgType* ，以及 [**CMSG 簽署的 \_ \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info)指標以取得已開啟之訊息的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7a93f-144">Call [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passing in CMSG\_SIGNED for *dwMsgType* and a pointer to [**CMSG\_SIGNED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) for *pvMsgEncodeInfo* to get a handle to the opened message.</span></span>
8.  <span data-ttu-id="7a93f-145">呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)，傳入步驟7中取出的控制碼，以及要簽署及編碼的資料指標。</span><span class="sxs-lookup"><span data-stu-id="7a93f-145">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), passing in the handle retrieved in step 7, and a pointer to the data that is to be signed and encoded.</span></span> <span data-ttu-id="7a93f-146">您可以視需要多次呼叫這個函式，以完成編碼程式。</span><span class="sxs-lookup"><span data-stu-id="7a93f-146">This function can be called as many times as necessary to complete the encoding process.</span></span>
9.  <span data-ttu-id="7a93f-147">呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入步驟7中取出的控制碼和適當的參數類型，以存取所需的編碼資料。</span><span class="sxs-lookup"><span data-stu-id="7a93f-147">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 7 and the appropriate parameter types to access the desired, encoded data.</span></span> <span data-ttu-id="7a93f-148">例如，傳入 CMSG \_ CONTENT \_ PARAM 以取得整個 [*PKCS \# 7*](../secgloss/p-gly.md) 訊息的指標。</span><span class="sxs-lookup"><span data-stu-id="7a93f-148">For example, pass in CMSG\_CONTENT\_PARAM to get a pointer to the entire [*PKCS \#7*](../secgloss/p-gly.md) message.</span></span>

    <span data-ttu-id="7a93f-149">如果此編碼的結果是當做另一個編碼訊息的 [*內部資料*](../secgloss/i-gly.md) 使用，例如封包訊息，則 \_ 必須傳遞 CMSG 的 BARE \_ 內容 \_ 參數參數。</span><span class="sxs-lookup"><span data-stu-id="7a93f-149">If the result of this encoding is to be used as the [*inner data*](../secgloss/i-gly.md) for another encoded message, such as an enveloped message, the CMSG\_BARE\_CONTENT\_PARAM parameter must be passed.</span></span> <span data-ttu-id="7a93f-150">如需顯示此情況的範例，請參閱 [編碼封包訊息的替代程式碼](alternate-code-for-encoding-an-enveloped-message.md)。</span><span class="sxs-lookup"><span data-stu-id="7a93f-150">For an example showing this, see [Alternate Code for Encoding an Enveloped Message](alternate-code-for-encoding-an-enveloped-message.md).</span></span>

10. <span data-ttu-id="7a93f-151">藉由呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)來關閉訊息。</span><span class="sxs-lookup"><span data-stu-id="7a93f-151">Close the message by calling [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).</span></span>

<span data-ttu-id="7a93f-152">此程式的結果是編碼的訊息，其中包含原始資料、該資料的加密雜湊 (簽章) 和簽署者資訊。</span><span class="sxs-lookup"><span data-stu-id="7a93f-152">The result of this procedure is an encoded message that contains the original data, the encrypted hash of that data (signature), and the signer information.</span></span> <span data-ttu-id="7a93f-153">另外還有指向所需編碼 BLOB 的指標。</span><span class="sxs-lookup"><span data-stu-id="7a93f-153">There is also a pointer to the desired, encoded BLOB.</span></span>

<span data-ttu-id="7a93f-154">如需 C 編碼的詳細資料，請參閱 [c 程式範例：簽署、編碼、解碼和驗證訊息](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)。</span><span class="sxs-lookup"><span data-stu-id="7a93f-154">For C coding details, see [Example C Program: Signing, Encoding, Decoding, and Verifying a Message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span></span>

 

 
