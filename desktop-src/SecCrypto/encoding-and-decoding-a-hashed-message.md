---
description: 描述編碼雜湊訊息所需的工作。
ms.assetid: c1a65452-c634-4cc6-9afe-d6bf11d999d1
title: 編碼和解碼雜湊訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91d165634c1ae00a59f2c77b1fc5a36b53dbd96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975412"
---
# <a name="encoding-and-decoding-a-hashed-message"></a><span data-ttu-id="3598e-103">編碼和解碼雜湊訊息</span><span class="sxs-lookup"><span data-stu-id="3598e-103">Encoding and Decoding a Hashed Message</span></span>

<span data-ttu-id="3598e-104">雜湊資料是由任何類型的內容和內容的 [*雜湊*](../secgloss/h-gly.md) 所組成。</span><span class="sxs-lookup"><span data-stu-id="3598e-104">Hashed data consists of content of any type and a [*hash*](../secgloss/h-gly.md) of the content.</span></span> <span data-ttu-id="3598e-105">只有在建立雜湊之後，才需要確認訊息內容尚未經過修改，才能使用它。</span><span class="sxs-lookup"><span data-stu-id="3598e-105">It can be used when it is only necessary to confirm that the message content has not been modified since the hash was created.</span></span>

<span data-ttu-id="3598e-106">建立雜湊訊息時，可能會有多個雜湊演算法和多個雜湊。</span><span class="sxs-lookup"><span data-stu-id="3598e-106">When creating a hashed message, there can be multiple hash algorithms and multiple hashes.</span></span> <span data-ttu-id="3598e-107">下圖描述編碼雜湊訊息所需的工作。</span><span class="sxs-lookup"><span data-stu-id="3598e-107">The following illustration depicts the tasks required to encode a hashed message.</span></span> <span data-ttu-id="3598e-108">程式如下圖所述。</span><span class="sxs-lookup"><span data-stu-id="3598e-108">The procedure is described in the text that follows the illustration.</span></span>

![建立雜湊訊息](images/hashmsg.png)

<span data-ttu-id="3598e-110">**建立雜湊訊息**</span><span class="sxs-lookup"><span data-stu-id="3598e-110">**To create a hashed message**</span></span>

1.  <span data-ttu-id="3598e-111">取得要雜湊之資料的指標。</span><span class="sxs-lookup"><span data-stu-id="3598e-111">Get a pointer to the data to be hashed.</span></span>
2.  <span data-ttu-id="3598e-112">選取要使用的雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="3598e-112">Select the hash algorithm to be used.</span></span>
3.  <span data-ttu-id="3598e-113">使用雜湊演算法，透過雜湊函數來放置資料。</span><span class="sxs-lookup"><span data-stu-id="3598e-113">Put the data through a hashing function using the hash algorithm.</span></span>
4.  <span data-ttu-id="3598e-114">包含要雜湊處理的原始資料、雜湊演算法，以及編碼訊息中的雜湊。</span><span class="sxs-lookup"><span data-stu-id="3598e-114">Include the original data to be hashed, the hashing algorithms, and the hashes in the encoded message.</span></span>

<span data-ttu-id="3598e-115">若要使用低層級的訊息函式來完成剛剛所述的工作，請使用下列程式。</span><span class="sxs-lookup"><span data-stu-id="3598e-115">To use low-level message functions to accomplish the tasks just outlined, use the following procedure.</span></span>

<span data-ttu-id="3598e-116">**使用低層級訊息函式來雜湊和編碼訊息**</span><span class="sxs-lookup"><span data-stu-id="3598e-116">**To hash and encode a message using low-level message functions**</span></span>

1.  <span data-ttu-id="3598e-117">建立或取出要進行雜湊處理的內容。</span><span class="sxs-lookup"><span data-stu-id="3598e-117">Create or retrieve the content to be hashed.</span></span>
2.  <span data-ttu-id="3598e-118">取得密碼編譯提供者。</span><span class="sxs-lookup"><span data-stu-id="3598e-118">Get a cryptographic provider.</span></span>
3.  <span data-ttu-id="3598e-119">將 [**CMSG \_ 雜湊 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) 結構初始化。</span><span class="sxs-lookup"><span data-stu-id="3598e-119">Initialize the [**CMSG\_HASHED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) structure.</span></span>
4.  <span data-ttu-id="3598e-120">呼叫 [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) 以取得編碼訊息 BLOB 的大小。</span><span class="sxs-lookup"><span data-stu-id="3598e-120">Call [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) to get the size of the encoded message BLOB.</span></span> <span data-ttu-id="3598e-121">為它配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="3598e-121">Allocate memory for it.</span></span>
5.  <span data-ttu-id="3598e-122">呼叫 [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)，傳入 CMSG \_ 雜湊的 *DwMsgType* 參數，以及 CMSG 參數 [**的 \_ 雜湊 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info)指標 。</span><span class="sxs-lookup"><span data-stu-id="3598e-122">Call [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passing in CMSG\_HASHED for the *dwMsgType* parameter and a pointer to [**CMSG\_HASHED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) for the *pvMsgEncodeInfo* parameter.</span></span> <span data-ttu-id="3598e-123">由於這個呼叫，您會取得已開啟之訊息的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3598e-123">As a result of this call, you get a handle to the opened message.</span></span>
6.  <span data-ttu-id="3598e-124">呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)，傳入在步驟5中抓取的控制碼，以及要進行雜湊處理和編碼的資料指標。</span><span class="sxs-lookup"><span data-stu-id="3598e-124">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), passing in the handle retrieved in step 5 and a pointer to the data that is to be hashed and encoded.</span></span> <span data-ttu-id="3598e-125">您可以視需要多次呼叫這個函式，以完成編碼程式。</span><span class="sxs-lookup"><span data-stu-id="3598e-125">This function can be called as many times as necessary to complete the encoding process.</span></span>
7.  <span data-ttu-id="3598e-126">呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入在步驟5中抓取的控制碼和適當的參數類型，以存取所需的編碼資料。</span><span class="sxs-lookup"><span data-stu-id="3598e-126">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 5 and the appropriate parameter types to access the desired, encoded data.</span></span> <span data-ttu-id="3598e-127">例如，傳入 CMSG \_ CONTENT \_ PARAM 以取得整個 [*PKCS \# 7*](../secgloss/p-gly.md) 訊息的指標。</span><span class="sxs-lookup"><span data-stu-id="3598e-127">For example, pass in CMSG\_CONTENT\_PARAM to get a pointer to the entire [*PKCS \#7*](../secgloss/p-gly.md) message.</span></span>

    <span data-ttu-id="3598e-128">如果此編碼的結果是做為另一個編碼訊息的 [*內部資料*](../secgloss/i-gly.md) ，例如封包訊息，則 \_ \_ 必須傳遞 CMSG 的 BARE 內容 \_ 參數。</span><span class="sxs-lookup"><span data-stu-id="3598e-128">If the result of this encoding is to be used as the [*inner data*](../secgloss/i-gly.md) for another encoded message, such as an enveloped message, CMSG\_BARE\_CONTENT\_PARAM must be passed.</span></span> <span data-ttu-id="3598e-129">如需顯示此情況的範例，請參閱 [編碼封包訊息的替代程式碼](alternate-code-for-encoding-an-enveloped-message.md)。</span><span class="sxs-lookup"><span data-stu-id="3598e-129">For an example showing this, see [Alternate Code for Encoding an Enveloped Message](alternate-code-for-encoding-an-enveloped-message.md).</span></span>

8.  <span data-ttu-id="3598e-130">藉由呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)來關閉訊息。</span><span class="sxs-lookup"><span data-stu-id="3598e-130">Close the message by calling [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).</span></span>

<span data-ttu-id="3598e-131">此程式的結果是編碼的訊息，其中包含原始資料、雜湊演算法和該資料的 [*雜湊*](../secgloss/h-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="3598e-131">The result of this procedure is an encoded message that contains the original data, the hashing algorithms, and the [*hash*](../secgloss/h-gly.md) of that data.</span></span> <span data-ttu-id="3598e-132">在步驟7中，會取得編碼訊息 [*BLOB*](../secgloss/b-gly.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="3598e-132">A pointer to the encoded message [*BLOB*](../secgloss/b-gly.md) is obtained in step 7.</span></span>

<span data-ttu-id="3598e-133">下列兩個程式會解碼並確認雜湊資料。</span><span class="sxs-lookup"><span data-stu-id="3598e-133">The following two procedures decode and then verify hashed data.</span></span>

<span data-ttu-id="3598e-134">**解碼雜湊資料**</span><span class="sxs-lookup"><span data-stu-id="3598e-134">**To decode hashed data**</span></span>

1.  <span data-ttu-id="3598e-135">取得編碼 BLOB 的指標。</span><span class="sxs-lookup"><span data-stu-id="3598e-135">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="3598e-136">呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)，傳遞必要的引數。</span><span class="sxs-lookup"><span data-stu-id="3598e-136">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="3598e-137">呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 一次，並傳入步驟2中抓取的控制碼，以及要解碼之資料的指標。</span><span class="sxs-lookup"><span data-stu-id="3598e-137">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="3598e-138">這會根據訊息類型，對訊息採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="3598e-138">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="3598e-139">呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入步驟2中抓取的控制碼，以及適當的參數類型來存取所需的解碼資料。</span><span class="sxs-lookup"><span data-stu-id="3598e-139">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2, and the appropriate parameter types to access the desired, decoded data.</span></span> <span data-ttu-id="3598e-140">例如，傳入 CMSG \_ content \_ PARAM 以取得已解碼內容的指標。</span><span class="sxs-lookup"><span data-stu-id="3598e-140">For example, pass in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content.</span></span>

<span data-ttu-id="3598e-141">**確認雜湊**</span><span class="sxs-lookup"><span data-stu-id="3598e-141">**To verify the hash**</span></span>

1.  <span data-ttu-id="3598e-142">呼叫 [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)，傳入 CMSG \_ CTRL \_ 確認 \_ 雜湊來驗證雜湊。</span><span class="sxs-lookup"><span data-stu-id="3598e-142">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_VERIFY\_HASH to verify the hashes.</span></span>
2.  <span data-ttu-id="3598e-143">呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) 以關閉訊息。</span><span class="sxs-lookup"><span data-stu-id="3598e-143">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="3598e-144">如需範例程式，請參閱 [範例 C 程式：編碼和解碼雜湊的訊息](example-c-program-encoding-and-decoding-a-hashed-message.md)。</span><span class="sxs-lookup"><span data-stu-id="3598e-144">For an example program, see [Example C Program: Encoding and Decoding a Hashed Message](example-c-program-encoding-and-decoding-a-hashed-message.md).</span></span>

 

 
