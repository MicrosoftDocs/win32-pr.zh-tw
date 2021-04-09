---
title: '工具提示控制項 (MSAA UI 元素參考) '
description: 工具提示控制項會顯示一個小型的快顯視窗，其中包含描述工具用途（以繪圖物件表示）在應用程式中的文字行。
ms.assetid: d3a65d7b-b882-4a1a-bac2-6995b64cf4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37557fd116084fc9ac53e8567afc90eda339750d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840044"
---
# <a name="tooltip-control-msaa-ui-element-reference"></a><span data-ttu-id="3436a-103">工具提示控制項 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="3436a-103">ToolTip Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="3436a-104">本主題描述用於 MSAA UI 元素參考的 **工具提示控制項** 物件。</span><span class="sxs-lookup"><span data-stu-id="3436a-104">This topic describes **ToolTip Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="3436a-105">此處未說明如何在各種 UI 架構中建立 **工具提示控制項** 物件。</span><span class="sxs-lookup"><span data-stu-id="3436a-105">How to create **ToolTip Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="3436a-106">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="3436a-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="3436a-107">工具提示控制項會顯示一個小型的快顯視窗，其中包含描述工具用途（以繪圖物件表示）在應用程式中的文字行。</span><span class="sxs-lookup"><span data-stu-id="3436a-107">A tooltip control displays a small pop-up window that contains a line of text that describes the purpose of a tool, represented as a graphical object, in an application.</span></span>

<span data-ttu-id="3436a-108">工具提示的視窗類別名稱是工具提示 \_ 類別，在 Commctrl 中定義為 "tooltip \_ class"。</span><span class="sxs-lookup"><span data-stu-id="3436a-108">The window class name for a tooltip is TOOLTIPS\_CLASS, which is defined as "tooltips\_class" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="3436a-109">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="3436a-109">IAccessible Methods</span></span>

<span data-ttu-id="3436a-110">工具提示控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="3436a-110">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="3436a-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="3436a-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="3436a-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="3436a-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="3436a-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="3436a-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="3436a-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="3436a-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="3436a-115">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="3436a-115">IAccessible Properties</span></span>

<span data-ttu-id="3436a-116">工具提示控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="3436a-116">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="3436a-117">屬性</span><span class="sxs-lookup"><span data-stu-id="3436a-117">Property</span></span>                                                                 | <span data-ttu-id="3436a-118">註解</span><span class="sxs-lookup"><span data-stu-id="3436a-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3436a-119">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="3436a-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="3436a-120">**ChildCount** 屬性為零。</span><span class="sxs-lookup"><span data-stu-id="3436a-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="3436a-121">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="3436a-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="3436a-122">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="3436a-122">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="3436a-123">**Name** 屬性是工具提示控制項中包含的文字。</span><span class="sxs-lookup"><span data-stu-id="3436a-123">The **Name** property is the text contained in the tooltip control.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="3436a-124">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="3436a-124">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="3436a-125">**父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="3436a-125">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="3436a-126">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="3436a-126">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="3436a-127">**Role** 屬性是 [**角色 \_ 系統 \_ 工具提示**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="3436a-127">The **Role** property is [**ROLE\_SYSTEM\_TOOLTIP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="3436a-128">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="3436a-128">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="3436a-129">**State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="3436a-129">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="3436a-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="3436a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3436a-131">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="3436a-131">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





