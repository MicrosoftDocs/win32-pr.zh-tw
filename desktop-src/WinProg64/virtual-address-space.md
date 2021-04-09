---
title: 64位 Windows) 的虛擬位址空間 (程式設計指南
description: 根據預設，64位的 Microsoft Windows 應用程式具有數 tb 的使用者模式位址空間。
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- 64位 Windows 程式設計指南64位 Windows 程式設計，虛擬位址空間
- 虛擬位址空間64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e4aa6eb67ebf931d1152b3a1101df2757e899b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024398"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a><span data-ttu-id="6393b-105">64位 Windows) 的虛擬位址空間 (程式設計指南</span><span class="sxs-lookup"><span data-stu-id="6393b-105">Virtual Address Space (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="6393b-106">根據預設，64位的 Microsoft Windows 應用程式具有數 tb 的使用者模式位址空間。</span><span class="sxs-lookup"><span data-stu-id="6393b-106">By default, 64-bit Microsoft Windows-based applications have a user-mode address space of several terabytes.</span></span> <span data-ttu-id="6393b-107">如需精確的值，請參閱 [windows 和 Windows Server 版本的記憶體限制](/windows/desktop/Memory/memory-limits-for-windows-releases)。</span><span class="sxs-lookup"><span data-stu-id="6393b-107">For precise values, see [Memory Limits for Windows and Windows Server Releases](/windows/desktop/Memory/memory-limits-for-windows-releases).</span></span> <span data-ttu-id="6393b-108">不過，應用程式可以指定系統應配置低於 2 gb 的應用程式記憶體。</span><span class="sxs-lookup"><span data-stu-id="6393b-108">However, applications can specify that the system should allocate all memory for the application below 2 gigabytes.</span></span> <span data-ttu-id="6393b-109">如果下列條件成立，則這項功能對64位應用程式很有説明：</span><span class="sxs-lookup"><span data-stu-id="6393b-109">This feature is beneficial for 64-bit applications if the following conditions are true:</span></span>

-   <span data-ttu-id="6393b-110">2 GB 的位址空間已足夠。</span><span class="sxs-lookup"><span data-stu-id="6393b-110">A 2 GB address space is sufficient.</span></span>
-   <span data-ttu-id="6393b-111">程式碼有許多指標截斷警告。</span><span class="sxs-lookup"><span data-stu-id="6393b-111">The code has many pointer truncation warnings.</span></span>
-   <span data-ttu-id="6393b-112">指標和整數可任意混合。</span><span class="sxs-lookup"><span data-stu-id="6393b-112">Pointers and integers are freely mixed.</span></span>
-   <span data-ttu-id="6393b-113">程式碼具有使用32位資料類型的多型。</span><span class="sxs-lookup"><span data-stu-id="6393b-113">The code has polymorphism using 32-bit data types.</span></span>

<span data-ttu-id="6393b-114">所有指標仍然是64位指標，但系統可確保每個記憶體配置都會低於 2 GB 的限制，因此，如果應用程式截斷指標，則不會遺失任何重要資料。</span><span class="sxs-lookup"><span data-stu-id="6393b-114">All pointers are still 64-bit pointers, but the system ensures that every memory allocation occurs below the 2 GB limit, so that if the application truncates a pointer, no significant data is lost.</span></span> <span data-ttu-id="6393b-115">指標可以截斷為32位值，然後藉由符號延伸或零延伸來延伸至64位值。</span><span class="sxs-lookup"><span data-stu-id="6393b-115">Pointers can be truncated to 32-bit values, then extended to 64-bit values by either sign extension or zero extension.</span></span>

<span data-ttu-id="6393b-116">若要指定此記憶體限制，請使用 **/LARGEADDRESSAWARE： NO** 連結器選項。</span><span class="sxs-lookup"><span data-stu-id="6393b-116">To specify this memory limitation, use the **/LARGEADDRESSAWARE:NO** linker option.</span></span> <span data-ttu-id="6393b-117">請注意，ARM64 二進位檔會忽略 **/LARGEADDRESSAWARE： NO** 。</span><span class="sxs-lookup"><span data-stu-id="6393b-117">Note that **/LARGEADDRESSAWARE:NO** is ignored for an ARM64 binary.</span></span> <span data-ttu-id="6393b-118">不過，請注意，使用此選項時可能會發生問題。</span><span class="sxs-lookup"><span data-stu-id="6393b-118">However, be aware that problems can occur when using this option.</span></span> <span data-ttu-id="6393b-119">如果您建立的 DLL 會使用這個選項，而且 DLL 是由未使用此選項的應用程式所呼叫，DLL 可能會截斷32位較高的64位指標。</span><span class="sxs-lookup"><span data-stu-id="6393b-119">If you build a DLL that uses this option and the DLL is called by an application that does not use this option, the DLL could truncate a 64-bit pointer whose upper 32 bits are significant.</span></span> <span data-ttu-id="6393b-120">這可能會導致應用程式失敗，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="6393b-120">This can cause application failure without any warning.</span></span>

 

 
