---
title: RPC 記憶體管理簡介
description: " (RPC) 記憶體管理的遠端程序呼叫簡介。"
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316063"
---
# <a name="introduction-to-rpc-memory-management"></a><span data-ttu-id="5b620-103">RPC 記憶體管理簡介</span><span class="sxs-lookup"><span data-stu-id="5b620-103">Introduction to RPC Memory Management</span></span>

<span data-ttu-id="5b620-104">在 RPC 的內容中，記憶體管理牽涉到：</span><span class="sxs-lookup"><span data-stu-id="5b620-104">In the context of RPC, memory management involves:</span></span>

-   <span data-ttu-id="5b620-105">在用戶端和伺服器執行緒的不同位址空間中，為用戶端與伺服器之間的單一概念位址空間，配置和解除配置所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5b620-105">Allocating and deallocating the memory needed to simulate a single conceptual address space between the client and the server in the different address spaces of the client and server's threads.</span></span>
-   <span data-ttu-id="5b620-106">判斷哪個軟體元件負責管理記憶體—應用程式或 MIDL 產生的存根。</span><span class="sxs-lookup"><span data-stu-id="5b620-106">Determining which software component is responsible for managing memory — the application or the MIDL-generated stub.</span></span>
-   <span data-ttu-id="5b620-107">選取會影響記憶體管理的 MIDL 屬性：方向屬性、指標屬性、陣列屬性，以及 ACF 屬性的 \[ [位元組 \_ 計數](/windows/desktop/Midl/byte-count) \] 、 \[ [配置](/windows/desktop/Midl/allocate) \] 和 \[ [啟用 \_ 配置](/windows/desktop/Midl/enable-allocate) \] 。</span><span class="sxs-lookup"><span data-stu-id="5b620-107">Selecting MIDL attributes that affect memory management: directional attributes, pointer attributes, array attributes, and the ACF attributes \[ [byte\_count](/windows/desktop/Midl/byte-count)\], \[ [allocate](/windows/desktop/Midl/allocate)\], and \[ [enable\_allocate](/windows/desktop/Midl/enable-allocate)\].</span></span>

<span data-ttu-id="5b620-108">當程式在其位址空間中呼叫函式或程式時，記憶體管理會比在分散式應用程式中更直接。</span><span class="sxs-lookup"><span data-stu-id="5b620-108">When a program calls a function or procedure in its address space, memory management is more straightforward than in a distributed application.</span></span> <span data-ttu-id="5b620-109">為了說明，下圖描述二進位樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="5b620-109">To illustrate, the following diagram depicts a binary tree.</span></span> <span data-ttu-id="5b620-110">為了將此資料結構傳遞至其位址空間中的程式，程式只會將指標傳遞至樹狀結構的根。</span><span class="sxs-lookup"><span data-stu-id="5b620-110">To pass this data structure to a procedure in its address space, a program simply passes a pointer to the root of the tree.</span></span>

![二進位樹狀結構，其中包含指向樹狀結構根目錄之資料的指標](images/bintree.png)

<span data-ttu-id="5b620-112">用戶端/伺服器 RPC 應用程式會在兩個不同的記憶體空間之間共用資料。</span><span class="sxs-lookup"><span data-stu-id="5b620-112">Client/server RPC applications share data across two different memory spaces.</span></span> <span data-ttu-id="5b620-113">這些記憶體空間不一定會在同一部電腦上。</span><span class="sxs-lookup"><span data-stu-id="5b620-113">These memory spaces may or may not be on the same computer.</span></span> <span data-ttu-id="5b620-114">無論何種方式，用戶端和伺服器都無法直接存取彼此的記憶體空間。</span><span class="sxs-lookup"><span data-stu-id="5b620-114">Either way, the client and server have no direct access to each other's memory space.</span></span> <span data-ttu-id="5b620-115">RPC 取決於在伺服器程式的位址空間中模擬用戶端程式位址空間的能力。</span><span class="sxs-lookup"><span data-stu-id="5b620-115">RPC depends on the ability to simulate the client program's address space in the server program's address space.</span></span> <span data-ttu-id="5b620-116">它也必須從伺服器傳回用戶端記憶體中的資料，包括新的和變更的資料。</span><span class="sxs-lookup"><span data-stu-id="5b620-116">It must also return data, including new and changed data, from the server to the client memory.</span></span>

<span data-ttu-id="5b620-117">在上圖所示的二進位樹狀結構中，將根節點的指標傳遞至遠端程式並不足夠。</span><span class="sxs-lookup"><span data-stu-id="5b620-117">In cases such as the binary tree depicted in the preceding diagram, it is not sufficient to pass a pointer to the root node to a remote procedure.</span></span> <span data-ttu-id="5b620-118">程式或存根必須將整個樹狀結構傳遞到伺服器的位址空間，才能讓遠端程式進行操作。</span><span class="sxs-lookup"><span data-stu-id="5b620-118">Either the program or the stubs must pass the entire tree to the server's address space for the remote procedure to operate on it.</span></span>

 

 