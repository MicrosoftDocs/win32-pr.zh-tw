---
title: '行事曆控制項 (MSAA UI 元素參考) '
description: 行事曆控制項提供簡單且直覺的方式，讓使用者從熟悉的介面中選取日期。
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839664"
---
# <a name="calendar-control-msaa-ui-element-reference"></a><span data-ttu-id="c6054-103">行事曆控制項 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="c6054-103">Calendar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="c6054-104">本主題說明用於 MSAA UI 專案參考之行事 **曆控制項** 物件的用途。</span><span class="sxs-lookup"><span data-stu-id="c6054-104">This topic describes **Calendar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="c6054-105">此處未說明如何在各種 UI 架構中建立行事 **曆控制項** 物件。</span><span class="sxs-lookup"><span data-stu-id="c6054-105">How to create **Calendar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="c6054-106">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="c6054-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="c6054-107">行事曆控制項提供簡單且直覺的方式，讓使用者從熟悉的介面中選取日期。</span><span class="sxs-lookup"><span data-stu-id="c6054-107">Calendar controls provide a simple and intuitive way for a user to select a date from a familiar interface.</span></span>

<span data-ttu-id="c6054-108">月曆控制項的視窗類別名稱是 MONTHCAL \_ 類別，其定義為 Commctrl 中的 "SysMonthCal32"。</span><span class="sxs-lookup"><span data-stu-id="c6054-108">The window class name for a month calendar control is MONTHCAL\_CLASS, which is defined as "SysMonthCal32" in Commctrl.h.</span></span> <span data-ttu-id="c6054-109">本主題中的資訊適用于 Commctrl 第5版中的月曆控制項。</span><span class="sxs-lookup"><span data-stu-id="c6054-109">Information in this topic applies to the month calendar control in version 5 of Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="c6054-110">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="c6054-110">IAccessible Methods</span></span>

<span data-ttu-id="c6054-111">行事曆控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="c6054-111">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="c6054-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="c6054-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="c6054-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="c6054-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="c6054-114">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="c6054-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="c6054-115">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="c6054-115">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="c6054-116">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="c6054-116">IAccessible Properties</span></span>

<span data-ttu-id="c6054-117">行事曆控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="c6054-117">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="c6054-118">屬性</span><span class="sxs-lookup"><span data-stu-id="c6054-118">Property</span></span>                                                                 | <span data-ttu-id="c6054-119">註解</span><span class="sxs-lookup"><span data-stu-id="c6054-119">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6054-120">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="c6054-120">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="c6054-121">**ChildCount** 屬性為零。</span><span class="sxs-lookup"><span data-stu-id="c6054-121">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="c6054-122">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="c6054-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="c6054-123">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="c6054-123">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="c6054-124">**Name** 屬性是從標記行事曆控制項的靜態文字控制項取得。</span><span class="sxs-lookup"><span data-stu-id="c6054-124">The **Name** property is obtained from the static text control that labels the calendar control.</span></span> <span data-ttu-id="c6054-125">當您建立控制項時，伺服器開發人員必須確保靜態文字控制項會緊接在定位順序中所標記的控制項之前。</span><span class="sxs-lookup"><span data-stu-id="c6054-125">When creating controls, server developers must ensure that a static text control immediately precedes the control that it labels within the tab order.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="c6054-126">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="c6054-126">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="c6054-127">**父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="c6054-127">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="c6054-128">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="c6054-128">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="c6054-129">**Role** 屬性是 [**role \_ SYSTEM \_ CLIENT**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="c6054-129">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="c6054-130">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="c6054-130">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="c6054-131">**State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態系統無法 \_ \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)的狀態系統焦點狀態系統可 \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ 設定焦點**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="c6054-131">The **State** property is a combination of one or more of the following [values](object-state-constants.md)[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c6054-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="c6054-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6054-133">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="c6054-133">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





