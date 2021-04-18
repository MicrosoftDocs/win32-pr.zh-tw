---
title: " (Windows Web 服務) 的調試"
description: 一組函式僅適用于 DEBUG 組建，且適用于測試和偵錯工具。
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Windows 的 Web 服務偵錯工具
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106965879"
---
# <a name="debugging-windows-web-services"></a><span data-ttu-id="ff437-106"> (Windows Web 服務) 的調試</span><span class="sxs-lookup"><span data-stu-id="ff437-106">Debugging (Windows Web Services)</span></span>

<span data-ttu-id="ff437-107">一組函式僅適用于 DEBUG 組建，且適用于測試和偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="ff437-107">A set of functions is only available in the DEBUG build, and are intended for testing and debugging.</span></span>


<span data-ttu-id="ff437-108">有一些函式和環境變數僅適用于偵錯工具模式。</span><span class="sxs-lookup"><span data-stu-id="ff437-108">There are a number of functions and environment variables available in the DEBUG mode only.</span></span> <span data-ttu-id="ff437-109">可以用來協助測試和偵測。</span><span class="sxs-lookup"><span data-stu-id="ff437-109">They can be used to help with testing and debugging.</span></span>

-   <span data-ttu-id="ff437-110">設定 WsTimeout = 0 會導致所有的超時都是無限的。</span><span class="sxs-lookup"><span data-stu-id="ff437-110">Setting WsTimeout=0 will cause all timeouts to be INFINITE.</span></span> <span data-ttu-id="ff437-111">當您在時間緊迫的作業期間逐步執行偵錯工具時，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="ff437-111">This is useful when stepping through the debugger during time sensitive operations.</span></span>
-   <span data-ttu-id="ff437-112">設定 WsFailCount 與呼叫 WsSetAutoFail 的效果相同。</span><span class="sxs-lookup"><span data-stu-id="ff437-112">Setting WsFailCount has the same effect as calling WsSetAutoFail.</span></span>
-   <span data-ttu-id="ff437-113">WsFlags 可讓您設定各種旗標來修改執行時間行為。</span><span class="sxs-lookup"><span data-stu-id="ff437-113">WsFlags allows you to set various flags that modify the runtime behavior.</span></span> <span data-ttu-id="ff437-114">語法為 WsFlags = a、b、c。</span><span class="sxs-lookup"><span data-stu-id="ff437-114">The syntax is WsFlags=a,b,c.</span></span> <span data-ttu-id="ff437-115">支援的旗標為 ModifyTimestamp、ModifyInclusivePrefixes、ModifyTimestampDigest、ModifyToHeaderDigest 和 ModifySignatureValue。</span><span class="sxs-lookup"><span data-stu-id="ff437-115">The supported flags are ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest and ModifySignatureValue.</span></span>

<span data-ttu-id="ff437-116">下列函式可用於進行調試：</span><span class="sxs-lookup"><span data-stu-id="ff437-116">The following functions are used with debugging:</span></span>

-   [<span data-ttu-id="ff437-117">**WsDumpMemory**</span><span class="sxs-lookup"><span data-stu-id="ff437-117">**WsDumpMemory**</span></span>](wsdumpmemory.md)
-   [<span data-ttu-id="ff437-118">**WsSetAutoFail**</span><span class="sxs-lookup"><span data-stu-id="ff437-118">**WsSetAutoFail**</span></span>](wssetautofail.md)

 

 




