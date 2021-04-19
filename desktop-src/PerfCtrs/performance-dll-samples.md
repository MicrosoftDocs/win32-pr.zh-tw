---
description: Windows SDK (WSDK) 包含三個完整的範例效能 Dll。
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: 效能 DLL 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e2210899651a065218474eb49175553a05aa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978969"
---
# <a name="performance-dll-samples"></a><span data-ttu-id="04cae-103">效能 DLL 範例</span><span class="sxs-lookup"><span data-stu-id="04cae-103">Performance DLL Samples</span></span>

<span data-ttu-id="04cae-104">Windows SDK (WSDK) 包含三個完整的範例效能 Dll。</span><span class="sxs-lookup"><span data-stu-id="04cae-104">The Windows SDK (WSDK) contains three complete sample performance DLLs.</span></span> <span data-ttu-id="04cae-105">這些範例位於範例 \\ WinBase \\ WinNT \\ PerfTool \\ PerfDlls 目錄中。</span><span class="sxs-lookup"><span data-stu-id="04cae-105">These samples are located in the Samples\\WinBase\\WinNT\\PerfTool\\PerfDlls directory.</span></span> <span data-ttu-id="04cae-106">此路徑的根目錄是 WSDK 的基礎安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="04cae-106">The root of this path is the base installation directory of the WSDK.</span></span> <span data-ttu-id="04cae-107">您可以從 [Microsoft Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) 下載 WSDK (搜尋 Windows SDK，然後針對最新發行的作業系統) 選取下載。</span><span class="sxs-lookup"><span data-stu-id="04cae-107">You can download the WSDK from the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (search for Windows SDK and select the download for the latest released operating system).</span></span>

<span data-ttu-id="04cae-108">此目錄中包含的範例包括：</span><span class="sxs-lookup"><span data-stu-id="04cae-108">The samples contained in this directory are:</span></span>

-   <span data-ttu-id="04cae-109">**AppMem**：提供 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc)、 [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)和 [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) 函式的對應項，這些函數會報告效能資訊。</span><span class="sxs-lookup"><span data-stu-id="04cae-109">**AppMem**—Provides counterparts of the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc), and [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) functions that report performance information.</span></span> <span data-ttu-id="04cae-110">登錄中的效能計數器和效能工具可以讀取效能資訊。</span><span class="sxs-lookup"><span data-stu-id="04cae-110">Performance counters in the registry and the Performance tool can read the performance information.</span></span>
-   <span data-ttu-id="04cae-111">**LeakyBin**：示範如何使用應用程式效能計數器。</span><span class="sxs-lookup"><span data-stu-id="04cae-111">**LeakyBin**—Demonstrates the use of application performance counters.</span></span>
-   <span data-ttu-id="04cae-112">**PerfGen**-在五個不同期間提供三個波形，以搭配效能工具使用，以已知的速率和值提供資料。</span><span class="sxs-lookup"><span data-stu-id="04cae-112">**PerfGen**—Provides three waveforms at five different periods for use with the Performance tool to provide data at a known rate and value.</span></span> <span data-ttu-id="04cae-113">這有助於測試使用效能資料的應用程式，並需要可預測的值來進行測試。</span><span class="sxs-lookup"><span data-stu-id="04cae-113">This can be useful in testing applications that use performance data and need predictable values to test against.</span></span>

 

 
