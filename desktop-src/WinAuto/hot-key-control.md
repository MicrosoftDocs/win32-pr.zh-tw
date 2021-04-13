---
title: '快速鍵控制 (MSAA UI 元素參考) '
description: 快速鍵控制項可讓使用者輸入按鍵的組合，用來做為快速鍵，讓他們能夠快速執行動作。 快速鍵控制項會顯示使用者輸入的按鍵，並確保使用者選取有效的按鍵組合。
ms.assetid: 56c9fee4-f3d3-4f61-8587-bf80186aa5b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aed12ce64fe25c091f6204d9143a0c6ebefb65a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301596"
---
# <a name="hot-key-control-msaa-ui-element-reference"></a><span data-ttu-id="df3e8-104">快速鍵控制 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="df3e8-104">Hot Key Control (MSAA UI Element Reference)</span></span>

<span data-ttu-id="df3e8-105">快速鍵控制項可讓使用者輸入按鍵的組合，用來做為快速鍵，讓他們能夠快速執行動作。</span><span class="sxs-lookup"><span data-stu-id="df3e8-105">Hot key controls allow users to enter a combination of keystrokes used as a hot key, which enables them to perform an action quickly.</span></span> <span data-ttu-id="df3e8-106">快速鍵控制項會顯示使用者輸入的按鍵，並確保使用者選取有效的按鍵組合。</span><span class="sxs-lookup"><span data-stu-id="df3e8-106">A hot key control displays the keystrokes entered by the user and ensures that the user selects a valid key combination.</span></span>

<span data-ttu-id="df3e8-107">快速鍵控制項的視窗類別名稱是快速鍵 \_ 類別，在 Commctrl 中定義為 "msctls \_ hotkey32"。</span><span class="sxs-lookup"><span data-stu-id="df3e8-107">The window class name for a hot key control is HOTKEY\_CLASS, which is defined as "msctls\_hotkey32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="df3e8-108">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="df3e8-108">IAccessible Methods</span></span>

<span data-ttu-id="df3e8-109">快速鍵控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="df3e8-109">Hot key controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="df3e8-110">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="df3e8-110">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="df3e8-111">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="df3e8-111">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="df3e8-112">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="df3e8-112">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="df3e8-113">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="df3e8-113">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="df3e8-114">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="df3e8-114">IAccessible Properties</span></span>

<span data-ttu-id="df3e8-115">快速鍵控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="df3e8-115">The Hot key controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="df3e8-116">屬性</span><span class="sxs-lookup"><span data-stu-id="df3e8-116">Property</span></span>                                                                             | <span data-ttu-id="df3e8-117">註解</span><span class="sxs-lookup"><span data-stu-id="df3e8-117">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df3e8-118">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="df3e8-118">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="df3e8-119">**ChildCount** 屬性一律為零。</span><span class="sxs-lookup"><span data-stu-id="df3e8-119">The **ChildCount** property is always zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="df3e8-120">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="df3e8-120">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="df3e8-121">**取得 \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="df3e8-121">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="df3e8-122">**KeyboardShortcut** 屬性是快速鍵控制項的存取金鑰，也就是快速鍵控制項標籤文字中的加底線字元。</span><span class="sxs-lookup"><span data-stu-id="df3e8-122">The **KeyboardShortcut** property is the hot key control's access key, which is an underlined character in the text of the hot key control's label.</span></span> <span data-ttu-id="df3e8-123">傳回的字串包含附加至字串 "Alt +" 的存取金鑰字元。</span><span class="sxs-lookup"><span data-stu-id="df3e8-123">The returned string contains the access key character appended to the string "Alt+".</span></span>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="df3e8-124">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="df3e8-124">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="df3e8-125">**Name** 屬性是靜態文字控制項中標示快速鍵控制項的文字。</span><span class="sxs-lookup"><span data-stu-id="df3e8-125">The **Name** property is the text from a static text control that labels the hot key control.</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="df3e8-126">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="df3e8-126">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="df3e8-127">**父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="df3e8-127">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="df3e8-128">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="df3e8-128">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="df3e8-129">**Role** 屬性為 [**role \_ SYSTEM \_ HOTKEYFIELD**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="df3e8-129">The **Role** property is [**ROLE\_SYSTEM\_HOTKEYFIELD**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="df3e8-130">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="df3e8-130">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="df3e8-131">**State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="df3e8-131">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |
| [<span data-ttu-id="df3e8-132">**取得 \_ accValue**</span><span class="sxs-lookup"><span data-stu-id="df3e8-132">**get\_accValue**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | <span data-ttu-id="df3e8-133">**Value** 屬性是一個字串，其中包含快速鍵欄位中的文字。</span><span class="sxs-lookup"><span data-stu-id="df3e8-133">The **Value** property is a string that contains the text in the hot key field.</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="df3e8-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="df3e8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df3e8-135">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="df3e8-135">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





