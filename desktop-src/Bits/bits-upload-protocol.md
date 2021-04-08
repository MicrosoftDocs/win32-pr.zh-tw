---
title: BITS 上傳通訊協定
description: 本節說明 BITS 上傳和上傳-回復工作類型的網路通訊協定。
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642426decd0bc37390fa9fdd9b1ad2be11a0aa84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671628"
---
# <a name="bits-upload-protocol"></a><span data-ttu-id="50ee4-103">BITS 上傳通訊協定</span><span class="sxs-lookup"><span data-stu-id="50ee4-103">BITS Upload Protocol</span></span>

<span data-ttu-id="50ee4-104">本節說明 BITS 上傳和上傳-回復工作類型的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="50ee4-104">This section describes the network protocol for BITS upload and upload-reply job types.</span></span> <span data-ttu-id="50ee4-105">BITS 上傳通訊協定會分層在 HTTP 1.1 之上，並使用許多現有的 HTTP 標頭，並定義新的標頭。</span><span class="sxs-lookup"><span data-stu-id="50ee4-105">The BITS upload protocol is layered on top of HTTP 1.1 and uses many of the existing HTTP headers and defines new headers.</span></span> <span data-ttu-id="50ee4-106">BITS 上傳通訊協定支援每個會話單一上傳檔案。</span><span class="sxs-lookup"><span data-stu-id="50ee4-106">The BITS upload protocol supports a single upload file per session.</span></span>

<span data-ttu-id="50ee4-107">BITS 會使用封包來描述用戶端要求和伺服器回應。</span><span class="sxs-lookup"><span data-stu-id="50ee4-107">BITS uses packets to describe client requests and server responses.</span></span> <span data-ttu-id="50ee4-108">BITS 封包類型標頭會指定正在傳送的封包類型。</span><span class="sxs-lookup"><span data-stu-id="50ee4-108">The BITS-Packet-Type header specifies the type of packet being sent.</span></span> <span data-ttu-id="50ee4-109">每個封包都包含特定標頭。</span><span class="sxs-lookup"><span data-stu-id="50ee4-109">Each packet contains specific headers.</span></span> <span data-ttu-id="50ee4-110">BITS 會使用 BITS \_ POST 動詞命令來識別 bits 上傳封包。</span><span class="sxs-lookup"><span data-stu-id="50ee4-110">BITS uses the BITS\_POST verb to identify BITS upload packets.</span></span> <span data-ttu-id="50ee4-111">回應封包一律會使用代表認可的 Ack 封包類型。</span><span class="sxs-lookup"><span data-stu-id="50ee4-111">Response packets always use the Ack packet type which stands for acknowledge.</span></span> <span data-ttu-id="50ee4-112">Ack 封包會在前一個要求的內容中傳送;一次只能有一個未處理的要求。</span><span class="sxs-lookup"><span data-stu-id="50ee4-112">The Ack packet is sent in the context of the previous request; there can be only one outstanding request at one time.</span></span>

<span data-ttu-id="50ee4-113">針對上傳-回復作業，BITS 會使用此通訊協定來上傳檔案，但不會使用此通訊協定將回復傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="50ee4-113">For upload-reply jobs, BITS uses this protocol to upload the file but does not use this protocol to send the reply to the client.</span></span> <span data-ttu-id="50ee4-114">相反地，BITS 伺服器會將回復檔案的位置傳送至用戶端，而用戶端會建立 BITS 下載作業來下載回復檔案。</span><span class="sxs-lookup"><span data-stu-id="50ee4-114">Instead, the BITS server sends the location of the reply file to the client and the client creates a BITS download job to download the reply file.</span></span>

<span data-ttu-id="50ee4-115">使用上傳通訊協定，以您自己的執行取代 BITS 用戶端或伺服器軟體。</span><span class="sxs-lookup"><span data-stu-id="50ee4-115">Use the upload protocol to replace the BITS client or server software with your own implementation.</span></span> <span data-ttu-id="50ee4-116">如需 BITS 用戶端所傳送的要求封包清單，請參閱 [Bits 要求封包](bits-request-packets.md)。</span><span class="sxs-lookup"><span data-stu-id="50ee4-116">For a list of request packets sent by the BITS client, see [BITS Request Packets](bits-request-packets.md).</span></span> <span data-ttu-id="50ee4-117">如需 BITS 伺服器所傳送的回應封包清單，請參閱 [Bits 回應封包](bits-response-packets.md)。</span><span class="sxs-lookup"><span data-stu-id="50ee4-117">For a list of response packets sent by the BITS server, see [BITS Response Packets](bits-response-packets.md).</span></span>

<span data-ttu-id="50ee4-118">用戶端會決定它如何回應 BITS 伺服器的錯誤或未預期的封包。</span><span class="sxs-lookup"><span data-stu-id="50ee4-118">The client determines how it responds to errors or unexpected packets from the BITS server.</span></span> <span data-ttu-id="50ee4-119">如果伺服器收到未預期的封包，伺服器應該傳送具有 400 (錯誤要求) 傳回碼的 Ack 封包。</span><span class="sxs-lookup"><span data-stu-id="50ee4-119">If the server receives a packet that it does not expect, the server should send an Ack packet with a 400 (Bad Request) return code.</span></span>

 

 




