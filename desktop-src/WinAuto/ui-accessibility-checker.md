---
title: '協助工具工具-AccChecker (UI 協助工具檢查程式) '
description: 描述 AccChecker (UI 協助工具檢查工具) ，此工具可用於測試應用程式的消費者介面自動化或 Microsoft Active Accessibility (MSAA) 執行。
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- UI 協助工具檢查程式
- AccChecker
- 消費者介面自動化的實作為測試
- UIA 實施，測試
- Microsoft Active Accessibility 的實作為測試
- MSAA 執行，測試
- 測試消費者介面自動化
- 測試 UIA
- 測試 Microsoft Active Accessibility
- 測試 MSAA
- UIA 測試控管
- 消費者介面自動化測試控管
- MSAA 測試控管
- Microsoft Active Accessibility 測試控管
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d2b85436735bfa08f8fc73cf4e465b11d71630
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "106996364"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a><span data-ttu-id="ccf5c-117">協助工具工具-AccChecker (UI 協助工具檢查程式) </span><span class="sxs-lookup"><span data-stu-id="ccf5c-117">Accessibility tools - AccChecker (UI Accessibility Checker)</span></span>

<span data-ttu-id="ccf5c-118">**AccChecker** (UI 協助工具檢查工具) 驗證消費者介面自動化 (UIA) 的設計和實行中是否符合重要的 ui 協助工具需求，或 MICROSOFT ACTIVE ACCESSIBILITY (MSAA) ，不論基礎 UI 架構為何。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-118">**AccChecker** (UI Accessibility Checker) verifies that key UI accessibility requirements are met in the design and implementation of UI Automation (UIA) or Microsoft Active Accessibility (MSAA) regardless of the underlying UI framework.</span></span> <span data-ttu-id="ccf5c-119">**AccChecker** 也包含一組 web 協助工具驗證。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-119">**AccChecker** also includes a set of web accessibility verifications.</span></span>

<span data-ttu-id="ccf5c-120">**AccChecker** 提供下列層級的功能：</span><span class="sxs-lookup"><span data-stu-id="ccf5c-120">**AccChecker** provides the following levels of functionality:</span></span>

- <span data-ttu-id="ccf5c-121">支援手動測試、訊息記錄和抑制產生的 Windows GUI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-121">A Windows GUI application that supports manual testing, message logging, and suppression generation.</span></span>
- <span data-ttu-id="ccf5c-122">用於自動化測試架構的 API。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-122">An API for use in automated testing frameworks.</span></span>
- <span data-ttu-id="ccf5c-123">在無法使用 **AccChecker** 受控 API 的情況下，支援非受控測試自動化的主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-123">A console application that supports unmanaged test automations for scenarios where the **AccChecker** managed API can't be used.</span></span>

<span data-ttu-id="ccf5c-124">所有層級的 **AccChecker** 功能都提供用來驗證 Microsoft Active Accessibility 程式設計存取、程式設計事件產生、控制項配置和鍵盤流覽的常式。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-124">All levels of **AccChecker** functionality provide routines for verifying Microsoft Active Accessibility programmatic access, programmatic event generation, control layout, and keyboard navigation.</span></span> <span data-ttu-id="ccf5c-125">**AccChecker** 也提供基本的螢幕讀取器轉譯服務。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-125">**AccChecker** also provides a basic screen reader transcription service.</span></span>

<span data-ttu-id="ccf5c-126">**AccChecker** 會隨 WINDOWS 軟體開發套件 (SDK) 安裝。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-126">**AccChecker** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ccf5c-127">它位於 \\ \\ <  > \\ < SDK 安裝路徑的 bin version *platform* > \\ AccChecker 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-127">It is located in the \\bin\\<*version*>\\<*platform*>\\AccChecker folder of the SDK installation path.</span></span>

> [!NOTE]
> <span data-ttu-id="ccf5c-128">**AccChecker** 是一種舊版工具。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-128">**AccChecker** is a legacy tool.</span></span> <span data-ttu-id="ccf5c-129">建議您改為使用 [協助工具深入](https://accessibilityinsights.io/) 解析。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-129">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf5c-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccf5c-130">Requirements</span></span>

<span data-ttu-id="ccf5c-131">需要 .NET Framework 2.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-131">Requires .NET Framework 2.0 or later.</span></span>

<span data-ttu-id="ccf5c-132">**AccChecker** 可以用來檢查沒有 Microsoft 消費者介面自動化的系統上的協助工具資料，但只能檢查 Microsoft Active Accessibility 屬性。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-132">**AccChecker** can be used to examine accessibility data on systems that don't have Microsoft UI Automation, but can only examine the Microsoft Active Accessibility properties.</span></span> <span data-ttu-id="ccf5c-133">若要檢查消費者介面自動化，消費者介面自動化必須存在於系統上。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-133">To examine UI Automation, UI Automation must be present on the system.</span></span> <span data-ttu-id="ccf5c-134">如需詳細資訊，請參閱 [消費者介面自動化](entry-uiauto-win32.md)的「需求」一節。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-134">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="ccf5c-135">**AccChecker** 會安裝為 windows SDK 中整個工具組的一部分，而不是以個別的 exe 下載方式來散發。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-135">**AccChecker** is installed as part of the overall set of tools in theWindows SDK, it is not distributed as a separate exe download.</span></span> <span data-ttu-id="ccf5c-136">Windows SDK 包含本節中記載的所有協助工具相關工具。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-136">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="ccf5c-137">取得 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="ccf5c-137">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="ccf5c-138">如果您需要先前的版本， (也有從該頁面連結的 SDK 下載封存。 ) </span><span class="sxs-lookup"><span data-stu-id="ccf5c-138">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccf5c-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="ccf5c-139">Related topics</span></span>

- [<span data-ttu-id="ccf5c-140">協助工具事件監控程式</span><span class="sxs-lookup"><span data-stu-id="ccf5c-140">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
- [<span data-ttu-id="ccf5c-141">檢查</span><span class="sxs-lookup"><span data-stu-id="ccf5c-141">Inspect</span></span>](inspect-objects.md)
- [<span data-ttu-id="ccf5c-142">測試控管</span><span class="sxs-lookup"><span data-stu-id="ccf5c-142">Testing Tools</span></span>](testing-tools.md)
- [<span data-ttu-id="ccf5c-143">使用者介面自動化確認</span><span class="sxs-lookup"><span data-stu-id="ccf5c-143">UI Automation Verify</span></span>](ui-automation-verify.md)
