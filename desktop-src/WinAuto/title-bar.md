---
title: '標題列 (MSAA UI 元素參考) '
description: 視窗頂端的標題列會顯示應用程式定義的圖示和文字行。
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fee3642a67be85b27eac6a73ac7c452f2349d1
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374278"
---
# <a name="title-bar-msaa-ui-element-reference"></a><span data-ttu-id="b3411-103">標題列 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="b3411-103">Title Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="b3411-104">本主題描述用於 MSAA UI 元素參考的 **標題列** 物件。</span><span class="sxs-lookup"><span data-stu-id="b3411-104">This topic describes **Title Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="b3411-105">此處未說明如何在各種 UI 架構中建立 **標題列** 物件。</span><span class="sxs-lookup"><span data-stu-id="b3411-105">How to create **Title Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="b3411-106">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="b3411-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="b3411-107">視窗頂端的標題列會顯示應用程式定義的圖示和文字行。</span><span class="sxs-lookup"><span data-stu-id="b3411-107">The title bar at the top of a window displays an application-defined icon and line of text.</span></span> <span data-ttu-id="b3411-108">文字會指定應用程式的名稱，並指出視窗的用途。</span><span class="sxs-lookup"><span data-stu-id="b3411-108">The text specifies the name of the application and indicates the purpose of the window.</span></span> <span data-ttu-id="b3411-109">標題列也可以讓使用者使用滑鼠或其他指標裝置來移動視窗。</span><span class="sxs-lookup"><span data-stu-id="b3411-109">The title bar also makes it possible for the user to move the window using a mouse or other pointing device.</span></span>

<span data-ttu-id="b3411-110">標題列至少包含三個小按鈕，可最小化、最大化或還原，以及關閉與標題列相關聯的視窗。</span><span class="sxs-lookup"><span data-stu-id="b3411-110">Title bars contain at least three small buttons that minimize, maximize or restore, and close the window associated with the title bar.</span></span> <span data-ttu-id="b3411-111">標題列也包含即時線上說明按鈕。</span><span class="sxs-lookup"><span data-stu-id="b3411-111">Title bars also contain a context-sensitive Help button.</span></span> <span data-ttu-id="b3411-112">在 Far-East 版本的 Windows 作業系統中執行的應用程式也可能包含輸入法編輯器 (IME) 按鈕。</span><span class="sxs-lookup"><span data-stu-id="b3411-112">Applications running in the Far-East version of the Windows operating system may also contain Input Method Editor (IME) buttons.</span></span> <span data-ttu-id="b3411-113">Microsoft Active Accessibility 會將這些按鈕公開為標題列的子項目。</span><span class="sxs-lookup"><span data-stu-id="b3411-113">Microsoft Active Accessibility exposes these buttons as child elements of the title bar.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="b3411-114">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="b3411-114">IAccessible Methods</span></span>

<span data-ttu-id="b3411-115">標題列支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="b3411-115">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="b3411-116">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="b3411-116">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="b3411-117">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="b3411-117">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="b3411-118">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="b3411-118">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="b3411-119">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="b3411-119">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="b3411-120">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="b3411-120">IAccessible Properties</span></span>

<span data-ttu-id="b3411-121">標題列支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="b3411-121">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3411-122">屬性</span><span class="sxs-lookup"><span data-stu-id="b3411-122">Property</span></span></th>
<th><span data-ttu-id="b3411-123">註解</span><span class="sxs-lookup"><span data-stu-id="b3411-123">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3411-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3411-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="b3411-125"><strong>ChildCount</strong>屬性為五。</span><span class="sxs-lookup"><span data-stu-id="b3411-125">The <strong>ChildCount</strong> property is five.</span></span> <span data-ttu-id="b3411-126"><strong>ChildCount</strong>屬性包含輸入法和上下文相關的 [說明] 按鈕（即使未顯示）。</span><span class="sxs-lookup"><span data-stu-id="b3411-126">The <strong>ChildCount</strong> property includes the IME and context-sensitive Help buttons even when they are not displayed.</span></span> <span data-ttu-id="b3411-127">未顯示的按鈕具有 [ <strong>狀態</strong> ] 屬性 <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="b3411-127">Buttons that are not displayed have the <strong>State</strong> property <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3411-128"><strong>get_accDescription</strong></span><span class="sxs-lookup"><span data-stu-id="b3411-128"><strong>get_accDescription</strong></span></span></td>
<td><span data-ttu-id="b3411-129">標題列本身的 [ <strong>描述</strong> ] 屬性是： &quot; 顯示視窗的名稱，並且包含操作控制項的控制項。 &quot; 標題列中的子按鈕具有下列描述：</span><span class="sxs-lookup"><span data-stu-id="b3411-129">The <strong>Description</strong> property of the title bar itself is: &quot;Displays the name of the window and contains controls to manipulate it.&quot; The child buttons in the title bar have the following descriptions:</span></span><br/>
<ul>
<li><span data-ttu-id="b3411-130">&quot;將視窗移出</span><span class="sxs-lookup"><span data-stu-id="b3411-130">&quot;Moves the window out of</span></span></li>
<li><span data-ttu-id="b3411-131">&quot;讓視窗填滿</span><span class="sxs-lookup"><span data-stu-id="b3411-131">&quot;Makes the window full</span></span></li>
<li><span data-ttu-id="b3411-132">&quot;將最小化或</span><span class="sxs-lookup"><span data-stu-id="b3411-132">&quot;Puts a minimized or</span></span></li>
<li><span data-ttu-id="b3411-133">&quot;關閉視窗&quot;</span><span class="sxs-lookup"><span data-stu-id="b3411-133">&quot;Closes the window&quot;</span></span></li>
<li><span data-ttu-id="b3411-134">&quot;進入或離開內容-</span><span class="sxs-lookup"><span data-stu-id="b3411-134">&quot;Enters or leaves context-</span></span></li>
<li><span data-ttu-id="b3411-135">&quot;按下按鍵時顯示鍵盤&quot;</span><span class="sxs-lookup"><span data-stu-id="b3411-135">&quot;Brings up the keyboard when pressed&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3411-136"><strong>get_accName</strong></span><span class="sxs-lookup"><span data-stu-id="b3411-136"><strong>get_accName</strong></span></span></td>
<td><span data-ttu-id="b3411-137">標題列本身不支援 <strong>Name</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="b3411-137">The title bar itself does not support the <strong>Name</strong> property.</span></span> <span data-ttu-id="b3411-138">標題列中的子按鈕具有下列名稱：</span><span class="sxs-lookup"><span data-stu-id="b3411-138">The child buttons in the title bar have the following names:</span></span>
<ul>
<li><span data-ttu-id="b3411-139">&quot;最小化&quot;</span><span class="sxs-lookup"><span data-stu-id="b3411-139">&quot;Minimize&quot;</span></span></li>
<li><span data-ttu-id="b3411-140">&quot;最大化 &quot; 或 &quot; 還原 &quot;</span><span class="sxs-lookup"><span data-stu-id="b3411-140">&quot;Maximize&quot; or &quot;Restore&quot;,</span></span></li>
<li><span data-ttu-id="b3411-141">&quot;關閉&quot;</span><span class="sxs-lookup"><span data-stu-id="b3411-141">&quot;Close&quot;</span></span></li>
<li><span data-ttu-id="b3411-142">&quot;內容說明&quot;</span><span class="sxs-lookup"><span data-stu-id="b3411-142">&quot;Context help&quot;</span></span></li>
<li><span data-ttu-id="b3411-143">&quot;IME&quot;</span><span class="sxs-lookup"><span data-stu-id="b3411-143">&quot;IME&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3411-144"><strong>get_accParent</strong></span><span class="sxs-lookup"><span data-stu-id="b3411-144"><strong>get_accParent</strong></span></span></td>
<td><span data-ttu-id="b3411-145">標題列的 <strong>父</strong> 屬性是主應用程式視窗 ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) 與標題列具有相同的應用程式定義視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="b3411-145">The <strong>Parent</strong> property of the title bar is the main application window ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) that has the same application-defined window class name as the title bar.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3411-146"><strong>get_accRole</strong></span><span class="sxs-lookup"><span data-stu-id="b3411-146"><strong>get_accRole</strong></span></span></td>
<td><span data-ttu-id="b3411-147"><strong>Role</strong>屬性為<a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="b3411-147">The <strong>Role</strong> property is <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span></span> <span data-ttu-id="b3411-148">標題列中的子按鈕具有 <strong>角色</strong> 屬性 <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="b3411-148">The child buttons in the title bar have the <strong>Role</strong> property <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3411-149"><strong>get_accState</strong></span><span class="sxs-lookup"><span data-stu-id="b3411-149"><strong>get_accState</strong></span></span></td>
<td><span data-ttu-id="b3411-150">標題列和子按鈕的 [<strong>狀態</strong>] 屬性可以是下列一或多個<a href="object-state-constants.md">值</a>的組合： <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3411-150">The <strong>State</strong> property for the title bar and the child buttons can be a combination of one or more of the following <a href="object-state-constants.md">values</a>: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3411-151"><strong>get_accValue</strong></span><span class="sxs-lookup"><span data-stu-id="b3411-151"><strong>get_accValue</strong></span></span></td>
<td><span data-ttu-id="b3411-152"><strong>Value</strong>屬性是與標題列中顯示的文字相同的字串。</span><span class="sxs-lookup"><span data-stu-id="b3411-152">The <strong>Value</strong> property is a string that is the same as the text displayed in the title bar.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="b3411-153">備註</span><span class="sxs-lookup"><span data-stu-id="b3411-153">Notes</span></span>

-   <span data-ttu-id="b3411-154">雖然應用程式的標題列具有 [**狀態] 屬性旗** 標 [**狀態系統可 \_ \_ 設定**](object-state-constants.md)目標，但 **它的狀態旗標**[**狀態系統並沒有 \_ \_ 焦點**](object-state-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="b3411-154">Although an application's title bar has the **State** property flag [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md), it never has the **State** flag [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md).</span></span> <span data-ttu-id="b3411-155">將焦點設定為標題列物件將焦點放在應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="b3411-155">Setting focus to a title bar object focuses the application window.</span></span>
-   <span data-ttu-id="b3411-156">因為標題列物件不支援 [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)，所以標題列上的按鈕是簡單的元素。</span><span class="sxs-lookup"><span data-stu-id="b3411-156">Because the title bar object does not support [**get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), the buttons on the title bar are simple elements.</span></span> <span data-ttu-id="b3411-157">它們本身不支援 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。</span><span class="sxs-lookup"><span data-stu-id="b3411-157">They do not support the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface themselves.</span></span> <span data-ttu-id="b3411-158">標題列物件提供這些子按鈕的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b3411-158">The title bar object provides information about these child buttons.</span></span>
-   <span data-ttu-id="b3411-159">由於標題列無法取得焦點且沒有預設動作，因此不支援此控制項的 [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) 和 [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) 方法。</span><span class="sxs-lookup"><span data-stu-id="b3411-159">Because title bars do not get focus and have no default action, the [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) and [**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) methods are not supported for this control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3411-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3411-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3411-161">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="b3411-161">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





