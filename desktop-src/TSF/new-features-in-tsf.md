---
title: TSF 中的新功能
description: 隨著 Microsoft WindowsXP Service Pack 1 的推出，文字服務架構 (TSF) 有數項新功能。
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- 文字服務架構 (TSF) 、新功能
- TSF (文字服務架構) 、新功能
- 文字服務，新功能
- 啟用 TSF 的應用程式，新功能
- 文字服務架構 (TSF) ，advanced support
- TSF (文字服務架構) ，advanced support
- 文字服務，advanced support
- 啟用 TSF 的應用程式，advanced support
- 文字服務架構 (TSF) 、Rich Edit
- TSF (文字服務架構) 、Rich Edit
- 文字服務，Rich Edit
- 啟用 TSF 的應用程式，Rich Edit
- Rich Edit
- 文字服務架構 (TSF) ，安全性
- TSF (文字服務架構) ，安全性
- 文字服務，安全性
- 啟用 TSF 的應用程式，安全性
- TSF 的安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a345087304be638be93fa352845cdd468bf15
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375500"
---
# <a name="new-features-in-tsf"></a><span data-ttu-id="4b132-121">TSF 中的新功能</span><span class="sxs-lookup"><span data-stu-id="4b132-121">New Features in TSF</span></span>

<span data-ttu-id="4b132-122">隨著 Microsoft WindowsXP Service Pack 1 的推出，文字服務架構 (TSF) 有數項新功能。</span><span class="sxs-lookup"><span data-stu-id="4b132-122">With the release of Microsoft WindowsXP Service Pack1, Text Services Framework (TSF) has several new features.</span></span>

## <a name="extended-support-of-advanced-text-services"></a><span data-ttu-id="4b132-123">Advanced Text Services 的延伸支援</span><span class="sxs-lookup"><span data-stu-id="4b132-123">Extended Support of Advanced Text Services</span></span>

<span data-ttu-id="4b132-124">TSF 和 Windows 已新增支援，可為整個桌面的所有應用程式提供一致的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="4b132-124">Support has been added to TSF and Windows to provide a consistent user interface for all applications across the desktop.</span></span> <span data-ttu-id="4b132-125">這項新的支援可讓不知道 TSF 的繼承應用程式或控制項充分利用一些 advanced text services。</span><span class="sxs-lookup"><span data-stu-id="4b132-125">This new support enables legacy applications or controls that are not aware of TSF to take advantage of some advanced text services for free.</span></span> <span data-ttu-id="4b132-126">例如，您現在可以在任何應用程式中，使用語音聽寫和手寫將文字輸入檔。</span><span class="sxs-lookup"><span data-stu-id="4b132-126">For example, speech dictation and handwriting can now be used to enter text into a document in any application.</span></span>

<span data-ttu-id="4b132-127">這項新功能只適用于 WindowsXP Service Pack 1 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4b132-127">This new feature is available only for WindowsXP Service Pack1 or later.</span></span> <span data-ttu-id="4b132-128">預設會關閉它。</span><span class="sxs-lookup"><span data-stu-id="4b132-128">It is turned off by default.</span></span> <span data-ttu-id="4b132-129">若要啟用它，請在 [**地區及語言選項**] 控制台的 [**文字服務] 和 [輸入語言**] 部分中，按一下 [新的 **Advanced** ] 索引標籤中的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="4b132-129">To enable it, click the check box in the new **Advanced** tab in the **Text Services and Input Languages** portion of the **Regional and Language Options** control panel.</span></span>

![在 tsf 控制台中不知道應用程式支援](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a><span data-ttu-id="4b132-131">豐富的編輯支援</span><span class="sxs-lookup"><span data-stu-id="4b132-131">Rich Edit Support</span></span>

<span data-ttu-id="4b132-132">[Microsoft® Rich Edit](../controls/rich-edit-controls.md) 版本4.1 （由應用程式用來以特殊字元和段落格式來查看和編輯文字）現在會公開 TSF 功能。</span><span class="sxs-lookup"><span data-stu-id="4b132-132">[Microsoft® Rich Edit](../controls/rich-edit-controls.md) Version 4.1, used by applications to view and edit text with special character and paragraph formatting, now exposes TSF functionality.</span></span> <span data-ttu-id="4b132-133">預設會關閉這項支援。</span><span class="sxs-lookup"><span data-stu-id="4b132-133">By default this support is turned off.</span></span> <span data-ttu-id="4b132-134">若要啟用 Rich Edit 中的 TSF，裝載應用程式會將特殊的視窗訊息傳送至 Rich Edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="4b132-134">To enable TSF in Rich Edit, a hosting application sends a special window message to the Rich Edit control.</span></span>

## <a name="security-improvements"></a><span data-ttu-id="4b132-135">安全性改善</span><span class="sxs-lookup"><span data-stu-id="4b132-135">Security Improvements</span></span>

<span data-ttu-id="4b132-136">TSF 的安全性和穩定性已大幅改善，可降低惡意程式存取堆疊、堆積或其他安全記憶體位置的可能性。</span><span class="sxs-lookup"><span data-stu-id="4b132-136">The security and robustness of TSF have been substantially improved, to reduce the likelihood of a hostile program being able to access the stack, heap, or other secure memory locations.</span></span> <span data-ttu-id="4b132-137">軟體發展工具組 (SDK) 範例應用程式和文字服務的安全性也已有所改善。</span><span class="sxs-lookup"><span data-stu-id="4b132-137">The security of software development kit (SDK) sample applications and text services has also been improved.</span></span>

 

 