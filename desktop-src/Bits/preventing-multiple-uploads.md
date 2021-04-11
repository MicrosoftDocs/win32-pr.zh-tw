---
title: 防止多個上傳
description: 當您上傳檔案時，BITS 會建立會話識別碼，以識別 BITS 用戶端和 BITS 伺服器的上傳會話。
ms.assetid: 97283f8e-d2fa-4383-9b92-a05f46680443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae59bb1d605af7e4dd53b0c1d66618b6816e7886
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020897"
---
# <a name="preventing-multiple-uploads"></a><span data-ttu-id="81b0f-103">防止多個上傳</span><span class="sxs-lookup"><span data-stu-id="81b0f-103">Preventing Multiple Uploads</span></span>

<span data-ttu-id="81b0f-104">當您上傳檔案時，BITS 會建立會話識別碼，以識別 BITS 用戶端和 BITS 伺服器的上傳會話。</span><span class="sxs-lookup"><span data-stu-id="81b0f-104">When you upload a file, BITS creates a session ID that identifies the upload session to both the BITS client and BITS server.</span></span> <span data-ttu-id="81b0f-105">如果 BITS 用戶端與伺服器之間的連接在 BITS 上傳檔案時中斷，用戶端會使用會話識別碼來嘗試繼續上傳。</span><span class="sxs-lookup"><span data-stu-id="81b0f-105">If the connection between the BITS client and server is broken while BITS is uploading a file, the client will use the session ID to try to resume the upload.</span></span>

<span data-ttu-id="81b0f-106">如果 BITS 用戶端連接到與之前相同的伺服器，伺服器將會辨識會話識別碼，而上傳將會從中中斷點繼續。</span><span class="sxs-lookup"><span data-stu-id="81b0f-106">If the BITS client connects to the same server as before, the server will recognize the session ID and the upload will resume from the point of interruption.</span></span> <span data-ttu-id="81b0f-107">但是，如果用戶端連接到不同的伺服器，用戶端就必須從頭開始上傳，因為新的伺服器沒有會話內容或先前上傳的資料。</span><span class="sxs-lookup"><span data-stu-id="81b0f-107">However, if the client connects to a different server, the client must start the upload from the beginning because the new server does not have the session context or the previously uploaded data.</span></span> <span data-ttu-id="81b0f-108">當 BITS 伺服器裝載于 web 伺服陣列，且未設定 BITS IIS 擴充屬性（ [BITSHostId](bits-iis-extension-properties.md)）時，bits 可能會連接到不同的伺服器。</span><span class="sxs-lookup"><span data-stu-id="81b0f-108">BITS may connect to a different server when the BITS server is hosted on a web farm and the BITS IIS extension property, [BITSHostId](bits-iis-extension-properties.md), is not set.</span></span> <span data-ttu-id="81b0f-109">BITSHostId 屬性會強制 BITS 用戶端連接到先前伺服器的唯一位址，而非共用伺服器位址，以防止重新開機。</span><span class="sxs-lookup"><span data-stu-id="81b0f-109">The BITSHostId property prevents restarts by forcing the BITS client to connect to the previous server's unique address instead of the shared server address.</span></span>

<span data-ttu-id="81b0f-110">BITS 伺服器將只會嘗試將上傳檔案一次傳送至伺服器應用程式，但可能會有可能傳送一次以上的檔案。</span><span class="sxs-lookup"><span data-stu-id="81b0f-110">The BITS server will attempt to send the upload file only once to the server application, but it is possible that the file may be sent more than one time.</span></span> <span data-ttu-id="81b0f-111">例如，如果 BITS 伺服器將檔案傳送至伺服器應用程式，然後在等候伺服器應用程式的回復時終止，則可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="81b0f-111">This can occur, for example, if the BITS server sends the file to the server application and then terminates while waiting for the reply from the server application.</span></span> <span data-ttu-id="81b0f-112">BITS 用戶端會收到來自 HTTP 層的錯誤碼，並在延遲後重試上傳。</span><span class="sxs-lookup"><span data-stu-id="81b0f-112">The BITS client will receive an error code from the HTTP layer, and retry the upload after a delay.</span></span> <span data-ttu-id="81b0f-113">如果伺服器保持離線的時間超過 [BITSHostIdFallbackTimeout](bits-iis-extension-properties.md) timeout，用戶端最後會再次將要求傳送至共用伺服器位址;不同的 BITS 伺服器將會收到檔案，然後再將它傳遞給伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="81b0f-113">If the server stays offline for longer than the [BITSHostIdFallbackTimeout](bits-iis-extension-properties.md) timeout, then the client will eventually send the request to the shared server address again; a different BITS server will receive the file and deliver it again to the server application.</span></span>

<span data-ttu-id="81b0f-114">即使是單一前端伺服器，也會發生類似的情況。</span><span class="sxs-lookup"><span data-stu-id="81b0f-114">A similar case can occur even with a single front-end server.</span></span> <span data-ttu-id="81b0f-115">例如，當用戶端將整個檔案上傳到伺服器時，最終區塊會導致伺服器將檔案轉寄至伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="81b0f-115">For example, when the client has uploaded the entire file to the server, the final block causes the server to forward the file to the server application.</span></span> <span data-ttu-id="81b0f-116">如果 BITS 伺服器或伺服器應用程式在處理檔案之後，但在通知傳送至用戶端之前終止，則用戶端會收到錯誤碼，並于稍後重試。</span><span class="sxs-lookup"><span data-stu-id="81b0f-116">If the BITS server or the server application terminate after the file is processed but before the acknowledgment is sent to the client, then the client will receive an error code and retry later.</span></span> <span data-ttu-id="81b0f-117">當用戶端重試時，BITS 伺服器會看到最後一個區塊已上傳，並再次將檔案轉寄至伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="81b0f-117">When the client retries, the BITS server will see that the final block has been uploaded, and it will again forward the file to the server application.</span></span> <span data-ttu-id="81b0f-118">如果接收上傳檔案多次是您的伺服器應用程式的問題，您應該考慮在資料中包含交易識別碼。</span><span class="sxs-lookup"><span data-stu-id="81b0f-118">If receiving the upload file multiple times is an issue for your server application, you should consider including a transaction identifier in the data.</span></span>

 

 




