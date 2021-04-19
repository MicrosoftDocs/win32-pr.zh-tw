---
title: COM 處理常式
description: COM 處理常式的目的是要提供一些 \ 0034; smart \ 0034;用戶端位址空間中的程式碼，可優化用戶端與伺服器之間的呼叫。 處理常式可以覆寫一些介面，同時透過 proxy) 將其他介面直接委派給伺服器 (。
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb66a94942cd46424339cfffbde925f62e20e5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967186"
---
# <a name="com-handlers"></a><span data-ttu-id="9571a-104">COM 處理常式</span><span class="sxs-lookup"><span data-stu-id="9571a-104">COM Handlers</span></span>

<span data-ttu-id="9571a-105">COM 處理常式的目的是在用戶端位址空間中提供一些「智慧型」程式碼，以優化用戶端與伺服器之間的呼叫。</span><span class="sxs-lookup"><span data-stu-id="9571a-105">The purpose of COM handlers is to provide some "smart" code in the client address space that can optimize calls between a client and server.</span></span> <span data-ttu-id="9571a-106">處理常式可以覆寫一些介面，同時透過 proxy) 將其他介面直接委派給伺服器 (。</span><span class="sxs-lookup"><span data-stu-id="9571a-106">Handlers can override some interfaces while delegating others directly to the server (through the proxy).</span></span>

<span data-ttu-id="9571a-107">COM 處理常式有兩種類型：</span><span class="sxs-lookup"><span data-stu-id="9571a-107">There are two types of COM handlers:</span></span>

-   <span data-ttu-id="9571a-108">[OLE 處理常式](the-ole-handler.md) 是一種重量級 DLL，可提供連結和內嵌的重要服務。</span><span class="sxs-lookup"><span data-stu-id="9571a-108">[The OLE handler](the-ole-handler.md) is a heavyweight DLL that provides important services for linking and embedding.</span></span> <span data-ttu-id="9571a-109">它通常是在伺服器啟動之前建立的，而且會在内嵌物件進入執行狀態時，讓伺服器啟動時啟動。</span><span class="sxs-lookup"><span data-stu-id="9571a-109">It is usually created before the server is launched and is initialized so that the server is activated when the embedded object enters the running state.</span></span>
-   <span data-ttu-id="9571a-110">[輕量用戶端處理常式](the-lightweight-client-side-handler.md) 可基於任何目的而建立，可能非常小，而且無法在伺服器之前建立。</span><span class="sxs-lookup"><span data-stu-id="9571a-110">[The lightweight client-side handler](the-lightweight-client-side-handler.md) can be created for any purpose, can be very small, and cannot be created before the server.</span></span>

 

 




