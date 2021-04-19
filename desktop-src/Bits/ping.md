---
title: Ping
description: 使用 Ping 封包來建立連接，並與伺服器協商安全性。
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- Ping 位
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "106967871"
---
# <a name="ping"></a><span data-ttu-id="3a046-104">Ping</span><span class="sxs-lookup"><span data-stu-id="3a046-104">Ping</span></span>

<span data-ttu-id="3a046-105">使用 **Ping** 封包來建立連接，並與伺服器協商安全性。</span><span class="sxs-lookup"><span data-stu-id="3a046-105">Use the **Ping** packet to establish a connection and negotiate security with the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a><span data-ttu-id="3a046-106">標題</span><span class="sxs-lookup"><span data-stu-id="3a046-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="3a046-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST</span><span class="sxs-lookup"><span data-stu-id="3a046-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="3a046-108">識別此封包到 BITS 伺服器的位特定動詞。</span><span class="sxs-lookup"><span data-stu-id="3a046-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="3a046-109">將遠端 URL 取代為絕對或相對 URI。</span><span class="sxs-lookup"><span data-stu-id="3a046-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="3a046-110">通常，將遠端 URL 取代為作業的遠端檔案名。</span><span class="sxs-lookup"><span data-stu-id="3a046-110">Typically, replace remote-URL with the remote file name of the job.</span></span>

</dd> <dt>

<span data-ttu-id="3a046-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型</span><span class="sxs-lookup"><span data-stu-id="3a046-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="3a046-112">將此要求封包識別為 Ping 封包。</span><span class="sxs-lookup"><span data-stu-id="3a046-112">Identifies this request packet as a Ping packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a046-113">備註</span><span class="sxs-lookup"><span data-stu-id="3a046-113">Remarks</span></span>

<span data-ttu-id="3a046-114">**Ping** 封包是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="3a046-114">The **Ping** packet is optional.</span></span> <span data-ttu-id="3a046-115">您可以使用建立 [**會話**](create-session.md)封包來建立連線和協商安全性，而不是傳送 **Ping** 封包。</span><span class="sxs-lookup"><span data-stu-id="3a046-115">Instead of sending a **Ping** packet, you can use the [**Create-Session**](create-session.md) packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="3a046-116">不過，針對此目的使用 **Ping** 封包較有效率。</span><span class="sxs-lookup"><span data-stu-id="3a046-116">However, it is more efficient to use the **Ping** packet for this purpose.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a046-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a046-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a046-118">**Ping 的 Ack**</span><span class="sxs-lookup"><span data-stu-id="3a046-118">**Ack for Ping**</span></span>](ack-for-ping.md)
</dt> <dt>

[<span data-ttu-id="3a046-119">**建立-會話**</span><span class="sxs-lookup"><span data-stu-id="3a046-119">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




