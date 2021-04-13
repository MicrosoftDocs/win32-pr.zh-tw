---
title: '標題控制項 (MSAA UI 元素參考) '
description: 標題控制項會在資訊的資料行頂端顯示標題，並讓使用者按一下標題來排序資訊。 當選取 [詳細資料] 視圖時，Windows 檔案總管使用標題控制項。
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301599"
---
# <a name="header-control-msaa-ui-element-reference"></a><span data-ttu-id="dba7b-104">標題控制項 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="dba7b-104">Header Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="dba7b-105">本主題將描述用於 MSAA UI 元素參考的 **標題控制項** 物件。</span><span class="sxs-lookup"><span data-stu-id="dba7b-105">This topic describes **Header Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="dba7b-106">此處未說明如何在各種 UI 架構中建立 **標題控制項** 物件。</span><span class="sxs-lookup"><span data-stu-id="dba7b-106">How to create **Header Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="dba7b-107">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="dba7b-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="dba7b-108">標題控制項會在資訊的資料行頂端顯示標題，並讓使用者按一下標題來排序資訊。</span><span class="sxs-lookup"><span data-stu-id="dba7b-108">A header control displays headings at the top of columns of information and lets the user sort the information by clicking the headings.</span></span> <span data-ttu-id="dba7b-109">當選取 [詳細資料] 視圖時，Windows 檔案總管使用標題控制項。</span><span class="sxs-lookup"><span data-stu-id="dba7b-109">Windows Explorer uses a header control when the Details view is selected.</span></span>

<span data-ttu-id="dba7b-110">標題控制項的視窗類別名稱是 WC \_ 標頭，其定義為 Commctrl 中的 "SysHeader32"。</span><span class="sxs-lookup"><span data-stu-id="dba7b-110">The window class name for a header control is WC\_HEADER, which is defined as "SysHeader32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="dba7b-111">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="dba7b-111">IAccessible Methods</span></span>

<span data-ttu-id="dba7b-112">標題控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="dba7b-112">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="dba7b-113">方法</span><span class="sxs-lookup"><span data-stu-id="dba7b-113">Method</span></span>                                                                    | <span data-ttu-id="dba7b-114">註解</span><span class="sxs-lookup"><span data-stu-id="dba7b-114">Comments</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="dba7b-115">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="dba7b-115">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="dba7b-116">這個方法會藉由按一下標頭來執行預設動作。</span><span class="sxs-lookup"><span data-stu-id="dba7b-116">This method performs the default action by clicking the header.</span></span> |
| [<span data-ttu-id="dba7b-117">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="dba7b-117">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [<span data-ttu-id="dba7b-118">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="dba7b-118">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [<span data-ttu-id="dba7b-119">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="dba7b-119">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [<span data-ttu-id="dba7b-120">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="dba7b-120">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="dba7b-121">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="dba7b-121">IAccessible Properties</span></span>

<span data-ttu-id="dba7b-122">標題控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="dba7b-122">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="dba7b-123">屬性</span><span class="sxs-lookup"><span data-stu-id="dba7b-123">Property</span></span>                                                                       | <span data-ttu-id="dba7b-124">註解</span><span class="sxs-lookup"><span data-stu-id="dba7b-124">Comments</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dba7b-125">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="dba7b-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="dba7b-126">**ChildCount** 屬性為零。</span><span class="sxs-lookup"><span data-stu-id="dba7b-126">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="dba7b-127">**取得 \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="dba7b-127">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="dba7b-128">**DefaultAction** 屬性為 "Click"。</span><span class="sxs-lookup"><span data-stu-id="dba7b-128">The **DefaultAction** property is "Click".</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="dba7b-129">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="dba7b-129">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [<span data-ttu-id="dba7b-130">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="dba7b-130">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="dba7b-131">**名稱** 屬性與資料行標題的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="dba7b-131">The **Name** property is the same as the name of the column header.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="dba7b-132">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="dba7b-132">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | <span data-ttu-id="dba7b-133">**父** 屬性是視窗 ([**角色 \_ 系統 \_ 清單**](object-roles.md)) ，它會圍繞控制項，而且具有與控制項相同的視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="dba7b-133">The **Parent** property is a window ( [**ROLE\_SYSTEM\_LIST**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span>                                                      |
| [<span data-ttu-id="dba7b-134">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="dba7b-134">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="dba7b-135">**Role** 屬性為 [**role \_ SYSTEM \_ COLUMNHEADER**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="dba7b-135">The **Role** property is [**ROLE\_SYSTEM\_COLUMNHEADER**](object-roles.md).</span></span>                                                                                                                                  |
| [<span data-ttu-id="dba7b-136">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="dba7b-136">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="dba7b-137">**State** 屬性的值一律為 [**state \_ system \_ READONLY**](object-state-constants.md) ，也可以包含 [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="dba7b-137">The value for the **State** property is always [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) and can also include [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dba7b-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="dba7b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dba7b-139">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="dba7b-139">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




