---
title: 平面捲軸
description: 本節包含用來控制一般捲軸之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e611e8d5755d119a8c24bdbccb9f10408d3d7d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839599"
---
# <a name="flat-scroll-bar"></a><span data-ttu-id="6f374-103">平面捲軸</span><span class="sxs-lookup"><span data-stu-id="6f374-103">Flat Scroll Bar</span></span>

<span data-ttu-id="6f374-104">本節包含用來控制一般捲軸之程式設計項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6f374-104">This section contains information about the programming elements used to control flat scroll bars.</span></span>

### <a name="overviews"></a><span data-ttu-id="6f374-105">概觀</span><span class="sxs-lookup"><span data-stu-id="6f374-105">Overviews</span></span>



| <span data-ttu-id="6f374-106">主題</span><span class="sxs-lookup"><span data-stu-id="6f374-106">Topic</span></span>                                    | <span data-ttu-id="6f374-107">目錄</span><span class="sxs-lookup"><span data-stu-id="6f374-107">Contents</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f374-108">平面捲軸</span><span class="sxs-lookup"><span data-stu-id="6f374-108">Flat Scroll Bars</span></span>](flat-scroll-bars.md) | <span data-ttu-id="6f374-109">Microsoft Internet Explorer 4.0 推出了一個新的視覺技術，稱為「一般捲軸」。</span><span class="sxs-lookup"><span data-stu-id="6f374-109">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="6f374-110">功能上，一般捲軸的行為就像標準捲軸。</span><span class="sxs-lookup"><span data-stu-id="6f374-110">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="6f374-111">不同之處在于，您可以自訂其外觀，以比標準捲軸更大的範圍。</span><span class="sxs-lookup"><span data-stu-id="6f374-111">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="6f374-112">函式</span><span class="sxs-lookup"><span data-stu-id="6f374-112">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6f374-113">主題</span><span class="sxs-lookup"><span data-stu-id="6f374-113">Topic</span></span></th>
<th><span data-ttu-id="6f374-114">目錄</span><span class="sxs-lookup"><span data-stu-id="6f374-114">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f374-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="6f374-116">啟用或停用一或兩個平面捲軸方向按鈕。</span><span class="sxs-lookup"><span data-stu-id="6f374-116">Enables or disables one or both flat scroll bar direction buttons.</span></span> <span data-ttu-id="6f374-117">如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="6f374-117">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f374-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="6f374-119">取得平面捲軸的資訊。</span><span class="sxs-lookup"><span data-stu-id="6f374-119">Gets the information for a flat scroll bar.</span></span> <span data-ttu-id="6f374-120">如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="6f374-120">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f374-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="6f374-122">取得平面捲軸的捲動方塊位置。</span><span class="sxs-lookup"><span data-stu-id="6f374-122">Gets the thumb position in a flat scroll bar.</span></span> <span data-ttu-id="6f374-123">如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="6f374-123">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f374-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="6f374-125">取得平面捲軸的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f374-125">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="6f374-126">這個函數也可以用來判斷是否已針對此視窗呼叫 <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="6f374-126">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f374-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span></span></td>
<td><span data-ttu-id="6f374-128">取得平面捲軸的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f374-128">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="6f374-129">這個函數也可以用來判斷是否已針對此視窗呼叫 <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="6f374-129">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="6f374-130">這等同于 <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="6f374-130">This is identical to <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f374-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="6f374-132">取得平面捲軸的捲軸範圍。</span><span class="sxs-lookup"><span data-stu-id="6f374-132">Gets the scroll range for a flat scroll bar.</span></span> <span data-ttu-id="6f374-133">如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="6f374-133">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f374-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="6f374-135">設定一般捲軸的資訊。</span><span class="sxs-lookup"><span data-stu-id="6f374-135">Sets the information for a flat scroll bar.</span></span> <span data-ttu-id="6f374-136">如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="6f374-136">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f374-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="6f374-138">將 thumb 的目前位置設定為平面捲軸。</span><span class="sxs-lookup"><span data-stu-id="6f374-138">Sets the current position of the thumb in a flat scroll bar.</span></span> <span data-ttu-id="6f374-139">如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="6f374-139">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f374-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="6f374-141">設定平面捲軸的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f374-141">Sets the properties for a flat scroll bar.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f374-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="6f374-143">設定平面捲軸的捲軸範圍。</span><span class="sxs-lookup"><span data-stu-id="6f374-143">Sets the scroll range of a flat scroll bar.</span></span> <span data-ttu-id="6f374-144">如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="6f374-144">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f374-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="6f374-146">顯示或隱藏平面捲軸。</span><span class="sxs-lookup"><span data-stu-id="6f374-146">Shows or hides a flat scroll bar.</span></span> <span data-ttu-id="6f374-147">如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="6f374-147">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f374-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="6f374-149">初始化特定視窗的平面捲軸。</span><span class="sxs-lookup"><span data-stu-id="6f374-149">Initializes flat scroll bars for a particular window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f374-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f374-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="6f374-151">取消初始化特定視窗的平面捲軸。</span><span class="sxs-lookup"><span data-stu-id="6f374-151">Uninitializes flat scroll bars for a particular window.</span></span> <span data-ttu-id="6f374-152">指定的視窗將會還原為標準捲軸。</span><span class="sxs-lookup"><span data-stu-id="6f374-152">The specified window will revert to standard scroll bars.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

 





