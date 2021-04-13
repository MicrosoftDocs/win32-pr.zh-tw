---
title: '消費者介面自動化確認 (UIA 確認) '
description: 消費者介面自動化確認 (UIA 確認) 是測試架構，適用于手動和自動化測試 Microsoft 消費者介面自動化的控制項或應用程式的執行。
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- 使用者介面自動化確認
- UIA 確認
- 消費者介面自動化的實作為測試
- 測試消費者介面自動化
- UIA 測試控管
- 消費者介面自動化測試控管
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374614"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a><span data-ttu-id="87fe2-109">協助工具工具-消費者介面自動化確認 (UIA 確認) </span><span class="sxs-lookup"><span data-stu-id="87fe2-109">Accessibility tools - UI Automation Verify (UIA Verify)</span></span>

<span data-ttu-id="87fe2-110">**消費者介面自動化確認 (UIA 確認)** 是測試架構，適用于手動和自動化測試 Microsoft 消費者介面自動化的控制項或應用程式的執行。</span><span class="sxs-lookup"><span data-stu-id="87fe2-110">**UI Automation Verify (UIA Verify)** is a testing framework for manual and automated testing of a control's or application's implementation of Microsoft UI Automation.</span></span> <span data-ttu-id="87fe2-111">測試架構的大部分功能都是來自稱為 WUIATestLibrary.dll 的 DLL。</span><span class="sxs-lookup"><span data-stu-id="87fe2-111">Most of the testing framework's functionality comes from a DLL called WUIATestLibrary.dll.</span></span> <span data-ttu-id="87fe2-112">此 DLL 包含測試特定消費者介面自動化功能的程式碼，也支援記錄測試結果。</span><span class="sxs-lookup"><span data-stu-id="87fe2-112">This DLL contains the code for testing specific UI Automation functionality, and it also supports logging of the test results.</span></span> <span data-ttu-id="87fe2-113">您可以將應用程式整合到測試程式碼中，並定期進行自動化測試或消費者介面自動化案例的點檢查。</span><span class="sxs-lookup"><span data-stu-id="87fe2-113">You can integrate your application into the test code and conduct regular, automated testing or spot checks of your UI Automation scenarios.</span></span>

<span data-ttu-id="87fe2-114">**UIA 確認** 已隨 WINDOWS 軟體開發套件 (SDK) 安裝。</span><span class="sxs-lookup"><span data-stu-id="87fe2-114">**UIA Verify** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="87fe2-115">它位於 \\ \\ < SDK 安裝路徑的 bin *version* > \\ < *platform* > \\ UIAVerify 資料夾中 (VisualUIAVerifyNative.exe) 。</span><span class="sxs-lookup"><span data-stu-id="87fe2-115">It is located in the \\bin\\<*version*>\\<*platform*>\\UIAVerify folder of the SDK installation path (VisualUIAVerifyNative.exe).</span></span>

<span data-ttu-id="87fe2-116">**UIA 驗證** 是由稱為消費者介面自動化測試程式庫的 API，以及稱為 Visual **消費者介面自動化驗證** 的 GUI 介面所組成。</span><span class="sxs-lookup"><span data-stu-id="87fe2-116">**UIA Verify** consists of an API called the UI Automation Test Library, and a GUI interface called Visual **UI Automation Verify**.</span></span> <span data-ttu-id="87fe2-117">以下主題將說明這些情況。</span><span class="sxs-lookup"><span data-stu-id="87fe2-117">These are described in the following topics.</span></span>

> [!NOTE]
> <span data-ttu-id="87fe2-118">**消費者介面自動化 Verify** 是舊版工具。</span><span class="sxs-lookup"><span data-stu-id="87fe2-118">**UI Automation Verify** is a legacy tool.</span></span> <span data-ttu-id="87fe2-119">建議您改為使用 [協助工具深入](https://accessibilityinsights.io/) 解析。</span><span class="sxs-lookup"><span data-stu-id="87fe2-119">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="87fe2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="87fe2-120">Requirements</span></span>

<span data-ttu-id="87fe2-121">消費者介面自動化必須存在於系統上。</span><span class="sxs-lookup"><span data-stu-id="87fe2-121">UI Automation must be present on the system.</span></span> <span data-ttu-id="87fe2-122">如需詳細資訊，請參閱 [消費者介面自動化](entry-uiauto-win32.md)的「需求」一節。</span><span class="sxs-lookup"><span data-stu-id="87fe2-122">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="87fe2-123">**UIA Verify** 會安裝為 Windows SDK 的整體工具組的一部分，而不是以個別下載方式來散發。</span><span class="sxs-lookup"><span data-stu-id="87fe2-123">**UIA Verify** is installed as part of the overall set of tools in the Windows SDK, it is not distributed as a separate download.</span></span> <span data-ttu-id="87fe2-124">Windows SDK 包含本節中記載的所有協助工具相關工具。</span><span class="sxs-lookup"><span data-stu-id="87fe2-124">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="87fe2-125">取得 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="87fe2-125">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="87fe2-126">如果您需要先前的版本， (也有從該頁面連結的 SDK 下載封存。 ) </span><span class="sxs-lookup"><span data-stu-id="87fe2-126">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

<span data-ttu-id="87fe2-127">若要執行 **UIA 確認** 作為視覺化檢視，請在 [bin platform UIAVerify] 資料夾中找出 VisualUIAVerifyNative.exe， \\ \\ <  > \\ 然後執行它 (您通常不需要以系統管理員身分執行) 。</span><span class="sxs-lookup"><span data-stu-id="87fe2-127">To run **UIA Verify** as a visual tool, find VisualUIAVerifyNative.exe in the \\bin\\<*platform*>\\UIAVerify folder and run it (you don't typically have to run as administrator).</span></span> <span data-ttu-id="87fe2-128">如需詳細資訊，請參閱 [Visual 消費者介面自動化驗證](visual-ui-automation-verify.md)。</span><span class="sxs-lookup"><span data-stu-id="87fe2-128">For more information, see [Visual UI Automation Verify](visual-ui-automation-verify.md).</span></span> <span data-ttu-id="87fe2-129">若要使用程式庫，請參閱 [消費者介面自動化測試程式庫](ui-automation-test-library.md)。</span><span class="sxs-lookup"><span data-stu-id="87fe2-129">To use the libraries, see [UI Automation Test Library](ui-automation-test-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="87fe2-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="87fe2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87fe2-131">協助工具事件監控程式</span><span class="sxs-lookup"><span data-stu-id="87fe2-131">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
</dt> <dt>

[<span data-ttu-id="87fe2-132">檢查</span><span class="sxs-lookup"><span data-stu-id="87fe2-132">Inspect</span></span>](inspect-objects.md)
</dt> <dt>

[<span data-ttu-id="87fe2-133">測試控管</span><span class="sxs-lookup"><span data-stu-id="87fe2-133">Testing Tools</span></span>](testing-tools.md)
</dt> <dt>

[<span data-ttu-id="87fe2-134">UI 協助工具檢查程式</span><span class="sxs-lookup"><span data-stu-id="87fe2-134">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




