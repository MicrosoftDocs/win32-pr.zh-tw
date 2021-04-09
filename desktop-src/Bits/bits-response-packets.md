---
title: BITS 回應封包
description: BITS 回應封包
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839368"
---
# <a name="bits-response-packets"></a><span data-ttu-id="41efd-103">BITS 回應封包</span><span class="sxs-lookup"><span data-stu-id="41efd-103">BITS Response Packets</span></span>

<span data-ttu-id="41efd-104">下表列出針對上傳和上傳-回復作業傳送至 BITS 用戶端的回應封包。</span><span class="sxs-lookup"><span data-stu-id="41efd-104">The following table lists the response packets sent to the BITS client for upload and upload-reply jobs.</span></span> <span data-ttu-id="41efd-105">資料表會列出傳送給用戶端的一般順序中的封包。</span><span class="sxs-lookup"><span data-stu-id="41efd-105">The table lists the packets in the typical sequence they are sent to the client.</span></span>



| <span data-ttu-id="41efd-106">回應封包</span><span class="sxs-lookup"><span data-stu-id="41efd-106">Response packet</span></span>                                      | <span data-ttu-id="41efd-107">目的</span><span class="sxs-lookup"><span data-stu-id="41efd-107">Purpose</span></span>                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41efd-108">Ping 的 Ack</span><span class="sxs-lookup"><span data-stu-id="41efd-108">Ack for Ping</span></span>](ack-for-ping.md)                     | <span data-ttu-id="41efd-109">認可 [Ping](ping.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="41efd-109">Acknowledges the [Ping](ping.md) request.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="41efd-110">Create-Session 的 Ack</span><span class="sxs-lookup"><span data-stu-id="41efd-110">Ack for Create-Session</span></span>](ack-for-create-session.md) | <span data-ttu-id="41efd-111">認可 [建立會話](create-session.md) 的要求，並傳回 BITS 用戶端在所有後續要求中用來識別此檔案傳輸會話的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="41efd-111">Acknowledges the [Create-Session](create-session.md) request and returns a session identifier that the BITS client uses on all subsequent requests to identify this file transfer session.</span></span> |
| [<span data-ttu-id="41efd-112">適用于片段的 Ack</span><span class="sxs-lookup"><span data-stu-id="41efd-112">Ack for Fragment</span></span>](ack-for-fragment.md)             | <span data-ttu-id="41efd-113">認可 [片段](fragment.md) 要求，並將片段寫入伺服器上的上傳檔案。</span><span class="sxs-lookup"><span data-stu-id="41efd-113">Acknowledges the [Fragment](fragment.md) request and writes the fragment to the upload file on the server.</span></span>                                                                                 |
| [<span data-ttu-id="41efd-114">確認是否已關閉會話</span><span class="sxs-lookup"><span data-stu-id="41efd-114">Ack for Close-Session</span></span>](ack-for-close-session.md)   | <span data-ttu-id="41efd-115">認可「 [關閉會話](close-session.md) 」要求，並釋放與該會話相關聯的所有資源。</span><span class="sxs-lookup"><span data-stu-id="41efd-115">Acknowledges the [Close-Session](close-session.md) request and releases all resources associated with the session.</span></span>                                                                         |
| [<span data-ttu-id="41efd-116">Ack 以進行取消-會話</span><span class="sxs-lookup"><span data-stu-id="41efd-116">Ack for Cancel-Session</span></span>](ack-for-cancel-session.md) | <span data-ttu-id="41efd-117">認可 [取消會話](cancel-session.md) 的要求，並釋放與會話相關聯的所有資源。</span><span class="sxs-lookup"><span data-stu-id="41efd-117">Acknowledges the [Cancel-Session](cancel-session.md) request and releases all resources associated with the session.</span></span>                                                                       |



 

 

 




