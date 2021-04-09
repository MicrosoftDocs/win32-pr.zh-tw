---
title: UI 自動化規格和社群承諾
description: 消費者介面自動化規格提供 Microsoft 協助工具架構的相關資訊，包括 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化。
ms.assetid: 5fab2d7a-0b1c-4119-b7f4-afdf86db74e7
keywords:
- 消費者介面自動化，規格
- 消費者介面自動化，團體承諾
- 消費者介面自動化的規格
- 消費者介面自動化的社區承諾
- 消費者介面自動化，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d369493fae6bd82f882dc9251df7185be7b862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840851"
---
# <a name="ui-automation-specification-and-community-promise"></a><span data-ttu-id="1d222-108">UI 自動化規格和社群承諾</span><span class="sxs-lookup"><span data-stu-id="1d222-108">UI Automation Specification and Community Promise</span></span>

<span data-ttu-id="1d222-109">消費者介面自動化規格提供 Microsoft 協助工具架構的相關資訊，包括 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化。</span><span class="sxs-lookup"><span data-stu-id="1d222-109">The UI Automation Specification provides information about Microsoft accessibility frameworks, including Microsoft Active Accessibility and Microsoft UI Automation.</span></span> <span data-ttu-id="1d222-110">它會討論每個架構的主要元件、提供設計考慮和範例，並描述執行的需求。</span><span class="sxs-lookup"><span data-stu-id="1d222-110">It discusses each framework's main components, provides design considerations and examples, and describes requirements for implementation.</span></span> <span data-ttu-id="1d222-111">如需詳細資訊，請參閱 [消費者介面自動化規格](ui-automation-specification.md)。</span><span class="sxs-lookup"><span data-stu-id="1d222-111">For more information, see [UI Automation Specification](ui-automation-specification.md).</span></span>

<span data-ttu-id="1d222-112">消費者介面自動化的社區承諾可讓任何人自由執行消費者介面自動化規格，而不需要與 Microsoft 簽訂任何合約。</span><span class="sxs-lookup"><span data-stu-id="1d222-112">The UI Automation Community Promise enables anyone to freely implement the UI Automation Specification without needing to sign any agreements with Microsoft.</span></span> <span data-ttu-id="1d222-113">此外，您也不需要對 Microsoft 的任何提及或任何參考。</span><span class="sxs-lookup"><span data-stu-id="1d222-113">Further, there is no need to make any mention of, or any reference to, Microsoft.</span></span> <span data-ttu-id="1d222-114">如需詳細資訊，請參閱消費者介面自動化的「 [社會承諾](uiauto-specandcommunitypromise.md)」。</span><span class="sxs-lookup"><span data-stu-id="1d222-114">For more information, see [UI Automation Community Promise](uiauto-specandcommunitypromise.md).</span></span>

## <a name="ui-automation-specification"></a><span data-ttu-id="1d222-115">消費者介面自動化規格</span><span class="sxs-lookup"><span data-stu-id="1d222-115">UI Automation Specification</span></span>

<span data-ttu-id="1d222-116">消費者介面自動化規格提供 Microsoft 的協助工具架構的相關資訊，包括 Active Accessibility、消費者介面自動化和消費者介面自動化 Express。</span><span class="sxs-lookup"><span data-stu-id="1d222-116">The UI Automation Specification provides information about Microsoft's accessibility frameworks, including Active Accessibility, UI Automation, and UI Automation Express.</span></span> <span data-ttu-id="1d222-117">它會討論每個架構的主要元件、提供設計考慮和範例，並描述執行的需求。</span><span class="sxs-lookup"><span data-stu-id="1d222-117">It discusses each framework's main components, provides design considerations and examples, and describes requirements for implementation.</span></span>

### <a name="ui-automation-specification-copyright-license"></a><span data-ttu-id="1d222-118">消費者介面自動化規格著作權授權</span><span class="sxs-lookup"><span data-stu-id="1d222-118">UI Automation Specification Copyright License</span></span>

<span data-ttu-id="1d222-119">下列著作權授權適用于消費者介面自動化規格，而且必須包含在消費者介面自動化規格所組成的任何副本中。</span><span class="sxs-lookup"><span data-stu-id="1d222-119">The following copyright license applies to the UI Automation Specification and must be included in any copies that are made of the UI Automation Specification.</span></span> <span data-ttu-id="1d222-120">目前的消費者介面自動化規格可從 Microsoft 下載中心取得。</span><span class="sxs-lookup"><span data-stu-id="1d222-120">The current UI Automation Specification is available on the Microsoft Download Center.</span></span>

### <a name="legal-notice"></a><span data-ttu-id="1d222-121">法律注意事項</span><span class="sxs-lookup"><span data-stu-id="1d222-121">Legal Notice</span></span>

<span data-ttu-id="1d222-122">將本檔的內容複寫、顯示和散佈 (「規格」 ) 的許可權，但在任何情況下都不需要付費或獲得專利，但前提是您在您所進行的所有規格複本（或其部分）上都包含下列通知：</span><span class="sxs-lookup"><span data-stu-id="1d222-122">Permission to copy, display, and distribute the contents of this document (the "Specification"), in any medium for any purpose without fee or royalty is hereby granted, provided that you include the following notice on ALL copies of the Specification, or portions thereof, that you make:</span></span>

<span data-ttu-id="1d222-123">Copyright © Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="1d222-123">Copyright © Microsoft Corporation.</span></span> <span data-ttu-id="1d222-124">著作權所有，並保留一切權利。</span><span class="sxs-lookup"><span data-stu-id="1d222-124">All rights reserved.</span></span> <span data-ttu-id="1d222-125">本檔的複製、顯示和散發的許可權可在 [消費者介面自動化的社會承諾](uiauto-specandcommunitypromise.md)中取得。</span><span class="sxs-lookup"><span data-stu-id="1d222-125">Permission to copy, display, and distribute this document is available at [UI Automation Community Promise](uiauto-specandcommunitypromise.md).</span></span>

<span data-ttu-id="1d222-126">如果您在衍生工作中包含規格的所有必要部分，並提供上述通知，您可能會建立規格的衍生作品。</span><span class="sxs-lookup"><span data-stu-id="1d222-126">You may create derivative works of the Specification, provided that you include all required portions of the Specification in your derivative work, and provide the notice above.</span></span>

<span data-ttu-id="1d222-127">有興趣實行符合消費者介面自動化規格之軟體的當事人，有個別的專利承諾。</span><span class="sxs-lookup"><span data-stu-id="1d222-127">There is a separate patent promise available to parties interested in implementing software that conforms to the UI Automation Specification.</span></span> <span data-ttu-id="1d222-128">此專利授權可在以下位置取得： [消費者介面自動化的社會承諾](uiauto-specandcommunitypromise.md)</span><span class="sxs-lookup"><span data-stu-id="1d222-128">This patent license is available at this location: [UI Automation Community Promise](uiauto-specandcommunitypromise.md)</span></span>

<span data-ttu-id="1d222-129">此規格是以「原樣」提供，Microsoft 不提供任何明示或默示明示或默示明示或默示擔保，包括但不限於適售性、適用于特定用途、非侵權或標題的擔保;規格的內容適用于任何用途;這類內容的執行也不會侵害任何協力廠商專利、著作權、商標或其他權利。</span><span class="sxs-lookup"><span data-stu-id="1d222-129">The Specification is provided "as is" and Microsoft makes no representations or warranties, express or implied, including, but not limited to, warranties of merchantability, fitness for a particular purpose, non-infringement, or title; that the contents of the Specification are suitable for any purpose; nor that the implementation of such contents will not infringe any third-party patents, copyrights, trademarks or other rights.</span></span> <span data-ttu-id="1d222-130">對於任何使用或散發的規格，Microsoft 概不負任何直接、間接、特殊、偶發或衍生的損害。</span><span class="sxs-lookup"><span data-stu-id="1d222-130">Microsoft will not be liable for any direct, indirect, special, incidental or consequential damages arising out of or relating to any use or distribution of the Specification.</span></span>

<span data-ttu-id="1d222-131">Microsoft 的名稱和商標不得以任何方式使用，包括與規格相關的廣告或宣傳或其內容，而不需要特定的先前書面許可。</span><span class="sxs-lookup"><span data-stu-id="1d222-131">The name and trademarks of Microsoft may NOT be used in any manner, including advertising or publicity pertaining to the Specification or its contents without specific, written prior permission.</span></span> <span data-ttu-id="1d222-132">規格中的著作權標題將隨時保留給 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1d222-132">Title to copyright in the Specification will at all times remain with Microsoft.</span></span>

<span data-ttu-id="1d222-133">概無任何以默示、禁止翻供或其他方式授與之權利。</span><span class="sxs-lookup"><span data-stu-id="1d222-133">No other rights are granted by implication, estoppel or otherwise.</span></span>

## <a name="ui-automation-community-promise"></a><span data-ttu-id="1d222-134">消費者介面自動化的社會承諾</span><span class="sxs-lookup"><span data-stu-id="1d222-134">UI Automation Community Promise</span></span>

<span data-ttu-id="1d222-135">Microsoft 無法挽回承諾不要針對您進行任何 Microsoft 必要的宣告，以供您進行銷售、匯入或散發任何實行、匯入或散發任何實行、符合其中一個涵蓋的規格，而且符合該規格的必要部分必要部分的規範， ( 「涵蓋的執行」 ) ，請遵循下列各項：</span><span class="sxs-lookup"><span data-stu-id="1d222-135">Microsoft irrevocably promises not to assert any Microsoft Necessary Claims against you for making, using, selling, offering for sale, importing or distributing any implementation, to the extent it conforms to one of the Covered Specifications, and is compliant with all of the required parts of the mandatory provisions of that specification ("Covered Implementation"), subject to the following:</span></span>

<span data-ttu-id="1d222-136">這是由 Microsoft 直接提供給您的個人承諾，且您已確認為受益的條件，即不會收到來自供應商、轉銷商或其他與此承諾的 Microsoft 權利。</span><span class="sxs-lookup"><span data-stu-id="1d222-136">This is a personal promise directly from Microsoft to you, and you acknowledge as a condition of benefitting from it that no Microsoft rights are received from suppliers, distributors, or otherwise in connection with this promise.</span></span> <span data-ttu-id="1d222-137">如果您在 Microsoft 對任何涵蓋的規格中進行了「簽署、維護或主動參與專利侵權訴訟，則這項個人承諾不適用於任何由您所建立或使用的涵蓋範圍。</span><span class="sxs-lookup"><span data-stu-id="1d222-137">If you file, maintain, or voluntarily participate in a patent infringement lawsuit against a Microsoft implementation of any Covered Specification, then this personal promise does not apply with respect to any Covered Implementation made or used by you.</span></span> <span data-ttu-id="1d222-138">為了清楚說明，「Microsoft 必要宣告」是 Microsoft 所擁有或 Microsoft 控制的專利的宣告，這些都是必要部分的必要部分 (其中也包含詳細描述之涵蓋規格) 的必要元素，而不是僅在涵蓋的規格中參考的部分。</span><span class="sxs-lookup"><span data-stu-id="1d222-138">To clarify, "Microsoft Necessary Claims" are those claims of Microsoft-owned or Microsoft-controlled patents that are necessary to implement the required portions (which also include the required elements of optional portions) of the Covered Specification that are described in detail and not those merely referenced in the Covered Specification.</span></span>

<span data-ttu-id="1d222-139">這項 Microsoft 承諾不保證 (我) 任何 Microsoft 發出的專利索賠涵蓋了涵蓋的實施或可強制執行，或 (ii) 涵蓋的實施不會侵害任何協力廠商的專利或其他智慧財產權。</span><span class="sxs-lookup"><span data-stu-id="1d222-139">This promise by Microsoft is not an assurance that either (i) any of Microsoft's issued patent claims covers a Covered Implementation or are enforceable, or (ii) a Covered Implementation would not infringe patents or other intellectual property rights of any third party.</span></span> <span data-ttu-id="1d222-140">除了這項承諾中明確陳述的其他權利，也應被視為授與、放棄或接收隱含、耗盡、禁止反悔或其他權利。</span><span class="sxs-lookup"><span data-stu-id="1d222-140">No other rights except those expressly stated in this promise shall be deemed granted, waived or received by implication, exhaustion, estoppel, or otherwise.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d222-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d222-141">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1d222-142">**概念**</span><span class="sxs-lookup"><span data-stu-id="1d222-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1d222-143">UI 自動化基礎</span><span class="sxs-lookup"><span data-stu-id="1d222-143">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 




