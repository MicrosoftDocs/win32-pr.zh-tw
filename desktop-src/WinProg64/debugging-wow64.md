---
title: 調試 WOW64
description: 在 WOW64 下執行的應用程式可以使用 x86 裝載的偵錯工具或原生偵錯工具來進行調試。
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- WOW64 64 位 Windows 程式設計，偵錯工具
- 偵錯工具 WOW64 64 位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7590b0b4f44f9e1a48a204723fb0652b9c2e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382585"
---
# <a name="debugging-wow64"></a><span data-ttu-id="08aca-105">調試 WOW64</span><span class="sxs-lookup"><span data-stu-id="08aca-105">Debugging WOW64</span></span>

<span data-ttu-id="08aca-106">在 WOW64 下執行的應用程式可以透過兩種方式進行調試：</span><span class="sxs-lookup"><span data-stu-id="08aca-106">Applications running under WOW64 can be debugged two ways:</span></span>

-   <span data-ttu-id="08aca-107">使用 x86 裝載的偵錯工具，例如 NTSD、WinDbg 或 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="08aca-107">Use an x86-hosted debugger such as NTSD, WinDbg, or Visual Studio.</span></span> <span data-ttu-id="08aca-108">32位的 NTSD 已安裝到零售安裝上的% systemroot% \\ syswow64。</span><span class="sxs-lookup"><span data-stu-id="08aca-108">The 32-bit NTSD is installed to %systemroot%\\syswow64 on retail installations.</span></span> <span data-ttu-id="08aca-109">請注意，您可以使用 x86 偵錯工具來對 x86 程式碼進行偵錯工具，但無法使用它來對 WOW64 Thunk 層中的中斷點進行拆解或設定，因為它是64位的原生程式碼。</span><span class="sxs-lookup"><span data-stu-id="08aca-109">Note that x86 debuggers can be used to debug x86 code, but cannot be used to disassemble or set breakpoints within the WOW64 thunk layer because it is 64-bit native code.</span></span>
-   <span data-ttu-id="08aca-110">使用原生偵錯工具，例如 CDB、NTSD 或 WinDbg 以及 WOW64 偵錯工具擴充功能，Wow64exts.dll。</span><span class="sxs-lookup"><span data-stu-id="08aca-110">Use a native debugger such as CDB, NTSD, or WinDbg and the WOW64 debugger extension, Wow64exts.dll.</span></span> <span data-ttu-id="08aca-111">如果原生偵錯工具在處理器為 x86 模式時中斷，偵錯工具會以 x86 進程的形式呈現進程。</span><span class="sxs-lookup"><span data-stu-id="08aca-111">If the native debugger breaks while the processor is in x86 mode, the debugger presents the process as an x86 process.</span></span> <span data-ttu-id="08aca-112">如果處理器處於原生模式中，偵錯工具會以原生模式呈現進程。</span><span class="sxs-lookup"><span data-stu-id="08aca-112">If the processor is in native mode, the debugger presents the process as native.</span></span>

<span data-ttu-id="08aca-113">適用于 Windows 的偵錯工具中包含了 CDB、NTSD 和 WinDbg。</span><span class="sxs-lookup"><span data-stu-id="08aca-113">CDB, NTSD, and WinDbg are included in Debugging Tools for Windows.</span></span> <span data-ttu-id="08aca-114">如需詳細資訊，請參閱 [Windows 的偵錯工具](/windows-hardware/drivers/debugger/) 檔。</span><span class="sxs-lookup"><span data-stu-id="08aca-114">For more information, see the [Debugging Tools for Windows](/windows-hardware/drivers/debugger/) documentation.</span></span>

<span data-ttu-id="08aca-115">Wow64exts 偵錯工具擴充功能與 WinDbg 一起安裝。</span><span class="sxs-lookup"><span data-stu-id="08aca-115">The Wow64exts debugger extension is installed with WinDbg.</span></span> <span data-ttu-id="08aca-116">使用！ load wow64exts 命令載入偵錯工具擴充功能。</span><span class="sxs-lookup"><span data-stu-id="08aca-116">Use the !load wow64exts command to load the debugger extension.</span></span> <span data-ttu-id="08aca-117">下表列出！ wow64exts 偵錯工具延伸模組命令。</span><span class="sxs-lookup"><span data-stu-id="08aca-117">The following table lists the !wow64exts debugger extension commands.</span></span>



| <span data-ttu-id="08aca-118">命令</span><span class="sxs-lookup"><span data-stu-id="08aca-118">Command</span></span>                | <span data-ttu-id="08aca-119">描述</span><span class="sxs-lookup"><span data-stu-id="08aca-119">Description</span></span>                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08aca-120">！ wow64exts sw</span><span class="sxs-lookup"><span data-stu-id="08aca-120">!wow64exts.sw</span></span>          | <span data-ttu-id="08aca-121">在 x86 和原生模式之間切換。</span><span class="sxs-lookup"><span data-stu-id="08aca-121">Switches between x86 and native mode.</span></span>                                                                                                    |
| <span data-ttu-id="08aca-122">！ wow64exts 的 *計數*</span><span class="sxs-lookup"><span data-stu-id="08aca-122">!wow64exts.k *count*</span></span>   | <span data-ttu-id="08aca-123">傾印結合的32位/64 位堆疊追蹤。</span><span class="sxs-lookup"><span data-stu-id="08aca-123">Dumps a combined 32-bit/64-bit stack trace.</span></span> <span data-ttu-id="08aca-124">如果指定 *count* ，此命令會傾印每個堆疊追蹤中的第一個 *計數* 位址。</span><span class="sxs-lookup"><span data-stu-id="08aca-124">If *count* is specified, the command dumps the first *count* addresses in each stack trace.</span></span>  |
| <span data-ttu-id="08aca-125">！ wow64exts.info</span><span class="sxs-lookup"><span data-stu-id="08aca-125">!wow64exts.info</span></span>        | <span data-ttu-id="08aca-126">傾印程式 PEB 的基本資訊、目前線程的 TEB，以及 WOW64 所使用的執行緒區域儲存 (TLS) 位置。</span><span class="sxs-lookup"><span data-stu-id="08aca-126">Dumps basic information about the PEB of the process, the TEB of the current thread, and thread local storage (TLS) slots used by WOW64.</span></span> |
| <span data-ttu-id="08aca-127">！ wow64exts。 r *位址*</span><span class="sxs-lookup"><span data-stu-id="08aca-127">!wow64exts.r *address*</span></span> | <span data-ttu-id="08aca-128">傾印指定位址的內容。</span><span class="sxs-lookup"><span data-stu-id="08aca-128">Dumps context for the specified address.</span></span> <span data-ttu-id="08aca-129">如果未指定 *address* ，命令會傾印處理器的內容。</span><span class="sxs-lookup"><span data-stu-id="08aca-129">If *address* is not specified, the command dumps context for the processor.</span></span>                     |



 

 

 