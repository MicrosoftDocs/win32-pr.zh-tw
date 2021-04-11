---
title: WOW64 下的例外狀況處理
description: WOW64 使用原生 x64、ia64 或 ARM64 例外狀況做為 x86 例外狀況的傳輸。 因此，在 WOW64 下執行的32位應用程式中，未攔截的例外狀況行為就像原生64位例外狀況。
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb57e56b85be4769d452a5772ff7b0024724641
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023956"
---
# <a name="exception-handling-under-wow64"></a><span data-ttu-id="37980-104">WOW64 下的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="37980-104">Exception Handling under WOW64</span></span>

<span data-ttu-id="37980-105">WOW64 使用原生 x64、ia64 或 ARM64 例外狀況做為 x86 例外狀況的傳輸。</span><span class="sxs-lookup"><span data-stu-id="37980-105">WOW64 uses native x64, ia64, or ARM64 exceptions as a transport for x86 exceptions.</span></span> <span data-ttu-id="37980-106">因此，在 WOW64 下執行的32位應用程式中，未攔截的例外狀況行為就像原生64位例外狀況。</span><span class="sxs-lookup"><span data-stu-id="37980-106">Therefore, in a 32-bit application running under WOW64, uncaught exceptions behave like native 64-bit exceptions.</span></span>

<span data-ttu-id="37980-107">在32位版本的 Windows 上執行的應用程式中，未攔截的例外狀況會傳遞至應用程式的較高層級例外狀況處理常式（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="37980-107">In an application running on a 32-bit version of Windows, uncaught exceptions are passed on to higher-level exception handlers of the application, when available.</span></span> <span data-ttu-id="37980-108">在 WOW64 下執行的相同32位應用程式中，系統可能會隱藏未攔截的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="37980-108">In the same 32-bit application running under WOW64, the system may suppress uncaught exceptions.</span></span>

<span data-ttu-id="37980-109">**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 WOW64 下執行的相同32位應用程式中，系統會呼叫例外狀況篩選器，但可能隱藏未攔截的例外狀況，而不會叫用相關聯的處理常式。</span><span class="sxs-lookup"><span data-stu-id="37980-109">**Windows Vista, Windows Server 2003 and Windows XP:** In the same 32-bit application running under WOW64, the system calls the exception filters but may suppress uncaught exceptions without invoking the associated handlers.</span></span> <span data-ttu-id="37980-110">從 Windows Vista Service Pack 1 (SP1) 開始，此行為已變更。</span><span class="sxs-lookup"><span data-stu-id="37980-110">This behavior changed starting with Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="37980-111">如需視窗程式中未攔截之例外狀況的詳細資訊，請參閱 [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="37980-111">For more information about uncaught exceptions in window procedures, see the [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

 

 