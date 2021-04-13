---
title: 'Cursor (MSAA UI 元素參考) '
description: 游標是螢幕上的位置，由指標裝置（例如，滑鼠、畫筆或軌跡球）控制的小型圖片。 當使用者移動指標裝置時，Windows 作業系統會移動游標。
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300304"
---
# <a name="cursor-msaa-ui-element-reference"></a><span data-ttu-id="f69b3-104">Cursor (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="f69b3-104">Cursor (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="f69b3-105">本主題說明 MSAA UI 專案參考之用途的資料指標。</span><span class="sxs-lookup"><span data-stu-id="f69b3-105">This topic describes cursors for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="f69b3-106">此處未說明如何在各種 UI 架構中使用資料指標。</span><span class="sxs-lookup"><span data-stu-id="f69b3-106">How to use cursors in various UI frameworks is not described here.</span></span> <span data-ttu-id="f69b3-107">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="f69b3-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="f69b3-108">游標是螢幕上的位置，由指標裝置（例如，滑鼠、畫筆或軌跡球）控制的小型圖片。</span><span class="sxs-lookup"><span data-stu-id="f69b3-108">A cursor is a small picture whose location on the screen is controlled by a pointing device, such as a mouse, pen, or trackball.</span></span> <span data-ttu-id="f69b3-109">當使用者移動指標裝置時，Windows 作業系統會移動游標。</span><span class="sxs-lookup"><span data-stu-id="f69b3-109">When the user moves the pointing device, the Windows operating system moves the cursor.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="f69b3-110">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="f69b3-110">IAccessible Methods</span></span>

<span data-ttu-id="f69b3-111">資料指標支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="f69b3-111">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="f69b3-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="f69b3-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="f69b3-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="f69b3-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="f69b3-114">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="f69b3-114">IAccessible Properties</span></span>

<span data-ttu-id="f69b3-115">資料指標支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="f69b3-115">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="f69b3-116">[**get \_ AccChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)- **ChildCount** 屬性為零。</span><span class="sxs-lookup"><span data-stu-id="f69b3-116">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="f69b3-117">[**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)-開發人員可以建立自訂資料指標，或使用其資料指標識別碼所識別的預先定義資料指標。</span><span class="sxs-lookup"><span data-stu-id="f69b3-117">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—Developers can create custom cursors or use the predefined cursors that are identified by their cursor ID.</span></span> <span data-ttu-id="f69b3-118">游標的 **名稱** 屬性取決於其圖形，而且是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="f69b3-118">The **Name** property of the cursor depends on its shape and is one of the following:</span></span> 

    | <span data-ttu-id="f69b3-119">游標圖形</span><span class="sxs-lookup"><span data-stu-id="f69b3-119">Cursor shape</span></span>     | <span data-ttu-id="f69b3-120">Name</span><span class="sxs-lookup"><span data-stu-id="f69b3-120">Name</span></span>              |
    |------------------|-------------------|
    | <span data-ttu-id="f69b3-121">自訂資料指標</span><span class="sxs-lookup"><span data-stu-id="f69b3-121">Custom cursor</span></span>    | <span data-ttu-id="f69b3-122">不明</span><span class="sxs-lookup"><span data-stu-id="f69b3-122">"Unknown"</span></span>         |
    | <span data-ttu-id="f69b3-123">IDC \_ 箭號</span><span class="sxs-lookup"><span data-stu-id="f69b3-123">IDC\_ARROW</span></span>       | <span data-ttu-id="f69b3-124">"Normal"</span><span class="sxs-lookup"><span data-stu-id="f69b3-124">"Normal"</span></span>          |
    | <span data-ttu-id="f69b3-125">IDC \_ I 字形狀</span><span class="sxs-lookup"><span data-stu-id="f69b3-125">IDC\_IBEAM</span></span>       | <span data-ttu-id="f69b3-126">編輯</span><span class="sxs-lookup"><span data-stu-id="f69b3-126">"Edit"</span></span>            |
    | <span data-ttu-id="f69b3-127">IDC \_ 等候</span><span class="sxs-lookup"><span data-stu-id="f69b3-127">IDC\_WAIT</span></span>        | <span data-ttu-id="f69b3-128">繼續</span><span class="sxs-lookup"><span data-stu-id="f69b3-128">"Wait"</span></span>            |
    | <span data-ttu-id="f69b3-129">IDC \_ 交叉</span><span class="sxs-lookup"><span data-stu-id="f69b3-129">IDC\_CROSS</span></span>       | <span data-ttu-id="f69b3-130">示意圖</span><span class="sxs-lookup"><span data-stu-id="f69b3-130">"Graphic"</span></span>         |
    | <span data-ttu-id="f69b3-131">IDC \_ UPARROW</span><span class="sxs-lookup"><span data-stu-id="f69b3-131">IDC\_UPARROW</span></span>     | <span data-ttu-id="f69b3-132">創建</span><span class="sxs-lookup"><span data-stu-id="f69b3-132">"Up"</span></span>              |
    | <span data-ttu-id="f69b3-133">IDC \_ SIZENWSE</span><span class="sxs-lookup"><span data-stu-id="f69b3-133">IDC\_SIZENWSE</span></span>    | <span data-ttu-id="f69b3-134">「NWSE 大小」</span><span class="sxs-lookup"><span data-stu-id="f69b3-134">"NWSE size"</span></span>       |
    | <span data-ttu-id="f69b3-135">IDC \_ SIZENESW</span><span class="sxs-lookup"><span data-stu-id="f69b3-135">IDC\_SIZENESW</span></span>    | <span data-ttu-id="f69b3-136">「NESW 大小」</span><span class="sxs-lookup"><span data-stu-id="f69b3-136">"NESW size"</span></span>       |
    | <span data-ttu-id="f69b3-137">IDC \_ SIZEWE</span><span class="sxs-lookup"><span data-stu-id="f69b3-137">IDC\_SIZEWE</span></span>      | <span data-ttu-id="f69b3-138">「水準大小」</span><span class="sxs-lookup"><span data-stu-id="f69b3-138">"Horizontal size"</span></span> |
    | <span data-ttu-id="f69b3-139">IDC \_ SIZENS</span><span class="sxs-lookup"><span data-stu-id="f69b3-139">IDC\_SIZENS</span></span>      | <span data-ttu-id="f69b3-140">「垂直大小」</span><span class="sxs-lookup"><span data-stu-id="f69b3-140">"Vertical size"</span></span>   |
    | <span data-ttu-id="f69b3-141">IDC \_ SIZEALL</span><span class="sxs-lookup"><span data-stu-id="f69b3-141">IDC\_SIZEALL</span></span>     | <span data-ttu-id="f69b3-142">刪除</span><span class="sxs-lookup"><span data-stu-id="f69b3-142">"Move"</span></span>            |
    | <span data-ttu-id="f69b3-143">IDC \_ 否</span><span class="sxs-lookup"><span data-stu-id="f69b3-143">IDC\_NO</span></span>          | <span data-ttu-id="f69b3-144">禁止</span><span class="sxs-lookup"><span data-stu-id="f69b3-144">"Forbidden"</span></span>       |
    | <span data-ttu-id="f69b3-145">IDC \_ APPSTARTING</span><span class="sxs-lookup"><span data-stu-id="f69b3-145">IDC\_APPSTARTING</span></span> | <span data-ttu-id="f69b3-146">「應用程式啟動」</span><span class="sxs-lookup"><span data-stu-id="f69b3-146">"App start"</span></span>       |
    | <span data-ttu-id="f69b3-147">IDC \_ 說明</span><span class="sxs-lookup"><span data-stu-id="f69b3-147">IDC\_HELP</span></span>        | <span data-ttu-id="f69b3-148">連線</span><span class="sxs-lookup"><span data-stu-id="f69b3-148">"Help"</span></span>            |

    

     

-   <span data-ttu-id="f69b3-149">[**取得 \_ AccRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)- **role** 屬性是 [**role 系統 \_ 資料 \_ 指標**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="f69b3-149">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property is [**ROLE\_SYSTEM\_CURSOR**](object-roles.md).</span></span>
-   <span data-ttu-id="f69b3-150">[**get \_ AccState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)- **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：</span><span class="sxs-lookup"><span data-stu-id="f69b3-150">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property is a combination of one or more of the following [values](object-state-constants.md):</span></span>

    <span data-ttu-id="f69b3-151">[**狀態 \_系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 浮動**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="f69b3-151">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FLOATING**](object-state-constants.md)</span></span>

## <a name="notes"></a><span data-ttu-id="f69b3-152">備註</span><span class="sxs-lookup"><span data-stu-id="f69b3-152">Notes</span></span>

-   <span data-ttu-id="f69b3-153">與其他 UI 元素不同的是，資料指標物件沒有相關聯的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="f69b3-153">Unlike other UI elements, the cursor object does not have an associated window handle.</span></span> <span data-ttu-id="f69b3-154">若要取得資料指標物件的存取權，用戶端必須設定 [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) ，並等候資料指標物件產生事件。</span><span class="sxs-lookup"><span data-stu-id="f69b3-154">To obtain access to the cursor object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the cursor object to generate events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f69b3-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="f69b3-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f69b3-156">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="f69b3-156">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




