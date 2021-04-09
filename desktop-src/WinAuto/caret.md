---
title: '插入號 (MSAA UI 元素參考) '
description: 插入點是視窗工作區或接受鍵盤輸入之控制項中的閃爍線、區塊或點陣圖。
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3855e4825c6c8b8498f0b4b278a099452baa9d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "103841831"
---
# <a name="caret-msaa-ui-element-reference"></a><span data-ttu-id="26f01-103">插入號 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="26f01-103">Caret (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="26f01-104">本主題說明 MSAA UI 元素參考的游標。</span><span class="sxs-lookup"><span data-stu-id="26f01-104">This topic describes carets for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="26f01-105">此處未說明如何在各種 UI 架構中使用游標。</span><span class="sxs-lookup"><span data-stu-id="26f01-105">How to use carets in various UI frameworks is not described here.</span></span> <span data-ttu-id="26f01-106">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="26f01-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="26f01-107">插入點是視窗工作區或接受鍵盤輸入之控制項中的閃爍線、區塊或點陣圖。</span><span class="sxs-lookup"><span data-stu-id="26f01-107">The caret is a flashing line, block, or bitmap in the client area of a window or in a control that accepts keyboard input.</span></span> <span data-ttu-id="26f01-108">指出插入文字或圖形的位置。</span><span class="sxs-lookup"><span data-stu-id="26f01-108">It indicates the place at which text or graphics are inserted.</span></span> <span data-ttu-id="26f01-109">因為一次只有一個視窗具有鍵盤焦點，系統中只會有一個插入號。</span><span class="sxs-lookup"><span data-stu-id="26f01-109">Because only one window at a time has the keyboard focus, there is only one caret in the system.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="26f01-110">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="26f01-110">IAccessible Methods</span></span>

<span data-ttu-id="26f01-111">插入號支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="26f01-111">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="26f01-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="26f01-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="26f01-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="26f01-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="26f01-114">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="26f01-114">IAccessible Properties</span></span>

<span data-ttu-id="26f01-115">插入號支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="26f01-115">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26f01-116">屬性</span><span class="sxs-lookup"><span data-stu-id="26f01-116">Property</span></span></th>
<th><span data-ttu-id="26f01-117">註解</span><span class="sxs-lookup"><span data-stu-id="26f01-117">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26f01-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f01-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="26f01-119"><strong>ChildCount</strong>屬性為零。</span><span class="sxs-lookup"><span data-stu-id="26f01-119">The <strong>ChildCount</strong> property is zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26f01-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f01-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span></span></td>
<td><span data-ttu-id="26f01-121"><strong>Name</strong>屬性為 &quot; Edit &quot; 。</span><span class="sxs-lookup"><span data-stu-id="26f01-121">The <strong>Name</strong> property is &quot;Edit&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26f01-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f01-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span></span></td>
<td><span data-ttu-id="26f01-123"><strong>Role</strong>屬性為<strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>。</span><span class="sxs-lookup"><span data-stu-id="26f01-123">The <strong>Role</strong> property is <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26f01-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span><span class="sxs-lookup"><span data-stu-id="26f01-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span></span></td>
<td><span data-ttu-id="26f01-125"><strong>State</strong>屬性可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="26f01-125">Possible values for the <strong>State</strong> property include:</span></span>
<ul>
<li><span data-ttu-id="26f01-126">零，表示插入號是可見的</span><span class="sxs-lookup"><span data-stu-id="26f01-126">Zero, which means the caret is visible</span></span></li>
<li><span data-ttu-id="26f01-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span><span class="sxs-lookup"><span data-stu-id="26f01-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="26f01-128">備註</span><span class="sxs-lookup"><span data-stu-id="26f01-128">Notes</span></span>

-   <span data-ttu-id="26f01-129">與其他 UI 元素不同的是，插入號物件沒有相關聯的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="26f01-129">Unlike other UI elements, the caret object does not have an associated window handle.</span></span> <span data-ttu-id="26f01-130">若要取得插入號物件的存取權，用戶端必須設定 [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) ，並等候插入號物件產生事件。</span><span class="sxs-lookup"><span data-stu-id="26f01-130">To obtain access to the caret object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the caret object to generate events.</span></span>
-   <span data-ttu-id="26f01-131">Riched20.dll (在文字編輯器（例如 Windows) 98 中的 Microsoft WordPad）所提供的 rich edit 控制項中的插入號物件，在文字選取期間變更其位置時，不會傳送任何 [WinEvents](winevents-infrastructure.md) 。</span><span class="sxs-lookup"><span data-stu-id="26f01-131">The caret object in the rich edit control provided by Riched20.dll (which is used in text editors such as Microsoft WordPad in Windows 98) does not send any [WinEvents](winevents-infrastructure.md) when its position is changed during text selection.</span></span> <span data-ttu-id="26f01-132">當使用者按下 SHIFT 和方向鍵選取文字時，插入號物件不會觸發 [**事件 \_ 物件 \_ LOCATIONCHANGE**](event-constants.md) new-winevent。</span><span class="sxs-lookup"><span data-stu-id="26f01-132">When users press SHIFT and arrow keys to select text, the caret object does not trigger the [**EVENT\_OBJECT\_LOCATIONCHANGE**](event-constants.md) WinEvent.</span></span> <span data-ttu-id="26f01-133">同樣地，當您透過 rich edit 訊息以程式設計方式設定選取專案時，插入號物件不會傳送任何事件來指出其新位置。</span><span class="sxs-lookup"><span data-stu-id="26f01-133">Similarly, when the selection is set programmatically through rich edit messages, the caret object does not send any events to indicate its new position.</span></span>

    <span data-ttu-id="26f01-134">使用 Riched20.dll 的所有應用程式都會出現此問題。</span><span class="sxs-lookup"><span data-stu-id="26f01-134">All applications that use Riched20.dll exhibit this problem.</span></span> <span data-ttu-id="26f01-135">使用較舊版本之 rich edit 控制項的應用程式，會根據選取專案正確地傳送事件。</span><span class="sxs-lookup"><span data-stu-id="26f01-135">Applications using earlier versions of the rich edit control correctly send events based on the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26f01-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="26f01-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26f01-137">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="26f01-137">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




