---
description: 網路提供者是支援特定網路通訊協定的 DLL。
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: 網路提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e3cc231f461d48e7ce71d908cb92f6cd06eabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194062"
---
# <a name="network-providers"></a><span data-ttu-id="2f83b-103">網路提供者</span><span class="sxs-lookup"><span data-stu-id="2f83b-103">Network Providers</span></span>

<span data-ttu-id="2f83b-104">網路提供者是支援特定網路通訊協定的 DLL。</span><span class="sxs-lookup"><span data-stu-id="2f83b-104">A network provider is a DLL that supports a specific network protocol.</span></span> <span data-ttu-id="2f83b-105">它也會實行 [網路提供者 API](network-provider-api.md)。</span><span class="sxs-lookup"><span data-stu-id="2f83b-105">It also implements the [Network Provider API](network-provider-api.md).</span></span> <span data-ttu-id="2f83b-106">這可讓它與 Windows 作業系統互動，以接收標準的網路要求，例如連線或中斷連接要求。</span><span class="sxs-lookup"><span data-stu-id="2f83b-106">This enables it to interact with the Windows operating system to receive standard network requests, such as connection or disconnection requests.</span></span> <span data-ttu-id="2f83b-107">為了處理這些要求，網路提供者接著會呼叫網路提供者所支援之網路通訊協定適用的特定網路 API。</span><span class="sxs-lookup"><span data-stu-id="2f83b-107">To handle these requests, the network provider then calls the network-specific API that is appropriate to the network protocol the network provider supports.</span></span> <span data-ttu-id="2f83b-108">換句話說，網路提供者會將網路特有的功能包裝在 DLL 中，以將標準介面公開給 Windows。</span><span class="sxs-lookup"><span data-stu-id="2f83b-108">In other words, the network provider wraps the network-specific functionality in a DLL, which exposes a standard interface to Windows.</span></span>

<span data-ttu-id="2f83b-109">使用網路提供者時，Windows 可以支援許多不同類型的網路通訊協定，而不需要知道每個網路的網路特定詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2f83b-109">Using network providers, Windows can support many different types of network protocols without having to know the network-specific details of each network.</span></span> <span data-ttu-id="2f83b-110">這是不可或缺的，因為新的網路通訊協定一直都在開發中。</span><span class="sxs-lookup"><span data-stu-id="2f83b-110">This is essential because new network protocols are being developed all the time.</span></span> <span data-ttu-id="2f83b-111">使用網路提供者時，支援新的通訊協定只需要建立並安裝新的網路提供者。</span><span class="sxs-lookup"><span data-stu-id="2f83b-111">With network providers, supporting a new protocol simply requires creating and installing a new network provider.</span></span>

<span data-ttu-id="2f83b-112">如需網路提供者函式和結構的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="2f83b-112">For information about network provider functions and structures, see the following topics:</span></span>

-   [<span data-ttu-id="2f83b-113">網路提供者函式</span><span class="sxs-lookup"><span data-stu-id="2f83b-113">Network Provider Functions</span></span>](authentication-functions.md)
-   [<span data-ttu-id="2f83b-114">網路提供者結構</span><span class="sxs-lookup"><span data-stu-id="2f83b-114">Network Provider Structures</span></span>](authentication-structures.md)

 

 



