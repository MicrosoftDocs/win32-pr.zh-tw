---
title: Close-Session
description: 使用 Close-Session 封包來告訴 BITS 伺服器檔案上傳已完成，並結束會話。
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Session 位
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe791ba4706689fd23dea8886f5b8f54f135841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841012"
---
# <a name="close-session"></a><span data-ttu-id="99303-104">Close-Session</span><span class="sxs-lookup"><span data-stu-id="99303-104">Close-Session</span></span>

<span data-ttu-id="99303-105">使用「 **關閉會話** 」封包，告訴 BITS 伺服器檔案上傳已完成，並結束會話。</span><span class="sxs-lookup"><span data-stu-id="99303-105">Use the **Close-Session** packet to tell the BITS server that file upload is complete and to end the session.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="99303-106">標題</span><span class="sxs-lookup"><span data-stu-id="99303-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="99303-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST</span><span class="sxs-lookup"><span data-stu-id="99303-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="99303-108">識別此封包到 BITS 伺服器的位特定動詞。</span><span class="sxs-lookup"><span data-stu-id="99303-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="99303-109">將遠端 URL 取代為絕對或相對 URI。</span><span class="sxs-lookup"><span data-stu-id="99303-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="99303-110">通常，將遠端 URL 取代為作業的遠端檔案名。</span><span class="sxs-lookup"><span data-stu-id="99303-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="99303-111">如需網路負載平衡的考慮，請參閱 [**建立會話**](create-session.md) 封包中的 BITS 主機識別碼標頭。</span><span class="sxs-lookup"><span data-stu-id="99303-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="99303-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型</span><span class="sxs-lookup"><span data-stu-id="99303-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="99303-113">將此要求封包識別為 Close-Session 封包。</span><span class="sxs-lookup"><span data-stu-id="99303-113">Identifies this request packet as a Close-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="99303-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>位-會話識別碼</span><span class="sxs-lookup"><span data-stu-id="99303-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="99303-115">識別伺服器會話的字串 GUID。</span><span class="sxs-lookup"><span data-stu-id="99303-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="99303-116">將 {guid} 取代為伺服器在 [**建立會話**](ack-for-create-session.md) 回應封包的 Ack 中傳回的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="99303-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99303-117">備註</span><span class="sxs-lookup"><span data-stu-id="99303-117">Remarks</span></span>

<span data-ttu-id="99303-118">BITS 伺服器會釋放所有資源，並在接收到此封包時刪除所有暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="99303-118">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="99303-119">針對上傳-回復作業，您必須先下載回復，再傳送 **關閉會話**。</span><span class="sxs-lookup"><span data-stu-id="99303-119">For upload-reply jobs, you must download the reply before sending **Close-Session**.</span></span> <span data-ttu-id="99303-120">否則，回復會遺失。</span><span class="sxs-lookup"><span data-stu-id="99303-120">Otherwise, the reply is lost.</span></span>

<span data-ttu-id="99303-121">如果您在上傳所有片段之前傳送此封包，則會刪除上傳檔案;您無法上傳部分檔案。</span><span class="sxs-lookup"><span data-stu-id="99303-121">If you send this packet before uploading all fragments, the upload file is deleted; you cannot upload a partial file.</span></span>

## <a name="see-also"></a><span data-ttu-id="99303-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99303-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99303-123">**確認是否已關閉會話**</span><span class="sxs-lookup"><span data-stu-id="99303-123">**Ack for Close-Session**</span></span>](ack-for-close-session.md)
</dt> <dt>

[<span data-ttu-id="99303-124">**取消-會話**</span><span class="sxs-lookup"><span data-stu-id="99303-124">**Cancel-Session**</span></span>](cancel-session.md)
</dt> <dt>

[<span data-ttu-id="99303-125">**建立-會話**</span><span class="sxs-lookup"><span data-stu-id="99303-125">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




