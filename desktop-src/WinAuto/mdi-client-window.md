---
title: 'MDI 用戶端視窗 (MSAA UI 元素參考) '
description: 多重文件介面 (MDI) 是一種規格，可定義針對 Windows 撰寫之應用程式的標準使用者介面。 MDI 應用程式可讓使用者一次使用一個以上的檔。
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932170"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a><span data-ttu-id="a239f-104">MDI 用戶端視窗 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="a239f-104">MDI Client Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="a239f-105">多重文件介面 (MDI) 是一種規格，可定義針對 Windows 撰寫之應用程式的標準使用者介面。</span><span class="sxs-lookup"><span data-stu-id="a239f-105">The multiple document interface (MDI) is a specification that defines the standard user interface for applications written for Windows.</span></span> <span data-ttu-id="a239f-106">MDI 應用程式可讓使用者一次使用一個以上的檔。</span><span class="sxs-lookup"><span data-stu-id="a239f-106">An MDI application enables a user to work with more than one document at a time.</span></span>

<span data-ttu-id="a239f-107">MDI 應用程式有三種視窗：框架視窗、用戶端視窗和一些子視窗。</span><span class="sxs-lookup"><span data-stu-id="a239f-107">An MDI application has three kinds of windows: a frame window, a client window, and a number of child windows.</span></span> <span data-ttu-id="a239f-108">框架視窗就像是應用程式的主視窗，它會圍住用戶端視窗。</span><span class="sxs-lookup"><span data-stu-id="a239f-108">The frame window is like the main window of an application, and it surrounds the client window.</span></span> <span data-ttu-id="a239f-109">用戶端視窗是框架視窗的子系，作為子視窗的背景。</span><span class="sxs-lookup"><span data-stu-id="a239f-109">The client window is a child of the frame window and serves as the background for the child windows.</span></span> <span data-ttu-id="a239f-110">用戶端視窗也提供建立和操作在其中顯示檔之子視窗的支援。</span><span class="sxs-lookup"><span data-stu-id="a239f-110">The client window also provides support for creating and manipulating the child windows in which documents are displayed.</span></span>

<span data-ttu-id="a239f-111">MDI 用戶端視窗的視窗類別名稱是 "MDIClient"。</span><span class="sxs-lookup"><span data-stu-id="a239f-111">The window class name for an MDI client window is "MDIClient".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="a239f-112">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="a239f-112">IAccessible Methods</span></span>

<span data-ttu-id="a239f-113">MDI 用戶端視窗支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="a239f-113">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="a239f-114">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="a239f-114">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="a239f-115">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="a239f-115">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="a239f-116">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="a239f-116">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="a239f-117">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="a239f-117">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="a239f-118">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="a239f-118">IAccessible Properties</span></span>

<span data-ttu-id="a239f-119">MDI 用戶端視窗支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="a239f-119">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="a239f-120">屬性</span><span class="sxs-lookup"><span data-stu-id="a239f-120">Property</span></span>                                                                 | <span data-ttu-id="a239f-121">註解</span><span class="sxs-lookup"><span data-stu-id="a239f-121">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a239f-122">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="a239f-122">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="a239f-123">**ChildCount** 屬性是顯示檔的子視窗數目。</span><span class="sxs-lookup"><span data-stu-id="a239f-123">The **ChildCount** property is the number of child windows in which documents are displayed.</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="a239f-124">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="a239f-124">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a239f-125">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="a239f-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="a239f-126">**Name** 屬性為 "Workspace"。</span><span class="sxs-lookup"><span data-stu-id="a239f-126">The **Name** property is "Workspace".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="a239f-127">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="a239f-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="a239f-128">**父** 屬性是 MDI 框架視窗。</span><span class="sxs-lookup"><span data-stu-id="a239f-128">The **Parent** property is the MDI frame window.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="a239f-129">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="a239f-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="a239f-130">**Role** 屬性是 [**role \_ SYSTEM \_ 用戶端**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="a239f-130">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md)</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="a239f-131">**取得 \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="a239f-131">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a239f-132">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="a239f-132">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="a239f-133">**State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a239f-133">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="a239f-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="a239f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a239f-135">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="a239f-135">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





