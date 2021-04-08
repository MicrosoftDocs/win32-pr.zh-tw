---
title: WOW64 下的處理器親和性
description: 32位 Windows 最多可支援32個處理器。 因此，GetProcessAffinityMask 之類的函式會在 WOW64 下呼叫時模擬具有32處理器的電腦。
ms.assetid: f50a03e8-1c23-4eb0-a1ff-471c28d6b611
keywords:
- 處理器親和性 64-位 Windows 程式設計
- WOW64 64 位 Windows 程式設計，處理器親和性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60ad6cf5055737dc39abd735211c5b4ec4ab9d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682635"
---
# <a name="processor-affinity-under-wow64"></a><span data-ttu-id="af411-106">WOW64 下的處理器親和性</span><span class="sxs-lookup"><span data-stu-id="af411-106">Processor Affinity Under WOW64</span></span>

<span data-ttu-id="af411-107">32位 Windows 最多可支援32個處理器。</span><span class="sxs-lookup"><span data-stu-id="af411-107">32-bit Windows supports a maximum of 32 processors.</span></span> <span data-ttu-id="af411-108">因此， [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) 之類的函式會在 WOW64 下呼叫時模擬具有32處理器的電腦。</span><span class="sxs-lookup"><span data-stu-id="af411-108">Therefore, functions such as [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulate a computer with 32 processors when called under WOW64.</span></span>

<span data-ttu-id="af411-109">使用低32位來執行遮罩的前32位位 OR 運算，即可取得相似性遮罩。</span><span class="sxs-lookup"><span data-stu-id="af411-109">The affinity mask is obtained by performing a bitwise OR operation of the top 32 bits of the mask with the low 32 bits.</span></span> <span data-ttu-id="af411-110">因此，如果執行緒有處理器0、1和32的親和性，則 WOW64 會將親和性回報為0和1，因為處理器32會對應到處理器0。</span><span class="sxs-lookup"><span data-stu-id="af411-110">Therefore, if a thread has affinity for processors 0, 1, and 32, WOW64 reports the affinity as 0 and 1, because processor 32 maps to processor 0.</span></span> <span data-ttu-id="af411-111">設定處理器親和性的函式（例如 [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask)）會將處理器限制在 WOW64 下的第一個32處理器。</span><span class="sxs-lookup"><span data-stu-id="af411-111">Functions that set processor affinity, such as [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), restrict processors to the first 32 processors under WOW64.</span></span>

<span data-ttu-id="af411-112">如需處理器親和性的詳細資訊，請參閱 [多個處理器](/windows/desktop/ProcThread/multiple-processors)。</span><span class="sxs-lookup"><span data-stu-id="af411-112">For more information about processor affinity, see [Multiple Processors](/windows/desktop/ProcThread/multiple-processors).</span></span>

 

 