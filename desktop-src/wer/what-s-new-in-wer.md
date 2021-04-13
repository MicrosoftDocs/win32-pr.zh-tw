---
title: WER 的新功能
description: 此頁面摘要說明每個版本 Windows 錯誤報告 (WER) 的新功能。
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Windows 錯誤報告 Windows 錯誤報告，新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526776de3c5f88400e7cfae7ed9b9717318c223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314647"
---
# <a name="whats-new-in-wer"></a><span data-ttu-id="e8d85-104">WER 的新功能</span><span class="sxs-lookup"><span data-stu-id="e8d85-104">What's New in WER</span></span>

<span data-ttu-id="e8d85-105">此頁面摘要說明每個版本 Windows 錯誤報告 (WER) 的新功能。</span><span class="sxs-lookup"><span data-stu-id="e8d85-105">This page summarizes the new features of Windows Error Reporting (WER) for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="e8d85-106">Windows 7 與 Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e8d85-106">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="e8d85-107">下列清單摘要說明適用于 Windows 7 和 Windows Server 2008 R2 的新 WER 功能。</span><span class="sxs-lookup"><span data-stu-id="e8d85-107">The following list summarizes the new WER features for Windows 7 and Windows Server 2008 R2.</span></span>

-   <span data-ttu-id="e8d85-108">新增引發例外狀況的功能，以略過所有例外狀況處理常式，進而立即終止應用程式並叫用 Windows 錯誤報告。</span><span class="sxs-lookup"><span data-stu-id="e8d85-108">Adds the ability to raise an exception that bypasses all exception handlers thus terminating the application immediately and invoking Windows Error Reporting.</span></span> <span data-ttu-id="e8d85-109">如需詳細資訊，請參閱 [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="e8d85-109">For details, see the [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) function.</span></span>
-   <span data-ttu-id="e8d85-110">加入註冊跨進程例外狀況處理常式的功能，當發生損毀時，會呼叫 WER，以收集事件名稱、報告參數和偵錯工具啟動選項。</span><span class="sxs-lookup"><span data-stu-id="e8d85-110">Adds the ability to register an out-of-process exception handler that WER calls when a crash occurs to collect the event name, reporting parameters, and debug launching options.</span></span> <span data-ttu-id="e8d85-111">如需詳細資訊，請參閱 [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) 函數。</span><span class="sxs-lookup"><span data-stu-id="e8d85-111">For details, see the [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) function.</span></span>

<span data-ttu-id="e8d85-112">已新增的函式：</span><span class="sxs-lookup"><span data-stu-id="e8d85-112">Functions that were added:</span></span>

-   [<span data-ttu-id="e8d85-113">**OutOfProcessExceptionEventCallback**</span><span class="sxs-lookup"><span data-stu-id="e8d85-113">**OutOfProcessExceptionEventCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [<span data-ttu-id="e8d85-114">**OutOfProcessExceptionEventSignatureCallback**</span><span class="sxs-lookup"><span data-stu-id="e8d85-114">**OutOfProcessExceptionEventSignatureCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [<span data-ttu-id="e8d85-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span><span class="sxs-lookup"><span data-stu-id="e8d85-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   <span data-ttu-id="e8d85-116">[**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e8d85-116">[**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))</span></span>
-   [<span data-ttu-id="e8d85-117">**WerRegisterRuntimeExceptionModule**</span><span class="sxs-lookup"><span data-stu-id="e8d85-117">**WerRegisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [<span data-ttu-id="e8d85-118">**WerUnregisterRuntimeExceptionModule**</span><span class="sxs-lookup"><span data-stu-id="e8d85-118">**WerUnregisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

<span data-ttu-id="e8d85-119">已新增的結構：</span><span class="sxs-lookup"><span data-stu-id="e8d85-119">Structures that were added:</span></span>

-   [<span data-ttu-id="e8d85-120">**WER \_ 執行時間 \_ 例外狀況 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="e8d85-120">**WER\_RUNTIME\_EXCEPTION\_INFORMATION**</span></span>](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="e8d85-121">Windows Server 2008 和 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="e8d85-121">Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="e8d85-122">下列清單摘要說明 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 之 WER 的新功能。</span><span class="sxs-lookup"><span data-stu-id="e8d85-122">The following list summarizes the new features of WER for Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

-   <span data-ttu-id="e8d85-123">您可以設定 WER，如此一來，使用者模式應用程式損毀時，就會收集完整的使用者模式傾印，並將其儲存在本機上 (應用程式，這些應用程式會自行自訂損毀報告，包括 .NET 應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="e8d85-123">WER can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes (applications that do their own custom crash reporting, including .NET applications are not supported).</span></span> <span data-ttu-id="e8d85-124">如需詳細資訊，請參閱 [收集 User-Mode](collecting-user-mode-dumps.md)傾印。</span><span class="sxs-lookup"><span data-stu-id="e8d85-124">For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="e8d85-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8d85-125">Windows Vista</span></span>

<span data-ttu-id="e8d85-126">下列清單摘要說明適用于 Windows Vista Windows 錯誤報告 (WER) 的新功能：</span><span class="sxs-lookup"><span data-stu-id="e8d85-126">The following list summarizes the new features of Windows Error Reporting (WER) for Windows Vista:</span></span>

-   <span data-ttu-id="e8d85-127">在監視損毀和沒有回應的進程時，已擴充 WER。</span><span class="sxs-lookup"><span data-stu-id="e8d85-127">WER has been extended beyond monitoring crashes and unresponsive processes.</span></span> <span data-ttu-id="e8d85-128">WER 包含許多新的非重大事件種類支援，例如效能問題。</span><span class="sxs-lookup"><span data-stu-id="e8d85-128">WER includes support for many new types of non-critical events, such as performance issues.</span></span> <span data-ttu-id="e8d85-129">這可讓開發人員深入瞭解其客戶所開發之應用程式的體驗。</span><span class="sxs-lookup"><span data-stu-id="e8d85-129">This enables developers to learn more about the experiences their customers have with the applications they have developed.</span></span>
-   <span data-ttu-id="e8d85-130">新函式讓開發人員能夠彈性地建立、自訂和提交問題報表。</span><span class="sxs-lookup"><span data-stu-id="e8d85-130">New functions give developers the flexibility in creating, customizing, and submitting problem reports.</span></span> <span data-ttu-id="e8d85-131">如需詳細資訊，請參閱 [WER 函數](wer-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="e8d85-131">For more information, see [WER Functions](wer-functions.md).</span></span>
-   <span data-ttu-id="e8d85-132">改良的 [Windows 品質線上服務](https://www.microsoft.com/?ref=go) 讓開發人員能夠存取客戶提交給其應用程式的問題資訊，以及提供解決方案給這些客戶的機制。</span><span class="sxs-lookup"><span data-stu-id="e8d85-132">The improved [Windows Quality Online Services](https://www.microsoft.com/?ref=go) provides developers with access to the problem information that customers are submitting for their applications, and a mechanism to deliver solutions to these customers.</span></span>
-   <span data-ttu-id="e8d85-133">[應用程式復原和重新](/windows/desktop/Recovery/application-recovery-and-restart-portal)啟動和[重新開機管理員](/windows/desktop/RstMgr/restart-manager-portal)所引進的功能，可讓應用程式在發生重大失敗時自動復原資訊並重新啟動。</span><span class="sxs-lookup"><span data-stu-id="e8d85-133">The functions introduced by [Application Recovery and Restart](/windows/desktop/Recovery/application-recovery-and-restart-portal) and [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) enable applications to automatically recover information and restart in the event of a critical failure.</span></span> <span data-ttu-id="e8d85-134">開發人員可以在其應用程式中使用這些功能，以大幅改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="e8d85-134">Developers can use these features in their applications to significantly improve their user experience.</span></span>
-   <span data-ttu-id="e8d85-135">**Windows Vista 或 windows 7 上的行動中心的問題報告和解決方案** ，是使用者與 WER 互動的中心位置。</span><span class="sxs-lookup"><span data-stu-id="e8d85-135">**Problem Reports and Solutions on Windows Vista or the Action Center on Windows 7** is the central location for users to interact with WER.</span></span> <span data-ttu-id="e8d85-136">使用者可以檢查是否有新的解決方案、管理報表歷程記錄、查看問題報告的詳細資料，以及管理報告設定，包括讓 WER 自動檢查解決方案，而不會中斷使用者。</span><span class="sxs-lookup"><span data-stu-id="e8d85-136">Users can check for new solutions, manage their reporting history, view the details of a problem report, and manage reporting settings including enabling WER to check for solutions automatically without interrupting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8d85-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8d85-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8d85-138">Windows 錯誤報告</span><span class="sxs-lookup"><span data-stu-id="e8d85-138">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 