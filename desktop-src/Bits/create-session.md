---
title: Create-Session
description: 使用 Create-Session 封包向 BITS 伺服器要求上傳會話。
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session 位
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425ad3bd36305f94547cf2cd8b13c1a420491499
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462516"
---
# <a name="create-session"></a><span data-ttu-id="3ef8e-104">Create-Session</span><span class="sxs-lookup"><span data-stu-id="3ef8e-104">Create-Session</span></span>

<span data-ttu-id="3ef8e-105">使用 **Create-Session** 封包要求 BITS 伺服器的上傳會話。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-105">Use the **Create-Session** packet to request an upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a><span data-ttu-id="3ef8e-106">標題</span><span class="sxs-lookup"><span data-stu-id="3ef8e-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="3ef8e-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST</span><span class="sxs-lookup"><span data-stu-id="3ef8e-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="3ef8e-108">識別此封包到 BITS 伺服器的位特定動詞。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="3ef8e-109">將遠端 URL 取代為絕對或相對 URI。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="3ef8e-110">通常，將遠端 URL 取代為作業的遠端檔案名。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="3ef8e-111">如需網路負載平衡的考慮，請參閱 BITS-主機-識別碼標頭。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-111">For network load balancing considerations, see the BITS-Host-Id header.</span></span>

</dd> <dt>

<span data-ttu-id="3ef8e-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型</span><span class="sxs-lookup"><span data-stu-id="3ef8e-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="3ef8e-113">將此要求封包識別為 Create-Session 封包。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-113">Identifies this request packet as a Create-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="3ef8e-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-支援的通訊協定</span><span class="sxs-lookup"><span data-stu-id="3ef8e-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-Supported-Protocols</span></span>
</dt> <dd>

<span data-ttu-id="3ef8e-115">用戶端支援的通訊協定清單（以空格分隔）。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-115">Space-delimited list of the protocols that the client supports.</span></span> <span data-ttu-id="3ef8e-116">使用字串 Guid 來識別通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-116">Use string GUIDs to identify the protocols.</span></span> <span data-ttu-id="3ef8e-117">依喜好設定順序指定清單，從最高到最低。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-117">Specify the list in order of preference from most to least preferred.</span></span> <span data-ttu-id="3ef8e-118">下表列出 BITS 用戶端支援的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-118">The following table lists the protocol that the BITS client supports.</span></span> <span data-ttu-id="3ef8e-119">取代 {guid1} .。。具有清單中一或多個字串 Guid 的 {guidN}。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-119">Replace {guid1} ... {guidN} with one or more string GUIDs from the list.</span></span>



| <span data-ttu-id="3ef8e-120">通訊協定</span><span class="sxs-lookup"><span data-stu-id="3ef8e-120">Protocol</span></span>                                          | <span data-ttu-id="3ef8e-121">描述</span><span class="sxs-lookup"><span data-stu-id="3ef8e-121">Description</span></span>                         |
|---------------------------------------------------|-------------------------------------|
| <span data-ttu-id="3ef8e-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span><span class="sxs-lookup"><span data-stu-id="3ef8e-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span></span><br/> | <span data-ttu-id="3ef8e-123">BITS 1.5 上傳通訊協定</span><span class="sxs-lookup"><span data-stu-id="3ef8e-123">BITS 1.5 Upload Protocol</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ef8e-124">備註</span><span class="sxs-lookup"><span data-stu-id="3ef8e-124">Remarks</span></span>

<span data-ttu-id="3ef8e-125">傳送 Create-Session 封包之前，您應該先傳送 [**Ping**](ping.md) 封包來建立 HTTP 連線。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-125">You should send a [**Ping**](ping.md) packet to establish an HTTP connection before sending the Create-Session packet.</span></span> <span data-ttu-id="3ef8e-126">Create-Session 封包也可以建立連接;不過，Create-Session 封包的效率較低。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-126">The Create-Session packet can also establish the connection; however, the Create-Session packet is less efficient.</span></span>

<span data-ttu-id="3ef8e-127">伺服器會從用戶端在 BITS 支援的通訊協定標頭中提供的清單中選取想要使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-127">The server selects the protocol it wants to use from the list the client provides in the BITS-Supported-Protocols header.</span></span> <span data-ttu-id="3ef8e-128">伺服器會在 [**Create-Session**](ack-for-create-session.md) response 封包的 Ack BITS-Protocol 標頭中傳回選取的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-128">The server returns the selected protocol in the BITS-Protocol header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

<span data-ttu-id="3ef8e-129">用戶端預期伺服器會傳回 [**Create Session**](ack-for-create-session.md) response 封包的 Ack。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-129">The client expects the server to return an [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="3ef8e-130">如果伺服器可以建立會話，用戶端會使用 [**片段**](fragment.md) 要求封包，將檔案範圍傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="3ef8e-130">If the server was able to establish a session, the client uses the [**Fragment**](fragment.md) request packet to send ranges of the file to the server.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ef8e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ef8e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef8e-132">**Create-Session 的 Ack**</span><span class="sxs-lookup"><span data-stu-id="3ef8e-132">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="3ef8e-133">**片段**</span><span class="sxs-lookup"><span data-stu-id="3ef8e-133">**Fragment**</span></span>](fragment.md)
</dt> <dt>

[<span data-ttu-id="3ef8e-134">**坪**</span><span class="sxs-lookup"><span data-stu-id="3ef8e-134">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 





