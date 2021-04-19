---
description: Debug 和 trace 設備和 Windows 通訊端2。
ms.assetid: eb29fc21-92d6-4471-860a-fd1c531686f6
title: Debug 和 Trace 設備
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7288c6b4d72a7a375ee16da23a25b0a04a46df91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970171"
---
# <a name="debug-and-trace-facilities"></a><span data-ttu-id="4eb41-103">Debug 和 Trace 設備</span><span class="sxs-lookup"><span data-stu-id="4eb41-103">Debug and Trace Facilities</span></span>

<span data-ttu-id="4eb41-104">Windows 通訊端2應用程式開發人員需要隔離錯誤：</span><span class="sxs-lookup"><span data-stu-id="4eb41-104">Windows Sockets 2 application developers need to isolate bugs in:</span></span>

-   <span data-ttu-id="4eb41-105">應用程式。</span><span class="sxs-lookup"><span data-stu-id="4eb41-105">The application.</span></span>
-   <span data-ttu-id="4eb41-106">*Ws2 \_32.dll* 或其中一個相容性填充碼 dll。</span><span class="sxs-lookup"><span data-stu-id="4eb41-106">The *Ws2\_32.dll* or one of the compatibility shim DLLs.</span></span>
-   <span data-ttu-id="4eb41-107">服務提供者。</span><span class="sxs-lookup"><span data-stu-id="4eb41-107">The service provider.</span></span>

<span data-ttu-id="4eb41-108">Windows 通訊端2透過數個元件和功能來解決這項需求：</span><span class="sxs-lookup"><span data-stu-id="4eb41-108">Windows Sockets 2 addresses this need through several components and features:</span></span>

-   <span data-ttu-id="4eb41-109">在 Windows Vista 和更新版本上對 Winsock 追蹤的整合支援。</span><span class="sxs-lookup"><span data-stu-id="4eb41-109">Integrated support for Winsock tracing on Windows Vista and later.</span></span>
-   <span data-ttu-id="4eb41-110">在 Windows Vista 上， *Ws2 \_32.dll* 特別設計的 debug 版。</span><span class="sxs-lookup"><span data-stu-id="4eb41-110">A specially devised debug version of the *Ws2\_32.dll* on Windows Vista.</span></span>
-   <span data-ttu-id="4eb41-111">用於 Windows Server 2003 和 Windows XP 的個別基本 debug 和 trace 設備。</span><span class="sxs-lookup"><span data-stu-id="4eb41-111">A separate primitive debug and trace facility for use on Windows Server 2003 and Windows XP.</span></span>

## <a name="winsock-tracing-using-event-tracing-for-windows"></a><span data-ttu-id="4eb41-112">使用 Windows 事件追蹤的 Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="4eb41-112">Winsock Tracing using Event Tracing for Windows</span></span>

<span data-ttu-id="4eb41-113">Windows Vista 及更新版本中包含了使用 Windows 事件追蹤 (ETW) 的對 Winsock 追蹤的整合支援。</span><span class="sxs-lookup"><span data-stu-id="4eb41-113">Integrated support for Winsock tracing using Event Tracing for Windows (ETW) is included on Windows Vista and later.</span></span> <span data-ttu-id="4eb41-114">這是在 Windows Vista 和更新版本上追蹤 Winsock 呼叫的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="4eb41-114">This is the preferred method for tracing Winsock calls on Windows Vista and later.</span></span> <span data-ttu-id="4eb41-115">使用 ETW 的 Winsock 追蹤很輕量，且適用于 Windows 的零售版本。</span><span class="sxs-lookup"><span data-stu-id="4eb41-115">Winsock tracing using ETW is lightweight and works on retail versions of Windows.</span></span> <span data-ttu-id="4eb41-116">不需要額外的軟體或元件。</span><span class="sxs-lookup"><span data-stu-id="4eb41-116">No additional software or components are required.</span></span> <span data-ttu-id="4eb41-117">這項功能只需要在 Windows Vista 和更新版本上啟用。</span><span class="sxs-lookup"><span data-stu-id="4eb41-117">This feature just needs to be enabled on Windows Vista and later.</span></span> <span data-ttu-id="4eb41-118">如需詳細資訊，請參閱 [Winsock 追蹤](winsock-tracing.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="4eb41-118">For more detailed information, see the [Winsock Tracing](winsock-tracing.md) topics.</span></span>

## <a name="using-a-debug-version-of-ws2_32dll"></a><span data-ttu-id="4eb41-119">使用 Ws232.dll 的偵錯工具版本 \_</span><span class="sxs-lookup"><span data-stu-id="4eb41-119">Using a Debug Version of Ws2\_32.dll</span></span>

<span data-ttu-id="4eb41-120">在 Windows Vista 和 Winsock 追蹤上， *Ws2 \_32.dll* 的偵錯工具組合，可讓您監視 windows 通訊端 2 API 或 SPI 之間的所有程序呼叫，並進行控制。</span><span class="sxs-lookup"><span data-stu-id="4eb41-120">The combination of a debug version of the *Ws2\_32.dll* on Windows Vista and Winsock tracing allows all procedure calls across the Windows Sockets 2 API or SPI to be monitored and, to some extent, controlled.</span></span>

<span data-ttu-id="4eb41-121">如果已將適用于 Windows Vista 的 Microsoft Windows 軟體開發套件 (SDK) 版本安裝到預設位置，則適用于各種架構的 *Ws2 \_32.dll* debug 版本位於下列資料夾底下：</span><span class="sxs-lookup"><span data-stu-id="4eb41-121">If a version of the Microsoft Windows Software Development Kit (SDK) for Windows Vista is installed to the default location, debug versions of the *Ws2\_32.dll* for various architectures are located under the following folder:</span></span>

<span data-ttu-id="4eb41-122">**C： \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 \\ NoRedist**</span><span class="sxs-lookup"><span data-stu-id="4eb41-122">**C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\NoRedist**</span></span>

<span data-ttu-id="4eb41-123">*Ws2 \_32.dll* 的已檢查版本，應使用符合您要測試的 Windows 版本和 Service Pack。</span><span class="sxs-lookup"><span data-stu-id="4eb41-123">A checked version of the *Ws2\_32.dll* that matches the version of Windows and the Service Pack you are testing on should be used.</span></span> <span data-ttu-id="4eb41-124">請注意，可能已套用安全性修補程式，以更新您測試系統上的 *Ws2 \_32.dll* 。</span><span class="sxs-lookup"><span data-stu-id="4eb41-124">Be aware that security patches may have been applied that updated the *Ws2\_32.dll* on your test system.</span></span> <span data-ttu-id="4eb41-125">Windows Vista 和舊版平臺軟體發展工具組的 Windows SDK (SDK) DVD/CD 訂用帳戶包含適用于各種 Windows 版本的已檢查組建。</span><span class="sxs-lookup"><span data-stu-id="4eb41-125">The Windows SDK for Windows Vista and the earlier Platform Software Development Kit (SDK) DVD/CD subscriptions include checked builds for the various versions of Windows.</span></span> <span data-ttu-id="4eb41-126">您應使用相同的 *Ws2 \_32.dll* 檢查版本，做為要測試之系統上所使用的零售版本。</span><span class="sxs-lookup"><span data-stu-id="4eb41-126">You should use the same checked version of the *Ws2\_32.dll* as the retail version that was used on the system being tested.</span></span> <span data-ttu-id="4eb41-127">另外也請注意，在已檢查的組建下執行的行為，不會與使用零售組建執行的行為相同。</span><span class="sxs-lookup"><span data-stu-id="4eb41-127">Note also that behavior running under a checked build will not be the same as running with a retail build.</span></span>

<span data-ttu-id="4eb41-128">**注意**  Windows Server 2008 和更新版本的 Windows SDK 不再包含 *Ws2 \_32.dll* 的特殊偵錯工具版本。</span><span class="sxs-lookup"><span data-stu-id="4eb41-128">**Note**  The Windows SDK for Windows Server 2008 and later no longer includes special debug versions of the *Ws2\_32.dll*.</span></span> <span data-ttu-id="4eb41-129">開發人員應該改用使用 ETW 的 Winsock 追蹤，因為這項功能不需要 debug 組建。</span><span class="sxs-lookup"><span data-stu-id="4eb41-129">Developers should use Winsock tracing using ETW instead, since this feature does not require debug builds.</span></span>

## <a name="winsock-debug-and-trace-facility-on-windows-server-2003-and-windows-xp"></a><span data-ttu-id="4eb41-130">Windows Server 2003 和 Windows XP 上的 Winsock 調試和追蹤功能</span><span class="sxs-lookup"><span data-stu-id="4eb41-130">Winsock Debug and Trace Facility on Windows Server 2003 and Windows XP</span></span>

<span data-ttu-id="4eb41-131">舊版 Windows Windows 8 之前的版本和 Windows Server 2012 支援個別的基本偵錯工具和追蹤功能，此功能包含在 Windows SDK 和舊版平臺 SDK 的範例中。</span><span class="sxs-lookup"><span data-stu-id="4eb41-131">Older versions of Windows prior to Windows 8 and Windows Server 2012 support a separate primitive debug and trace facility that is included as a sample with the Windows SDK and the older Platform SDK.</span></span> <span data-ttu-id="4eb41-132">只有在不支援 Winsock 追蹤的 Windows Server 2003 和 Windows XP 上，才應該使用 debug/trace 設備。</span><span class="sxs-lookup"><span data-stu-id="4eb41-132">The debug/trace facility should only be used on Windows Server 2003 and Windows XP where Winsock tracing is not supported.</span></span>

<span data-ttu-id="4eb41-133">如果將 Windows 7 的 Windows SDK 安裝到預設位置，則會在下列資料夾中安裝這個基本的 Winsock 追蹤功能：</span><span class="sxs-lookup"><span data-stu-id="4eb41-133">If the Windows SDK for Windows 7 is installed to the default location, this primitive Winsock tracing feature is installed in the following folder:</span></span>

<span data-ttu-id="4eb41-134">**C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ NetDs \\ winsock \\ dt \_ dll**</span><span class="sxs-lookup"><span data-stu-id="4eb41-134">**C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\winsock\\dt\_dll**</span></span>

<span data-ttu-id="4eb41-135">此資料夾中的 *DbgSpec.doc* 檔案提供此基本追蹤設備的相關檔。</span><span class="sxs-lookup"><span data-stu-id="4eb41-135">The *DbgSpec.doc* file in this folder provides documentation on this primitive trace facility.</span></span> <span data-ttu-id="4eb41-136">您必須編譯 dt dll 資料夾中的範例程式碼 \_ ，才能使用此功能。</span><span class="sxs-lookup"><span data-stu-id="4eb41-136">The sample code in the dt\_dll folder needs to be compiled to use this facility.</span></span> <span data-ttu-id="4eb41-137">開發人員可自由使用原始程式碼開發符合其特定需求的 debug/trace DLL 版本。</span><span class="sxs-lookup"><span data-stu-id="4eb41-137">Developers are free to use the source code to develop versions of the debug/trace DLL that meet their specific needs.</span></span>

<span data-ttu-id="4eb41-138">請注意，這個基本的 Winsock 追蹤功能只適用于已安裝之 *Ws2 \_32.dll* 的偵錯工具版本。</span><span class="sxs-lookup"><span data-stu-id="4eb41-138">Note that this primitive Winsock trace feature will only work with the debug version of *Ws2\_32.dll* installed.</span></span> <span data-ttu-id="4eb41-139">因此您必須取得 *Ws2 \_32.dll* 的已檢查版本，使其符合您要測試的 Windows 版本和 Service Pack。</span><span class="sxs-lookup"><span data-stu-id="4eb41-139">So you will need to get a checked version of the *Ws2\_32.dll* that matches the version of Windows and the Service Pack you are testing on.</span></span>

<span data-ttu-id="4eb41-140">此基本 dt \_ dll 追蹤工具的限制在於，範例程式碼會針對每個 Winsock 函式呼叫使用全域鎖定 (重要區段) 。</span><span class="sxs-lookup"><span data-stu-id="4eb41-140">A limitation of this primitive dt\_dll trace facility is that the sample code uses a global lock (critical section) for each Winsock function call.</span></span> <span data-ttu-id="4eb41-141">這樣一來，這項功能就不太適合用來處理競爭情形。</span><span class="sxs-lookup"><span data-stu-id="4eb41-141">So this facility is not useful in dealing with race conditions.</span></span> <span data-ttu-id="4eb41-142">您必須大幅重新撰寫範例程式碼，以使此追蹤設備適用于處理最真正的 Winsock 問題， (取代全域鎖定) 。</span><span class="sxs-lookup"><span data-stu-id="4eb41-142">The sample code would need to be substantially rewritten to make this trace facility useful for dealing with most real Winsock problems (replacing the global locks).</span></span> <span data-ttu-id="4eb41-143">此範例程式碼可讓開發人員追蹤程序呼叫、程式傳回、參數值和傳回值。</span><span class="sxs-lookup"><span data-stu-id="4eb41-143">This sample code does allow developers to trace the procedure calls, procedure returns, parameter values, and return values.</span></span>

<span data-ttu-id="4eb41-144">開發人員可以使用這個基本機制來追蹤程序呼叫、程式傳回、參數值和傳回值。</span><span class="sxs-lookup"><span data-stu-id="4eb41-144">Developers can use this primitive mechanism to trace procedure calls, procedure returns, parameter values, and return values.</span></span> <span data-ttu-id="4eb41-145">在程序呼叫或程式傳回時，可以改變參數值和傳回值。</span><span class="sxs-lookup"><span data-stu-id="4eb41-145">Parameter values and return values can be altered on procedure call or procedure return.</span></span> <span data-ttu-id="4eb41-146">如有需要，可以防止或重新導向程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="4eb41-146">If desired, a procedure call can be prevented or redirected.</span></span> <span data-ttu-id="4eb41-147">藉由存取此層級的資訊和控制，開發人員可以更妥善地找出應用程式、 *Ws2 \_32.dll* 或服務提供者的問題。</span><span class="sxs-lookup"><span data-stu-id="4eb41-147">With access to this level of information and control, a developer is better able to isolate a problem in the application, *Ws2\_32.dll*, or service provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4eb41-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="4eb41-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eb41-149">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="4eb41-149">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> </dl>

 

 



