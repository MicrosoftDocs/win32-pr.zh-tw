---
description: 32位 Microsoft Windows 上的每個進程都有自己的虛擬位址空間，可讓您定址最多 4 gb 的記憶體。
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: 關於記憶體管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4110bf1d0768f1321fd89ddd1d5a985e3e54aa75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971406"
---
# <a name="about-memory-management"></a><span data-ttu-id="c3c15-103">關於記憶體管理</span><span class="sxs-lookup"><span data-stu-id="c3c15-103">About Memory Management</span></span>

<span data-ttu-id="c3c15-104">32位 Microsoft Windows 上的每個進程都有自己的虛擬位址空間，可讓您定址最多 4 gb 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="c3c15-104">Each process on 32-bit Microsoft Windows has its own virtual address space that enables addressing up to 4 gigabytes of memory.</span></span> <span data-ttu-id="c3c15-105">64位 Windows 上的每個進程都有 8 tb 的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="c3c15-105">Each process on 64-bit Windows has a virtual address space of 8 terabytes.</span></span> <span data-ttu-id="c3c15-106">進程的所有線程都可以存取其虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="c3c15-106">All threads of a process can access its virtual address space.</span></span> <span data-ttu-id="c3c15-107">但是，執行緒無法存取屬於另一個進程的記憶體，以防止其他進程損毀進程。</span><span class="sxs-lookup"><span data-stu-id="c3c15-107">However, threads cannot access memory that belongs to another process, which protects a process from being corrupted by another process.</span></span>

<span data-ttu-id="c3c15-108">如需虛擬位址空間和記憶體管理函數的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="c3c15-108">For information on the virtual address space and the memory management functions, see the following topics.</span></span>

-   [<span data-ttu-id="c3c15-109">虛擬位址空間</span><span class="sxs-lookup"><span data-stu-id="c3c15-109">Virtual Address Space</span></span>](virtual-address-space.md)
-   [<span data-ttu-id="c3c15-110">記憶體集區</span><span class="sxs-lookup"><span data-stu-id="c3c15-110">Memory Pools</span></span>](memory-pools.md)
-   [<span data-ttu-id="c3c15-111">記憶體效能資訊</span><span class="sxs-lookup"><span data-stu-id="c3c15-111">Memory Performance Information</span></span>](memory-performance-information.md)
-   [<span data-ttu-id="c3c15-112">虛擬記憶體函數</span><span class="sxs-lookup"><span data-stu-id="c3c15-112">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
-   [<span data-ttu-id="c3c15-113">堆積函數</span><span class="sxs-lookup"><span data-stu-id="c3c15-113">Heap Functions</span></span>](heap-functions.md)
-   [<span data-ttu-id="c3c15-114">檔案對應</span><span class="sxs-lookup"><span data-stu-id="c3c15-114">File Mapping</span></span>](file-mapping.md)
-   [<span data-ttu-id="c3c15-115">海量儲存體支援</span><span class="sxs-lookup"><span data-stu-id="c3c15-115">Large Memory Support</span></span>](large-memory-support.md)
-   [<span data-ttu-id="c3c15-116">全域和區域函數</span><span class="sxs-lookup"><span data-stu-id="c3c15-116">Global and Local Functions</span></span>](global-and-local-functions.md)
-   [<span data-ttu-id="c3c15-117">標準 C 程式庫函式</span><span class="sxs-lookup"><span data-stu-id="c3c15-117">Standard C Library Functions</span></span>](standard-c-library-functions.md)
-   [<span data-ttu-id="c3c15-118">比較記憶體配置方法</span><span class="sxs-lookup"><span data-stu-id="c3c15-118">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)

 

 



