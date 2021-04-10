---
title: '用戶端物件 (MSAA UI 元素參考) '
description: 工作區是視窗的一部分，其中應用程式會顯示輸出，例如文字或圖形。 例如，桌面發佈應用程式會在工作區中顯示檔的目前頁面。
ms.assetid: 1b3a800e-e3c1-4737-8ad0-41707eb1e985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be28ae4c31e1a2d2f72674a39d7db08730562816
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092852"
---
# <a name="client-object-msaa-ui-element-reference"></a><span data-ttu-id="1d293-104">用戶端物件 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="1d293-104">Client Object (MSAA UI Element Reference)</span></span>

<span data-ttu-id="1d293-105">工作區是視窗的一部分，其中應用程式會顯示輸出，例如文字或圖形。</span><span class="sxs-lookup"><span data-stu-id="1d293-105">The client area is the part of a window where the application displays output, such as text or graphics.</span></span> <span data-ttu-id="1d293-106">例如，桌面發佈應用程式會在工作區中顯示檔的目前頁面。</span><span class="sxs-lookup"><span data-stu-id="1d293-106">For example, a desktop publishing application displays the current page of a document in the client area.</span></span>

<span data-ttu-id="1d293-107">伺服器應用程式開發人員負責建立可存取的物件，以提供應用程式工作區內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1d293-107">Server application developers are responsible for creating accessible objects that provide information about the contents of the application's client area.</span></span>

<span data-ttu-id="1d293-108">如果用戶端應用程式要求應用程式內自訂 UI 元素的相關資訊，以及不支援 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的自訂 ui 元素，Microsoft Active Accessibility 會以最基本的資訊建立預設的可存取物件。</span><span class="sxs-lookup"><span data-stu-id="1d293-108">If a client application requests information about a custom UI element within an application, and the custom UI element that does not support the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface, Microsoft Active Accessibility creates a default accessible object with minimal information.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="1d293-109">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="1d293-109">IAccessible Methods</span></span>

<span data-ttu-id="1d293-110">工作區支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="1d293-110">The client area supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="1d293-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="1d293-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="1d293-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="1d293-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="1d293-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="1d293-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="1d293-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="1d293-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="1d293-115">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="1d293-115">IAccessible Properties</span></span>

<span data-ttu-id="1d293-116">工作區支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="1d293-116">The client area supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="1d293-117">屬性</span><span class="sxs-lookup"><span data-stu-id="1d293-117">Property</span></span>                                                                             | <span data-ttu-id="1d293-118">註解</span><span class="sxs-lookup"><span data-stu-id="1d293-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d293-119">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="1d293-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="1d293-120">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="1d293-120">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="1d293-121">**取得 \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="1d293-121">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="1d293-122">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="1d293-122">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="1d293-123">傳送 [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) 訊息以取得視窗文字。</span><span class="sxs-lookup"><span data-stu-id="1d293-123">Sends the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext) message to retrieve the window text.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="1d293-124">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="1d293-124">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="1d293-125">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="1d293-125">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="1d293-126">**Role** 屬性是 [**role \_ SYSTEM \_ CLIENT**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="1d293-126">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="1d293-127">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="1d293-127">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="1d293-128">**State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="1d293-128">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1d293-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d293-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d293-130">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="1d293-130">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

