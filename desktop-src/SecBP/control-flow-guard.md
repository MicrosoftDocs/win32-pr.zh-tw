---
description: 控制流程防護 (CFG) 是一種高度優化的平臺安全性功能，其建立是為了對抗記憶體損毀弱點。
ms.assetid: 116EAD64-7CAE-455C-BA43-9492F78DE873
title: 控制流程防護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cf97a648443135e7fee666ea4c259b1c32104e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115908"
---
# <a name="control-flow-guard"></a><span data-ttu-id="1f539-103">控制流程防護</span><span class="sxs-lookup"><span data-stu-id="1f539-103">Control Flow Guard</span></span>

## <a name="what-is-control-flow-guard"></a><span data-ttu-id="1f539-104">什麼是控制流程防護？</span><span class="sxs-lookup"><span data-stu-id="1f539-104">What is Control Flow Guard?</span></span>

<span data-ttu-id="1f539-105">控制流程防護 (CFG) 是一種高度優化的平臺安全性功能，其建立是為了對抗記憶體損毀弱點。</span><span class="sxs-lookup"><span data-stu-id="1f539-105">Control Flow Guard (CFG) is a highly-optimized platform security feature that was created to combat memory corruption vulnerabilities.</span></span> <span data-ttu-id="1f539-106">藉由對應用程式可從中執行程式碼的位置進行嚴格的限制，就能讓惡意探索更難利用緩衝區溢位等弱點來執行任意程式碼。</span><span class="sxs-lookup"><span data-stu-id="1f539-106">By placing tight restrictions on where an application can execute code from, it makes it much harder for exploits to execute arbitrary code through vulnerabilities such as buffer overflows.</span></span> <span data-ttu-id="1f539-107">CFG 擴充了先前的惡意探索緩和技術，例如 [/gs](/cpp/build/reference/gs-buffer-security-check?view=vs-2019)、 [DEP](../memory/data-execution-prevention.md)和 [ASLR](/archive/blogs/michael_howard/address-space-layout-randomization-in-windows-vista)。</span><span class="sxs-lookup"><span data-stu-id="1f539-107">CFG extends previous exploit mitigation technologies such as [/GS](/cpp/build/reference/gs-buffer-security-check?view=vs-2019), [DEP](../memory/data-execution-prevention.md), and [ASLR](/archive/blogs/michael_howard/address-space-layout-randomization-in-windows-vista).</span></span>

<span data-ttu-id="1f539-108">這項功能可在 Microsoft Visual Studio 2015 中取得，並可在「CFG 感知」版本的 Windows 上執行，也就是適用于桌上型電腦和伺服器的 x86 和 x64 版本，Windows 10 和 Windows 8.1 更新版 (KB3000850) 。</span><span class="sxs-lookup"><span data-stu-id="1f539-108">This feature is available in Microsoft Visual Studio 2015, and runs on "CFG-Aware" versions of Windows—the x86 and x64 releases for Desktop and Server of Windows 10 and Windows 8.1 Update (KB3000850).</span></span>

<span data-ttu-id="1f539-109">我們強烈建議開發人員為其應用程式啟用 CFG。</span><span class="sxs-lookup"><span data-stu-id="1f539-109">We strongly encourage developers to enable CFG for their applications.</span></span> <span data-ttu-id="1f539-110">您不需要為程式碼的每個部分啟用 CFG，因為已啟用混合的 CFG 和非 CFG 啟用的程式碼將會正常執行。</span><span class="sxs-lookup"><span data-stu-id="1f539-110">You don't have to enable CFG for every part of your code, as a mixture of CFG enabled and non-CFG enabled code will execute fine.</span></span> <span data-ttu-id="1f539-111">但是無法針對所有程式碼啟用 CFG，可以在保護中開啟間距。</span><span class="sxs-lookup"><span data-stu-id="1f539-111">But failing to enable CFG for all code can open gaps in the protection.</span></span> <span data-ttu-id="1f539-112">此外，CFG 啟用的程式碼可在「CFG 感知」版本的 Windows 上正常運作，因此完全與其相容。</span><span class="sxs-lookup"><span data-stu-id="1f539-112">Furthermore, CFG enabled code works fine on "CFG-Unaware" versions of Windows and is therefore fully compatible with them.</span></span>

## <a name="how-can-i-enable-cfg"></a><span data-ttu-id="1f539-113">如何啟用 CFG？</span><span class="sxs-lookup"><span data-stu-id="1f539-113">How Can I Enable CFG?</span></span>

<span data-ttu-id="1f539-114">在大部分情況下，不需要變更原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="1f539-114">In most cases, there is no need to change source code.</span></span> <span data-ttu-id="1f539-115">您只需要在 Visual Studio 2015 專案中新增一個選項，編譯器和連結器就會啟用 CFG。</span><span class="sxs-lookup"><span data-stu-id="1f539-115">All you have to do is add an option to your Visual Studio 2015 project, and the compiler and linker will enable CFG.</span></span>

<span data-ttu-id="1f539-116">最簡單的方法是流覽至 **專案 \| 屬性設定 \| 屬性 \| C/c + + 程式 \| 代碼產生** ，然後選擇 **[是] (/Guard： cf)** 用於控制流程防護。</span><span class="sxs-lookup"><span data-stu-id="1f539-116">The simplest method is to navigate to **Project \| Properties \| Configuration Properties \| C/C++ \| Code Generation** and choose **Yes (/guard:cf)** for Control Flow Guard.</span></span>

![visual studio 中的 cfg 屬性](images/cfg-vs.png)

<span data-ttu-id="1f539-118">或者，將 **/guard： cf** 新增至 **專案 \| 屬性設定 \| 屬性 \| C/c + + \| 命令列 \| 額外選項** (針對編譯器) 和 **/Guard： cf** 至 **專案屬性設定 \| \| 屬性 \| 連結器 \| 命令列 \| 額外選項** (的連結器) 。</span><span class="sxs-lookup"><span data-stu-id="1f539-118">Alternatively, add **/guard:cf** to **Project \| Properties \| Configuration Properties \| C/C++ \| Command Line \| Additional Options** (for the compiler) and **/guard:cf** to **Project \| Properties \| Configuration Properties \| Linker \| Command Line \| Additional Options** (for the linker).</span></span>

![編譯器的 cfg 屬性](images/cfg-compiler.png)![連結器的 cfg 屬性](images/cfg-linker.png)

<span data-ttu-id="1f539-121">如需其他資訊，請參閱 [/guard (啟用控制流程防護) ](/cpp/build/reference/guard-enable-control-flow-guard?view=vs-2019) 。</span><span class="sxs-lookup"><span data-stu-id="1f539-121">See [/guard (Enable Control Flow Guard)](/cpp/build/reference/guard-enable-control-flow-guard?view=vs-2019) for additional info.</span></span>

<span data-ttu-id="1f539-122">如果您是從命令列建立您的專案，您可以新增相同的選項。</span><span class="sxs-lookup"><span data-stu-id="1f539-122">If you are building your project from the command line, you can add the same options.</span></span> <span data-ttu-id="1f539-123">例如，如果您要編譯稱為 test .cpp 的專案，請使用 **cl/guard： cf test .cpp/guard： cf**。</span><span class="sxs-lookup"><span data-stu-id="1f539-123">For example, if you are compiling a project called test.cpp, use **cl /guard:cf test.cpp /link /guard:cf**.</span></span>

<span data-ttu-id="1f539-124">您也可以選擇使用記憶體管理 API 中的 [**SetProcessValidCallTargets**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessvalidcalltargets) ，以動態方式控制由 CFG 視為有效的一組 icall 目標位址。</span><span class="sxs-lookup"><span data-stu-id="1f539-124">You also have the option of dynamically controlling the set of icall target addresses that are considered valid by CFG using the [**SetProcessValidCallTargets**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessvalidcalltargets) from the Memory Management API.</span></span> <span data-ttu-id="1f539-125">您可以使用相同的 API 來指定頁面是否為 CFG 的無效或有效的目標。</span><span class="sxs-lookup"><span data-stu-id="1f539-125">The same API can be used to specify whether pages are invalid or valid targets for CFG.</span></span> <span data-ttu-id="1f539-126">[**VirtualProtect**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect)和 [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)函數預設會將可執行檔和認可頁面的指定區域視為有效的間接呼叫目標。</span><span class="sxs-lookup"><span data-stu-id="1f539-126">The [**VirtualProtect**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect) and [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) functions will by default treat a specified region of executable and committed pages as valid indirect call targets.</span></span> <span data-ttu-id="1f539-127">您可以覆寫此行為，例如在實作為時間的編譯器時，在呼叫 **VirtualAlloc** 時指定不正確頁面目標，或在呼叫 **VirtualProtect** 時指定 **\_ \_ 無效** 的頁面目標，如 [**記憶體保護常數**](/windows/desktop/Memory/memory-protection-constants)中所述。 **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f539-127">It is possible to override this behavior, such as when implementing a Just-in-Time compiler, by specifying **PAGE\_TARGETS\_INVALID** when calling **VirtualAlloc** or **PAGE\_TARGETS\_NO\_UPDATE** when calling **VirtualProtect** as detailed under [**Memory Protection Constants**](/windows/desktop/Memory/memory-protection-constants).</span></span>

## <a name="how-do-i-tell-that-a-binary-is-under-control-flow-guard"></a><span data-ttu-id="1f539-128">如何判斷二進位檔位於控制流程防護下？</span><span class="sxs-lookup"><span data-stu-id="1f539-128">How Do I Tell That a Binary is under Control Flow Guard?</span></span>

<span data-ttu-id="1f539-129">使用 */headers* 和 */loadconfig* 選項，從 Visual Studio 命令提示字元執行 [dumpbin 工具](/cpp/build/reference/dumpbin-reference) (包含在 Visual Studio 2015 安裝) 中： **dumpbin/headers/loadconfig test.exe**。</span><span class="sxs-lookup"><span data-stu-id="1f539-129">Run the [dumpbin tool](/cpp/build/reference/dumpbin-reference) (included in the Visual Studio 2015 installation) from the Visual Studio command prompt with the */headers* and */loadconfig* options: **dumpbin /headers /loadconfig test.exe**.</span></span> <span data-ttu-id="1f539-130">在 CFG 下，二進位檔的輸出應該會顯示標頭值包含 "Guard"，且載入設定值包含「CF 檢測」和「存在 FID 資料表」。</span><span class="sxs-lookup"><span data-stu-id="1f539-130">The output for a binary under CFG should show that the header values include "Guard", and that the load config values include "CF Instrumented" and "FID table present".</span></span>

![dumpbin/headers 的輸出](images/cfg-dumpbin-headers.png)

![dumpbin/loadconfig 的輸出](images/cfg-dumpbin-loadconfig.png)

## <a name="how-does-cfg-really-work"></a><span data-ttu-id="1f539-133">CFG 真正的運作方式為何？</span><span class="sxs-lookup"><span data-stu-id="1f539-133">How Does CFG Really Work?</span></span>

<span data-ttu-id="1f539-134">軟體弱點通常是藉由將不太可能、不尋常或極端的資料提供給執行中的程式而遭到惡意探索。</span><span class="sxs-lookup"><span data-stu-id="1f539-134">Software vulnerabilities are often exploited by providing unlikely, unusual, or extreme data to a running program.</span></span> <span data-ttu-id="1f539-135">例如，攻擊者可以藉由提供比預期更多的程式輸入，來利用緩衝區溢位弱點，藉此將程式所保留的區域保留以保留回應。</span><span class="sxs-lookup"><span data-stu-id="1f539-135">For example, an attacker can exploit a buffer overflow vulnerability by providing more input to a program than expected, thereby over-running the area reserved by the program to hold a response.</span></span> <span data-ttu-id="1f539-136">這可能會損毀可能保存函式指標的相鄰記憶體。</span><span class="sxs-lookup"><span data-stu-id="1f539-136">This could corrupt adjacent memory that may hold a function pointer.</span></span> <span data-ttu-id="1f539-137">當程式呼叫這個函式時，它可能會跳到攻擊者指定的非預期位置。</span><span class="sxs-lookup"><span data-stu-id="1f539-137">When the program calls through this function it may then jump to an unintended location specified by the attacker.</span></span>

<span data-ttu-id="1f539-138">不過，強大的編譯和執行時間支援組合，可實現控制流程完整性，以嚴格限制間接呼叫指示的執行位置。</span><span class="sxs-lookup"><span data-stu-id="1f539-138">However, a potent combination of compile and run-time support from CFG implements control flow integrity that tightly restricts where indirect call instructions can execute.</span></span>

<span data-ttu-id="1f539-139">編譯器會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="1f539-139">The compiler does the following:</span></span>

1.  <span data-ttu-id="1f539-140">將輕量安全性檢查新增至已編譯的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1f539-140">Adds lightweight security checks to the compiled code.</span></span>
2.  <span data-ttu-id="1f539-141">識別應用程式中的函式集合，這些函數是間接呼叫的有效目標。</span><span class="sxs-lookup"><span data-stu-id="1f539-141">Identifies the set of functions in the application that are valid targets for indirect calls.</span></span>

<span data-ttu-id="1f539-142">Windows 核心提供的執行時間支援：</span><span class="sxs-lookup"><span data-stu-id="1f539-142">The runtime support, provided by the Windows kernel:</span></span>

1.  <span data-ttu-id="1f539-143">有效率地維護識別有效間接呼叫目標的狀態。</span><span class="sxs-lookup"><span data-stu-id="1f539-143">Efficiently maintains state that identifies valid indirect call targets.</span></span>
2.  <span data-ttu-id="1f539-144">執行驗證間接呼叫目標是否有效的邏輯。</span><span class="sxs-lookup"><span data-stu-id="1f539-144">Implements the logic that verifies that an indirect call target is valid.</span></span>

<span data-ttu-id="1f539-145">說明：</span><span class="sxs-lookup"><span data-stu-id="1f539-145">To illustrate:</span></span>

![cfg 虛擬虛擬](images/cfg-pseudocode.jpg)

<span data-ttu-id="1f539-147">當 CFG 檢查在執行時間失敗時，Windows 會立即終止程式，進而中斷任何嘗試間接呼叫無效位址的惡意探索。</span><span class="sxs-lookup"><span data-stu-id="1f539-147">When a CFG check fails at runtime, Windows immediately terminates the program, thus breaking any exploit that attempts to indirectly call an invalid address.</span></span>

 

 
