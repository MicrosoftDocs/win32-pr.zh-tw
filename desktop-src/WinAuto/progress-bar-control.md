---
title: '進度列控制項 (MSAA UI 元素參考) '
description: 進度列控制項指出冗長作業的進度，例如從網際網路下載檔案。 通常進度會以從零 (0) 到 100 (100) 的百分比表示。
ms.assetid: 9165d00e-b3f3-41cd-812c-cd39313460fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9bbd9a648ee1c4d4f112577c8e41a5983f69038
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183874"
---
# <a name="progress-bar-control-msaa-ui-element-reference"></a><span data-ttu-id="7dc8d-104">進度列控制項 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="7dc8d-104">Progress Bar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="7dc8d-105">本主題說明 MSAA UI 元素參考的 **進度列控制項** 物件。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-105">This topic describes **Progress Bar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="7dc8d-106">此處未說明如何在各種 UI 架構中建立 **進度列控制項** 物件。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-106">How to create **Progress Bar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="7dc8d-107">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="7dc8d-108">進度列控制項指出冗長作業的進度，例如從網際網路下載檔案。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-108">Progress bar controls indicate the progress of a lengthy operation such as downloading a file from the Internet.</span></span> <span data-ttu-id="7dc8d-109">通常進度會以從零 (0) 到 100 (100) 的百分比表示。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-109">Usually the progress is expressed as a percentage from zero (0) to one hundred (100).</span></span>

<span data-ttu-id="7dc8d-110">進度列控制項的視窗類別名稱是進度 \_ 類別，在 Commctrl 中定義為「msctls \_ 進度」。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-110">The window class name for a progress bar control is PROGRESS\_CLASS, which is defined as "msctls\_progress" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="7dc8d-111">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="7dc8d-111">IAccessible Methods</span></span>

<span data-ttu-id="7dc8d-112">進度列控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="7dc8d-112">Progress bar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="7dc8d-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="7dc8d-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="7dc8d-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="7dc8d-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="7dc8d-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="7dc8d-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="7dc8d-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="7dc8d-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="7dc8d-117">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="7dc8d-117">IAccessible Properties</span></span>

<span data-ttu-id="7dc8d-118">進度列控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="7dc8d-118">Progress bar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="7dc8d-119">屬性</span><span class="sxs-lookup"><span data-stu-id="7dc8d-119">Property</span></span>                                                                             | <span data-ttu-id="7dc8d-120">註解</span><span class="sxs-lookup"><span data-stu-id="7dc8d-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7dc8d-121">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="7dc8d-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="7dc8d-122">**ChildCount** 屬性為零。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-122">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="7dc8d-123">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="7dc8d-123">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="7dc8d-124">**取得 \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="7dc8d-124">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="7dc8d-125">**KeyboardShortcut** 屬性是進度列的存取金鑰，在進度列的標籤文字中是加上底線的字元。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-125">The **KeyboardShortcut** property is the progress bar's access key, which is an underlined character in the text of the label for the progress bar.</span></span> <span data-ttu-id="7dc8d-126">傳回的字串包含附加至字串 "Alt +" 的存取金鑰字元。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-126">The returned string contains the access key character appended to the string "Alt+".</span></span>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="7dc8d-127">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="7dc8d-127">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="7dc8d-128">**Name** 屬性是靜態文字控制項中的文字，會標記進度列。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-128">The **Name** property is the text from a static text control that labels the progress bar.</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="7dc8d-129">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="7dc8d-129">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="7dc8d-130">**父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-130">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7dc8d-131">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="7dc8d-131">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="7dc8d-132">**Role** 屬性為 [**role \_ SYSTEM \_ PROGRESSBAR**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-132">The **Role** property is [**ROLE\_SYSTEM\_PROGRESSBAR**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="7dc8d-133">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="7dc8d-133">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="7dc8d-134">**State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="7dc8d-134">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |
| [<span data-ttu-id="7dc8d-135">**取得 \_ accValue**</span><span class="sxs-lookup"><span data-stu-id="7dc8d-135">**get\_accValue**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | <span data-ttu-id="7dc8d-136">**值** 屬性是從 "0%" 到 "100%" 的字串，可描述進度。</span><span class="sxs-lookup"><span data-stu-id="7dc8d-136">The **Value** property is a string from "0%" to "100%" that describes the progress.</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="7dc8d-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="7dc8d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dc8d-138">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="7dc8d-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





