---
title: Cancel-Session
description: 使用 Cancel-Session 封包來終止與 BITS 伺服器的上傳會話。
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Session 位
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106967861"
---
# <a name="cancel-session"></a><span data-ttu-id="5d949-104">Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="5d949-104">Cancel-Session</span></span>

<span data-ttu-id="5d949-105">使用 **取消會話** 封包來終止與 BITS 伺服器的上傳會話。</span><span class="sxs-lookup"><span data-stu-id="5d949-105">Use the **Cancel-Session** packet to terminate the upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="5d949-106">標題</span><span class="sxs-lookup"><span data-stu-id="5d949-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="5d949-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST</span><span class="sxs-lookup"><span data-stu-id="5d949-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="5d949-108">識別此封包到 BITS 伺服器的位特定動詞。</span><span class="sxs-lookup"><span data-stu-id="5d949-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="5d949-109">將遠端 URL 取代為絕對或相對 URI。</span><span class="sxs-lookup"><span data-stu-id="5d949-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="5d949-110">通常，將遠端 URL 取代為作業的遠端檔案名。</span><span class="sxs-lookup"><span data-stu-id="5d949-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="5d949-111">如需網路負載平衡的考慮，請參閱 [**建立會話**](create-session.md) 封包中的 BITS 主機識別碼標頭。</span><span class="sxs-lookup"><span data-stu-id="5d949-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="5d949-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型</span><span class="sxs-lookup"><span data-stu-id="5d949-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="5d949-113">將此要求封包識別為 Cancel-Session 封包。</span><span class="sxs-lookup"><span data-stu-id="5d949-113">Identifies this request packet as a Cancel-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="5d949-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>位-會話識別碼</span><span class="sxs-lookup"><span data-stu-id="5d949-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="5d949-115">識別伺服器會話的字串 GUID。</span><span class="sxs-lookup"><span data-stu-id="5d949-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="5d949-116">將 {guid} 取代為伺服器在 [**建立會話**](ack-for-create-session.md) 回應封包的 Ack 中傳回的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d949-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d949-117">備註</span><span class="sxs-lookup"><span data-stu-id="5d949-117">Remarks</span></span>

<span data-ttu-id="5d949-118">此封包會取消上傳工作（如果在傳送最後一個片段之前傳送）。</span><span class="sxs-lookup"><span data-stu-id="5d949-118">This packet cancels an upload job if it is sent before the last fragment is sent.</span></span> <span data-ttu-id="5d949-119">Cancel-Session 對於已傳送最後一個片段的檔案沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="5d949-119">Cancel-Session has no effect on a file whose last fragment has already been sent.</span></span> <span data-ttu-id="5d949-120">當 BITS 伺服器收到最後一個片段時，它會將檔案寫入其最終目的地，而在上傳-回復的情況下，會將檔案張貼至伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="5d949-120">When the BITS server receives the last fragment, it writes the file to its final destination and, in the case of an upload-reply, posts the file to the server application.</span></span> <span data-ttu-id="5d949-121">在上傳-回復案例中，Cancel-Session 封包會取消上傳-回復作業的回復部分。</span><span class="sxs-lookup"><span data-stu-id="5d949-121">In the upload-reply case, the Cancel-Session packet cancels the reply portion of an upload-reply job.</span></span>

<span data-ttu-id="5d949-122">BITS 伺服器會釋放所有資源，並在接收到此封包時刪除所有暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="5d949-122">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="5d949-123">BITS 用戶端會在使用者取消作業時傳送此封包。</span><span class="sxs-lookup"><span data-stu-id="5d949-123">The BITS client sends this packet when the user cancels the job.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d949-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d949-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d949-125">**Create-Session 的 Ack**</span><span class="sxs-lookup"><span data-stu-id="5d949-125">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="5d949-126">**關閉會話**</span><span class="sxs-lookup"><span data-stu-id="5d949-126">**Close-Session**</span></span>](close-session.md)
</dt> </dl>

 

 




