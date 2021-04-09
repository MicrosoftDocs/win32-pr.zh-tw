---
title: BITS 要求封包
description: BITS 要求封包
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931963"
---
# <a name="bits-request-packets"></a><span data-ttu-id="d0f22-103">BITS 要求封包</span><span class="sxs-lookup"><span data-stu-id="d0f22-103">BITS Request Packets</span></span>

<span data-ttu-id="d0f22-104">要求封包會描述用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="d0f22-104">Request packets describe client requests.</span></span> <span data-ttu-id="d0f22-105">在任何指定的時間，都只能有一個未處理的要求;傳送另一個要求之前，您必須先從伺服器接收目前要求的 [Ack](bits-response-packets.md) 。</span><span class="sxs-lookup"><span data-stu-id="d0f22-105">There can be only one outstanding request at any given time; you must receive an [Ack](bits-response-packets.md) for the current request from the server before sending another request.</span></span>

<span data-ttu-id="d0f22-106">下表列出針對上傳和上傳-回復作業傳送至 BITS 伺服器的要求封包。</span><span class="sxs-lookup"><span data-stu-id="d0f22-106">The following table lists the request packets sent to the BITS server for upload and upload-reply jobs.</span></span> <span data-ttu-id="d0f22-107">資料表會列出傳送至伺服器的一般順序中的封包。</span><span class="sxs-lookup"><span data-stu-id="d0f22-107">The table lists the packets in the typical sequence they are sent to the server.</span></span>



| <span data-ttu-id="d0f22-108">要求封包</span><span class="sxs-lookup"><span data-stu-id="d0f22-108">Request packet</span></span>                       | <span data-ttu-id="d0f22-109">目的</span><span class="sxs-lookup"><span data-stu-id="d0f22-109">Purpose</span></span>                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0f22-110">坪</span><span class="sxs-lookup"><span data-stu-id="d0f22-110">Ping</span></span>](ping.md)                     | <span data-ttu-id="d0f22-111">建立連接並與伺服器協商安全性。</span><span class="sxs-lookup"><span data-stu-id="d0f22-111">Establishes a connection and negotiates security with the server.</span></span>                                                                                              |
| [<span data-ttu-id="d0f22-112">建立-會話</span><span class="sxs-lookup"><span data-stu-id="d0f22-112">Create-Session</span></span>](create-session.md) | <span data-ttu-id="d0f22-113">要求 BITS 伺服器的上傳會話。</span><span class="sxs-lookup"><span data-stu-id="d0f22-113">Requests an upload session with the BITS server.</span></span>                                                                                                               |
| [<span data-ttu-id="d0f22-114">片段</span><span class="sxs-lookup"><span data-stu-id="d0f22-114">Fragment</span></span>](fragment.md)             | <span data-ttu-id="d0f22-115">將檔案的片段傳送至 BITS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="d0f22-115">Sends a fragment of the file to the BITS server.</span></span> <span data-ttu-id="d0f22-116">傳送的片段要求數目取決於您所選擇的片段大小和上傳檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="d0f22-116">The number of fragment requests sent depends on the fragment size you choose and the size of the upload file.</span></span> |
| [<span data-ttu-id="d0f22-117">關閉會話</span><span class="sxs-lookup"><span data-stu-id="d0f22-117">Close-Session</span></span>](close-session.md)   | <span data-ttu-id="d0f22-118">結束與 BITS 伺服器的檔案上傳會話。</span><span class="sxs-lookup"><span data-stu-id="d0f22-118">Ends the file upload session with the BITS server.</span></span>                                                                                                             |
| [<span data-ttu-id="d0f22-119">取消-會話</span><span class="sxs-lookup"><span data-stu-id="d0f22-119">Cancel-Session</span></span>](cancel-session.md) | <span data-ttu-id="d0f22-120">結束與 BITS 伺服器的檔案上傳會話。</span><span class="sxs-lookup"><span data-stu-id="d0f22-120">Ends the file upload session with the BITS server.</span></span> <span data-ttu-id="d0f22-121">一般而言，如果使用者取消作業，您會傳送 Cancel-Session 封包。</span><span class="sxs-lookup"><span data-stu-id="d0f22-121">Typically, you send the Cancel-Session packet if the user canceled the job.</span></span>                                 |



 

<span data-ttu-id="d0f22-122">Ping 封包是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="d0f22-122">The Ping packet is optional.</span></span> <span data-ttu-id="d0f22-123">您可以使用 Create-Session 封包來建立連線並協商安全性，而不是傳送 Ping 封包。</span><span class="sxs-lookup"><span data-stu-id="d0f22-123">Instead of sending a Ping packet, you can use the Create-Session packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="d0f22-124">不過，針對此目的使用 Ping 封包較有效率。</span><span class="sxs-lookup"><span data-stu-id="d0f22-124">However, it is more efficient to use the Ping packet for this purpose.</span></span>

 

 




