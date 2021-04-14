---
title: ADSI WinNT 提供者
description: Microsoft ADSI 提供者會執行一組 ADSI 物件來支援各種 ADSI 介面。
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- adsi winnt 提供者 ADSI
- WinNT 服務提供者 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371847"
---
# <a name="adsi-winnt-provider"></a><span data-ttu-id="cb4ff-105">ADSI WinNT 提供者</span><span class="sxs-lookup"><span data-stu-id="cb4ff-105">ADSI WinNT Provider</span></span>

<span data-ttu-id="cb4ff-106">Microsoft ADSI 提供者會執行一組 ADSI 物件來支援各種 ADSI 介面。</span><span class="sxs-lookup"><span data-stu-id="cb4ff-106">The Microsoft ADSI provider implements a set of ADSI objects to support various ADSI interfaces.</span></span> <span data-ttu-id="cb4ff-107">Windows 提供者的命名空間名稱是「WinNT」，而這個提供者通常稱為 WinNT 提供者。</span><span class="sxs-lookup"><span data-stu-id="cb4ff-107">The namespace name for the Windows provider is "WinNT" and this provider is commonly referred to as the WinNT provider.</span></span> <span data-ttu-id="cb4ff-108">若要存取 WinNT 提供者，請使用[Winnt AdsPath](winnt-adspath.md)系結至 winnt 的任何[ADSI 物件](adsi-objects-of-winnt.md)。</span><span class="sxs-lookup"><span data-stu-id="cb4ff-108">To access the WinNT provider, bind to any of the [ADSI objects of WinNT](adsi-objects-of-winnt.md), using the [WinNT AdsPath](winnt-adspath.md).</span></span>

<span data-ttu-id="cb4ff-109">WinNT 提供者包含在適用于 Windows 和 Windows Server 的 ADSI 系統元件中。</span><span class="sxs-lookup"><span data-stu-id="cb4ff-109">The WinNT provider is included in the ADSI system component for Windows and Windows Server.</span></span>

> [!Note]  
> <span data-ttu-id="cb4ff-110">預設的 WinNT 提供者無法假設為完全安全線程。</span><span class="sxs-lookup"><span data-stu-id="cb4ff-110">The default WinNT provider cannot be assumed to be completely thread-safe.</span></span> <span data-ttu-id="cb4ff-111">多執行緒應用程式的寫入器應該會處理多執行緒處理，以適當地協調執行緒之間的任何存取，例如信號、mutex、重要區段等等。</span><span class="sxs-lookup"><span data-stu-id="cb4ff-111">Writers of multithreaded applications should handle multithreading to properly coordinate any access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

 

 




