---
title: '靜態文字 (MSAA UI 元素參考) '
description: 靜態文字控制項提供便利的方式來顯示對話方塊和其他視窗上的文字。 靜態文字控制項通常作為其他控制項的標籤。
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f35581a9b305f28782d8faeac81105afb0d5147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840743"
---
# <a name="static-text-msaa-ui-element-reference"></a><span data-ttu-id="c2e2d-104">靜態文字 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="c2e2d-104">Static Text (MSAA UI Element Reference)</span></span>

<span data-ttu-id="c2e2d-105">靜態文字控制項提供便利的方式來顯示對話方塊和其他視窗上的文字。</span><span class="sxs-lookup"><span data-stu-id="c2e2d-105">Static text controls provide a convenient way to display text on dialog boxes and other windows.</span></span> <span data-ttu-id="c2e2d-106">靜態文字控制項通常作為其他控制項的標籤。</span><span class="sxs-lookup"><span data-stu-id="c2e2d-106">Static text controls often serve as labels for other controls.</span></span>

<span data-ttu-id="c2e2d-107">靜態文字控制項的視窗類別名稱是「靜態」。</span><span class="sxs-lookup"><span data-stu-id="c2e2d-107">The window class name for a static text control is "STATIC".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="c2e2d-108">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="c2e2d-108">IAccessible Methods</span></span>

<span data-ttu-id="c2e2d-109">靜態文字控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="c2e2d-109">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="c2e2d-110">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-110">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="c2e2d-111">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-111">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="c2e2d-112">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-112">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="c2e2d-113">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-113">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="c2e2d-114">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="c2e2d-114">IAccessible Properties</span></span>

<span data-ttu-id="c2e2d-115">靜態文字控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="c2e2d-115">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="c2e2d-116">屬性</span><span class="sxs-lookup"><span data-stu-id="c2e2d-116">Property</span></span>                                                                             | <span data-ttu-id="c2e2d-117">註解</span><span class="sxs-lookup"><span data-stu-id="c2e2d-117">Comments</span></span>                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2e2d-118">**取得 \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-118">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="c2e2d-119">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="c2e2d-120">**ChildCount** 屬性為零。</span><span class="sxs-lookup"><span data-stu-id="c2e2d-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="c2e2d-121">**取得 \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-121">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="c2e2d-122">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="c2e2d-123">**取得 \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-123">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="c2e2d-124">**取得 \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-124">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="c2e2d-125">**取得 \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-125">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="c2e2d-126">**KeyboardShortcut** 屬性是存取金鑰，也就是文字中加上底線的字元，可啟用與靜態文字相關聯的控制項。</span><span class="sxs-lookup"><span data-stu-id="c2e2d-126">The **KeyboardShortcut** property is the access key, which is the underlined character in the text that activates the control associated with the static text.</span></span> <span data-ttu-id="c2e2d-127">傳回的字串包含附加至字串 "Alt +" 的存取金鑰字元。</span><span class="sxs-lookup"><span data-stu-id="c2e2d-127">The returned string contains the access key character appended to the string "Alt+".</span></span>                                           |
| [<span data-ttu-id="c2e2d-128">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-128">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="c2e2d-129">[ **名稱** ] 屬性與靜態文字控制項中的文字相同。</span><span class="sxs-lookup"><span data-stu-id="c2e2d-129">The **Name** property is the same as the text in the static text control.</span></span>                                                                                                                                                                                                                     |
| [<span data-ttu-id="c2e2d-130">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="c2e2d-131">**父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="c2e2d-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                   |
| [<span data-ttu-id="c2e2d-132">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="c2e2d-133">**Role** 屬性為 [**role \_ SYSTEM \_ STATICTEXT**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="c2e2d-133">The **Role** property is [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md).</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="c2e2d-134">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="c2e2d-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="c2e2d-135">**State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 唯讀**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="c2e2d-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) \| [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="c2e2d-136">備註</span><span class="sxs-lookup"><span data-stu-id="c2e2d-136">Notes</span></span>

-   <span data-ttu-id="c2e2d-137">[](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) \_ \_ 當使用靜態文字物件上的 [**SELFLAG \_ TAKEFOCUS**](selflag.md)來呼叫時，accSelect 方法會傳回出現的 E MEMBERNOTFOUND。</span><span class="sxs-lookup"><span data-stu-id="c2e2d-137">The [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method returns DISP\_E\_MEMBERNOTFOUND when it is called with [**SELFLAG\_TAKEFOCUS**](selflag.md) on a static text object.</span></span>
-   <span data-ttu-id="c2e2d-138">具有 SS 圖示樣式的靜態控制項，會 \_ 在 **Name** 屬性中傳回不正確資料。</span><span class="sxs-lookup"><span data-stu-id="c2e2d-138">Static controls with the SS\_ICON style return invalid data in the **Name** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2e2d-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2e2d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2e2d-140">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="c2e2d-140">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





