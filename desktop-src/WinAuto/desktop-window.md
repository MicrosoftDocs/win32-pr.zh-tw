---
title: '桌面視窗 (MSAA UI 元素參考) '
description: 桌面視窗會顯示桌面清單視圖 (，其中包含我的電腦) 和包含 [開始] 按鈕的工作列等圖示。
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58208b3993964a367d093174d58d705beda23d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371944"
---
# <a name="desktop-window-msaa-ui-element-reference"></a><span data-ttu-id="bc5e8-103">桌面視窗 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="bc5e8-103">Desktop Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="bc5e8-104">桌面視窗會顯示桌面清單視圖 (，其中包含我的電腦) 和包含 [ **開始** ] 按鈕的工作列等圖示。</span><span class="sxs-lookup"><span data-stu-id="bc5e8-104">The desktop window displays the desktop list view (which contains icons such as My Computer) and the taskbar that contains the **Start** button.</span></span>

<span data-ttu-id="bc5e8-105">用戶端很少會查詢這個物件，因為清單視圖和工作列都涵蓋整個桌面。</span><span class="sxs-lookup"><span data-stu-id="bc5e8-105">This object is rarely queried by clients because the list view and the taskbar cover the entire desktop.</span></span> <span data-ttu-id="bc5e8-106">當您登入時，系統會在作業系統 shell 顯示清單視圖和工作列之前取出桌面物件。</span><span class="sxs-lookup"><span data-stu-id="bc5e8-106">The desktop object is retrieved when you log on, before the operating system shell displays the list view and taskbar.</span></span> <span data-ttu-id="bc5e8-107">在某些情況下，會在流覽其他物件時取得桌面。</span><span class="sxs-lookup"><span data-stu-id="bc5e8-107">In some cases, the desktop is obtained when navigating from other objects.</span></span>

<span data-ttu-id="bc5e8-108">桌面視窗的視窗類別名稱是 " \# 32769"。</span><span class="sxs-lookup"><span data-stu-id="bc5e8-108">The window class name for the desktop window is "\#32769".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="bc5e8-109">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="bc5e8-109">IAccessible Methods</span></span>

<span data-ttu-id="bc5e8-110">桌面視窗支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="bc5e8-110">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="bc5e8-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="bc5e8-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="bc5e8-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="bc5e8-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="bc5e8-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="bc5e8-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="bc5e8-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="bc5e8-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="bc5e8-115">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="bc5e8-115">IAccessible Properties</span></span>

<span data-ttu-id="bc5e8-116">桌面視窗支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="bc5e8-116">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="bc5e8-117">屬性</span><span class="sxs-lookup"><span data-stu-id="bc5e8-117">Property</span></span>                                                                 | <span data-ttu-id="bc5e8-118">註解</span><span class="sxs-lookup"><span data-stu-id="bc5e8-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc5e8-119">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="bc5e8-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="bc5e8-120">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="bc5e8-120">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="bc5e8-121">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="bc5e8-121">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="bc5e8-122">Name 屬性為 "Desktop"。</span><span class="sxs-lookup"><span data-stu-id="bc5e8-122">The Name property is "Desktop".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="bc5e8-123">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="bc5e8-123">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="bc5e8-124">**Role** 屬性是 [**role \_ SYSTEM \_ CLIENT**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="bc5e8-124">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="bc5e8-125">**取得 \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="bc5e8-125">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="bc5e8-126">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="bc5e8-126">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="bc5e8-127">**State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="bc5e8-127">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="bc5e8-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc5e8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc5e8-129">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="bc5e8-129">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





