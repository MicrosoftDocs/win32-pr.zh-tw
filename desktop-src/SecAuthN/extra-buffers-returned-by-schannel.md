---
description: Schannel 針對這些函式的輸入緩衝區中包含的不完整或超過的資訊，有一組定義完善的行為。
ms.assetid: 5fad1e76-6520-4ff7-b2b0-2cc2061062a1
title: Schannel 傳回的額外緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c9ce7a468b1b04389ad19f91785b64fb50e74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984681"
---
# <a name="extra-buffers-returned-by-schannel"></a><span data-ttu-id="1b33d-103">Schannel 傳回的額外緩衝區</span><span class="sxs-lookup"><span data-stu-id="1b33d-103">Extra Buffers Returned by Schannel</span></span>

<span data-ttu-id="1b33d-104">建立 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 時，必須在用戶端與伺服器之間傳送資訊，而且之後，因為安全訊息是使用 Schannel 提供的加密和解密功能來交換的。</span><span class="sxs-lookup"><span data-stu-id="1b33d-104">Information must be sent between the client and server while a [*security context*](/windows/desktop/SecGloss/s-gly) is being established and afterward because secure messages are exchanged by using the encryption and decryption features provided by Schannel.</span></span> <span data-ttu-id="1b33d-105">下列函式可用來完成這些工作：</span><span class="sxs-lookup"><span data-stu-id="1b33d-105">The following functions are used to accomplish these tasks:</span></span>

-   [<span data-ttu-id="1b33d-106">**AcceptSecurityCoNtext (一般)**</span><span class="sxs-lookup"><span data-stu-id="1b33d-106">**AcceptSecurityContext (General)**</span></span>](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
-   [<span data-ttu-id="1b33d-107">**InitializeSecurityCoNtext (一般)**</span><span class="sxs-lookup"><span data-stu-id="1b33d-107">**InitializeSecurityContext (General)**</span></span>](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
-   [<span data-ttu-id="1b33d-108">**DecryptMessage (一般)**</span><span class="sxs-lookup"><span data-stu-id="1b33d-108">**DecryptMessage (General)**</span></span>](/windows/win32/api/sspi/nf-sspi-decryptmessage)

<span data-ttu-id="1b33d-109">Schannel 針對這些函式的輸入緩衝區中包含的不完整或超過的資訊，有一組定義完善的行為。</span><span class="sxs-lookup"><span data-stu-id="1b33d-109">Schannel has a well-defined set of behaviors for incomplete or excess information included in the input buffers to these functions.</span></span> <span data-ttu-id="1b33d-110">用戶端與伺服器之間的資訊會以下列方式交換：</span><span class="sxs-lookup"><span data-stu-id="1b33d-110">Information is exchanged between the client and server in the following manner:</span></span>

1.  <span data-ttu-id="1b33d-111">本機合作物件會藉由呼叫 SSPI 函式並傳入資訊，與 Schannel 互動。</span><span class="sxs-lookup"><span data-stu-id="1b33d-111">The local party interacts with Schannel by calling an SSPI function and passing in information.</span></span> <span data-ttu-id="1b33d-112">一般而言，資訊是從遠端方收到的。</span><span class="sxs-lookup"><span data-stu-id="1b33d-112">Typically, the information was received from the remote party.</span></span>
2.  <span data-ttu-id="1b33d-113">函數會傳回包含資訊的狀態碼和輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1b33d-113">The function returns a status code and output buffers containing information.</span></span>
3.  <span data-ttu-id="1b33d-114">根據狀態碼，輸出緩衝區會透過某些通訊機制傳送給遠端方。</span><span class="sxs-lookup"><span data-stu-id="1b33d-114">Depending on the status code, the output buffers are sent to the remote party by means of some communication mechanism.</span></span>
4.  <span data-ttu-id="1b33d-115">遠端方會讀取由本機合作物件傳送的資訊。</span><span class="sxs-lookup"><span data-stu-id="1b33d-115">The remote party reads information sent by the local party.</span></span>
5.  <span data-ttu-id="1b33d-116">迴圈會重複，並將本機和遠端物件交換。</span><span class="sxs-lookup"><span data-stu-id="1b33d-116">The loop repeats, with the local and remote parties interchanged.</span></span> <span data-ttu-id="1b33d-117"> (遠端方呼叫 SSPI 函式，並傳入上一個步驟中讀取的資訊。 ) </span><span class="sxs-lookup"><span data-stu-id="1b33d-117">(The remote party calls an SSPI function and passes in the information read in the previous step.)</span></span>

<span data-ttu-id="1b33d-118">當 SSPI 函式的輸入緩衝區剛好包含所需的資訊時，一切都會如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="1b33d-118">Everything works as expected when the input buffer to the SSPI function contains exactly the information needed.</span></span> <span data-ttu-id="1b33d-119">不過，因為某些通訊協定的資料流程導向本質，所以可能不會發生這種情況;從遠端物件接收的資訊區塊可能包含比所需或更多的資料，而不是在單一函式呼叫中可由 Schannel 處理的資料。</span><span class="sxs-lookup"><span data-stu-id="1b33d-119">However, due to the stream-oriented nature of some communications protocols this may not be the case; a block of information received from a remote party may contain less data than is required or more data than can be processed by Schannel in a single function call.</span></span>

<span data-ttu-id="1b33d-120">如果輸入緩衝區包含太少的資訊，則函式會傳回 SEC \_ E \_ 未完成的 \_ 訊息。</span><span class="sxs-lookup"><span data-stu-id="1b33d-120">If the input buffer contains too little information, the functions return SEC\_E\_INCOMPLETE\_MESSAGE.</span></span> <span data-ttu-id="1b33d-121">呼叫端必須從遠端方取得額外的資料，然後再次呼叫函式。</span><span class="sxs-lookup"><span data-stu-id="1b33d-121">The caller must obtain additional data from the remote party and call the function again.</span></span>

<span data-ttu-id="1b33d-122">當輸入緩衝區包含太多資訊時，Schannel 不會將此視為錯誤。</span><span class="sxs-lookup"><span data-stu-id="1b33d-122">When the input buffers contains too much information, Schannel does not treat this as an error.</span></span> <span data-ttu-id="1b33d-123">函式會盡可能處理最多的輸入，並傳回該處理活動的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="1b33d-123">The function processes as much of the input as it can, and returns the status code for that processing activity.</span></span> <span data-ttu-id="1b33d-124">此外，Schannel 會傳回之 SECBUFFER 額外類型的輸出緩衝區，以指出輸入緩衝區中是否有未處理的資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1b33d-124">In addition, Schannel indicates the presence of unprocessed information in the input buffers by returning an output buffer of type SECBUFFER\_EXTRA.</span></span> <span data-ttu-id="1b33d-125">測試此類型緩衝區的輸出緩衝區是偵測這種情況的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="1b33d-125">Testing the output buffers for this type of buffer is the only way to detect this situation.</span></span> <span data-ttu-id="1b33d-126">額外緩衝區結構的 **cbBuffer** 欄位指出未處理多少位元組的輸入。</span><span class="sxs-lookup"><span data-stu-id="1b33d-126">The **cbBuffer** field of the extra buffer structure indicates how many bytes of input were not processed.</span></span>

> [!Note]  
> <span data-ttu-id="1b33d-127">額外緩衝區的 **pvBuffer** 欄位不包含一份多餘的資料。</span><span class="sxs-lookup"><span data-stu-id="1b33d-127">The **pvBuffer** field of the extra buffer does not contain a copy of the excess data.</span></span>

 

<span data-ttu-id="1b33d-128">如果您收到來自 SSPI 函式的額外緩衝區，您必須從輸入緩衝區移除已處理的資訊，然後再次呼叫該函式。</span><span class="sxs-lookup"><span data-stu-id="1b33d-128">If you receive an extra buffer from a SSPI function, you must remove the already processed information from the input buffer and call the function again.</span></span> <span data-ttu-id="1b33d-129">Schannel 通常會傳回額外的緩衝區，而不會傳回輸出緩衝區中的任何其他緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1b33d-129">Schannel can, and often does, return only the extra buffer and nothing else in the output buffers.</span></span>

 

 
