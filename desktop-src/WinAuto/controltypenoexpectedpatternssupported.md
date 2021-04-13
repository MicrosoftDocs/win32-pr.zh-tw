---
title: ControlTypeNoExpectedPatternsSupported
description: ControlTypeNoExpectedPatternsSupported
ms.assetid: 2C9CEFEA-8207-47A7-B100-A56CFBFB792D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c40f9f094589b312a033d6bdadf3fbf3b5020b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300999"
---
# <a name="controltypenoexpectedpatternssupported"></a><span data-ttu-id="5510f-103">ControlTypeNoExpectedPatternsSupported</span><span class="sxs-lookup"><span data-stu-id="5510f-103">ControlTypeNoExpectedPatternsSupported</span></span>

## <a name="text"></a><span data-ttu-id="5510f-104">Text</span><span class="sxs-lookup"><span data-stu-id="5510f-104">Text</span></span>

<span data-ttu-id="5510f-105">ControlType 為的元素 {0} 應至少支援下列其中一個模式： {1} 但此元素不會</span><span class="sxs-lookup"><span data-stu-id="5510f-105">Element with a ControlType of {0} should support at least one of these patterns:{1} but this element does not</span></span>

## <a name="type"></a><span data-ttu-id="5510f-106">類型</span><span class="sxs-lookup"><span data-stu-id="5510f-106">Type</span></span>

<span data-ttu-id="5510f-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="5510f-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="5510f-108">描述</span><span class="sxs-lookup"><span data-stu-id="5510f-108">Description</span></span>

<span data-ttu-id="5510f-109">專案的消費者介面自動化支援不符合消費者介面自動化規格，因為元素至少應支援其中一個提供的控制項模式清單，但不符合。</span><span class="sxs-lookup"><span data-stu-id="5510f-109">The element's UI Automation support does not comply with the UI Automation specification because the element should support at least one of the provided list of control patterns, but does not.</span></span> <span data-ttu-id="5510f-110">如此一來，這個元素可能無法正確地公開給輔助技術，這對使用者體驗可能會有嚴重的影響。</span><span class="sxs-lookup"><span data-stu-id="5510f-110">As a result, this element might not be properly exposed to assistive technologies, which could have a serious impact on user experience.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="5510f-111">可能的原因</span><span class="sxs-lookup"><span data-stu-id="5510f-111">Possible causes</span></span>

-   <span data-ttu-id="5510f-112">不完整的消費者介面自動化執行。</span><span class="sxs-lookup"><span data-stu-id="5510f-112">Incomplete UI Automation implementation.</span></span>
-   <span data-ttu-id="5510f-113">未正確設定 ControlType 屬性。</span><span class="sxs-lookup"><span data-stu-id="5510f-113">The ControlType property is not set correctly.</span></span>

## <a name="remarks"></a><span data-ttu-id="5510f-114">備註</span><span class="sxs-lookup"><span data-stu-id="5510f-114">Remarks</span></span>

<span data-ttu-id="5510f-115">AccChecker 會針對不定的進度列記錄這個錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="5510f-115">AccChecker logs this error message for an indeterminate progress bar.</span></span> <span data-ttu-id="5510f-116">您可以忽略此訊息及/或將它新增至隱藏清單。</span><span class="sxs-lookup"><span data-stu-id="5510f-116">You can ignore this message and/or add it to the suppressions list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5510f-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="5510f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5510f-118">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5510f-118">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="5510f-119">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="5510f-119">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="5510f-120">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="5510f-120">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




