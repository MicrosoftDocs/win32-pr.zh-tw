---
title: '群組方塊 (MSAA UI 元素參考) '
description: 群組方塊是圍繞一組控制項（例如核取方塊或選項按鈕）的矩形，其中包含應用程式定義的文字 (標籤) 。
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a105242aabd49d87241a2a49bdaca5c19edd350b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674580"
---
# <a name="group-box-msaa-ui-element-reference"></a><span data-ttu-id="85baa-103">群組方塊 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="85baa-103">Group Box (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="85baa-104">本主題描述用於 MSAA UI 元素參考的 **群組方塊** 物件。</span><span class="sxs-lookup"><span data-stu-id="85baa-104">This topic describes **Group Box** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="85baa-105">此處未說明如何在各種 UI 架構中建立 **群組** 方塊物件。</span><span class="sxs-lookup"><span data-stu-id="85baa-105">How to create **Group Box** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="85baa-106">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="85baa-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="85baa-107">群組方塊是圍繞一組控制項（例如核取方塊或選項按鈕）的矩形，其中包含應用程式定義的文字 (標籤) 。</span><span class="sxs-lookup"><span data-stu-id="85baa-107">A group box is a rectangle that surrounds a set of controls, such as check boxes or radio buttons, and contains an application-defined text (label).</span></span>

<span data-ttu-id="85baa-108">群組方塊的唯一目的是組織由標籤表示的一般用途相關控制項。</span><span class="sxs-lookup"><span data-stu-id="85baa-108">The sole purpose of a group box is to organize controls related by a common purpose, indicated by the label.</span></span>

<span data-ttu-id="85baa-109">群組方塊的視窗類別名稱為 "BUTTON"。</span><span class="sxs-lookup"><span data-stu-id="85baa-109">The window class name for a group box is "BUTTON".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="85baa-110">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="85baa-110">IAccessible Methods</span></span>

<span data-ttu-id="85baa-111">群組方塊支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="85baa-111">A group box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="85baa-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="85baa-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="85baa-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="85baa-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="85baa-114">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="85baa-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="85baa-115">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="85baa-115">IAccessible Properties</span></span>

<span data-ttu-id="85baa-116">群組方塊支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="85baa-116">A group box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="85baa-117">屬性</span><span class="sxs-lookup"><span data-stu-id="85baa-117">Property</span></span>                                                                             | <span data-ttu-id="85baa-118">註解</span><span class="sxs-lookup"><span data-stu-id="85baa-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85baa-119">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="85baa-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="85baa-120">**ChildCount** 屬性一律為零。</span><span class="sxs-lookup"><span data-stu-id="85baa-120">The **ChildCount** property is always zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="85baa-121">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="85baa-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="85baa-122">**取得 \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="85baa-122">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="85baa-123">群組方塊沒有鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="85baa-123">Group boxes do not have keyboard shortcuts.</span></span> <span data-ttu-id="85baa-124">但是，如果群組方塊的視窗文字包含 & 符號 (&) 字元，Microsoft Active Accessibility 會傳回非 Null 字串做為 **KeyboardShortcut** 屬性。</span><span class="sxs-lookup"><span data-stu-id="85baa-124">However, if the window text for the group box contains an ampersand (&) character, Microsoft Active Accessibility returns a non-Null string as the **KeyboardShortcut** property.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="85baa-125">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="85baa-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="85baa-126">[ **名稱** ] 屬性是從控制項的視窗文字 (或標題) （顯示在 [群組方塊] 中）取得。</span><span class="sxs-lookup"><span data-stu-id="85baa-126">The **Name** property is obtained from the control's window text (or caption), which is displayed with the group box.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="85baa-127">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="85baa-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="85baa-128">**父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="85baa-128">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="85baa-129">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="85baa-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="85baa-130">**Role** 屬性是 [**角色 \_ 系統 \_ 群組**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="85baa-130">The **Role** property is [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="85baa-131">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="85baa-131">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="85baa-132">**State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="85baa-132">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="85baa-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="85baa-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85baa-134">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="85baa-134">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





