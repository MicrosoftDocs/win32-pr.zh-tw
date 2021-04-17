---
title: 'NM_CUSTOMDRAW (工具列) 通知碼 (Commctrl) '
description: 由工具列傳送以通知其父視窗有關繪製作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e83a85f4-7955-411d-9a08-29f5b30158c5
keywords:
- NM_CUSTOMDRAW (工具列) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d1a33e6b7e9a26237813ec3a90e560f05dd9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509492"
---
# <a name="nm_customdraw-toolbar-notification-code"></a><span data-ttu-id="42266-105">NM \_ CUSTOMDRAW (工具列) 通知碼</span><span class="sxs-lookup"><span data-stu-id="42266-105">NM\_CUSTOMDRAW (toolbar) notification code</span></span>

<span data-ttu-id="42266-106">由工具列傳送以通知其父視窗有關繪製作業。</span><span class="sxs-lookup"><span data-stu-id="42266-106">Sent by a toolbar to notify its parent window about drawing operations.</span></span> <span data-ttu-id="42266-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="42266-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW
        
    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="42266-108">參數</span><span class="sxs-lookup"><span data-stu-id="42266-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42266-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42266-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42266-110">[版本 4.70](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="42266-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="42266-111">[**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42266-111">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="42266-112">此結構的 **dwItemSpec** 成員包含所繪製專案的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="42266-112">The **dwItemSpec** member of this structure contains the command identifier of the item being drawn.</span></span> <span data-ttu-id="42266-113">此結構的 **lItemlParam** 成員包含所繪製專案的 **dwData** 值。</span><span class="sxs-lookup"><span data-stu-id="42266-113">The **lItemlParam** member of this structure contains the **dwData** value for the item being drawn.</span></span>

<span data-ttu-id="42266-114">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="42266-114">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="42266-115">[**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42266-115">Pointer to an [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="42266-116">此結構之 **nmcd** 成員的 **dwItemSpec** 成員包含所繪製專案的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="42266-116">The **dwItemSpec** member of the **nmcd** member of this structure contains the command identifier of the item being drawn.</span></span> <span data-ttu-id="42266-117">此結構之 **nmcd** 成員的 **lItemlParam** 成員包含所繪製專案的 **dwData** 值。</span><span class="sxs-lookup"><span data-stu-id="42266-117">The **lItemlParam** member of the **nmcd** member of this structure contains the **dwData** value for the item being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42266-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="42266-118">Return value</span></span>

<span data-ttu-id="42266-119">您的應用程式可以傳回的值取決於目前的繪圖階段。</span><span class="sxs-lookup"><span data-stu-id="42266-119">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="42266-120">相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。</span><span class="sxs-lookup"><span data-stu-id="42266-120">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="42266-121">您必須傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="42266-121">You must return one of the following values.</span></span>



| <span data-ttu-id="42266-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="42266-122">Return code</span></span>                                                                                            | <span data-ttu-id="42266-123">Description</span><span class="sxs-lookup"><span data-stu-id="42266-123">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42266-124"><dt>**CDRF \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-124"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="42266-125">控制項將會自行繪製。</span><span class="sxs-lookup"><span data-stu-id="42266-125">The control will draw itself.</span></span> <span data-ttu-id="42266-126">它不會針對此繪製迴圈傳送任何額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="42266-126">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="42266-127">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-127">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="42266-128"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-128"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="42266-129">控制項將會通知任何專案相關繪圖作業的父系。</span><span class="sxs-lookup"><span data-stu-id="42266-129">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="42266-130">它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="42266-130">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="42266-131">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                         |
| <dl> <span data-ttu-id="42266-132"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-132"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="42266-133">控制項將會在清除專案之後通知父代。</span><span class="sxs-lookup"><span data-stu-id="42266-133">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="42266-134">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-134">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="42266-135"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-135"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="42266-136">控制項將會在繪製專案之後通知父系。</span><span class="sxs-lookup"><span data-stu-id="42266-136">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="42266-137">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-137">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="42266-138"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-138"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="42266-139">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="42266-139">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="42266-140">當正在繪製清單視圖子項目時，控制項將會通知父代。</span><span class="sxs-lookup"><span data-stu-id="42266-140">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="42266-141">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-141">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="42266-142"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-142"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="42266-143">您的應用程式已為專案指定新字型;控制項將會使用新的字型。</span><span class="sxs-lookup"><span data-stu-id="42266-143">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="42266-144">如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。</span><span class="sxs-lookup"><span data-stu-id="42266-144">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="42266-145">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-145">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="42266-146"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-146"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="42266-147">您的應用程式會以手動方式繪製專案。</span><span class="sxs-lookup"><span data-stu-id="42266-147">Your application drew the item manually.</span></span> <span data-ttu-id="42266-148">控制項不會繪製專案。</span><span class="sxs-lookup"><span data-stu-id="42266-148">The control will not draw the item.</span></span> <span data-ttu-id="42266-149">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-149">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="42266-150"><dt>**TBCDRF \_ BLENDICON**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-150"><dt>**TBCDRF\_BLENDICON**</dt></span></span> </dl>       | <span data-ttu-id="42266-151">[版本 5.00](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="42266-151">[Version 5.00](common-control-versions.md).</span></span> <span data-ttu-id="42266-152">將按鈕50百分比與背景混合。</span><span class="sxs-lookup"><span data-stu-id="42266-152">Blend the button 50 percent with the background.</span></span> <span data-ttu-id="42266-153">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="42266-154"><dt>**TBCDRF \_ NOBACKGROUND**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-154"><dt>**TBCDRF\_NOBACKGROUND**</dt></span></span> </dl>    | <span data-ttu-id="42266-155">[版本 5.00](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="42266-155">[Version 5.00](common-control-versions.md).</span></span> <span data-ttu-id="42266-156">不要繪製按鈕背景。</span><span class="sxs-lookup"><span data-stu-id="42266-156">Do not draw button background.</span></span> <span data-ttu-id="42266-157">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-157">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="42266-158"><dt>**TBCDRF \_ NOEDGES**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-158"><dt>**TBCDRF\_NOEDGES**</dt></span></span> </dl>         | <span data-ttu-id="42266-159">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="42266-159">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="42266-160">不要繪製按鈕邊緣。</span><span class="sxs-lookup"><span data-stu-id="42266-160">Do not draw button edges.</span></span> <span data-ttu-id="42266-161">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-161">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="42266-162"><dt>**TBCDRF \_ HILITEHOTTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-162"><dt>**TBCDRF\_HILITEHOTTRACK**</dt></span></span> </dl>  | <span data-ttu-id="42266-163">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="42266-163">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="42266-164">使用 [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw)結構的 **clrHighlightHotTrack** 成員來繪製熱追蹤專案的背景。</span><span class="sxs-lookup"><span data-stu-id="42266-164">Use the **clrHighlightHotTrack** member of the [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) structure to draw the background of hot-tracked items.</span></span> <span data-ttu-id="42266-165">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-165">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                        |
| <dl> <span data-ttu-id="42266-166"><dt>**TBCDRF \_ NOOFFSET**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-166"><dt>**TBCDRF\_NOOFFSET**</dt></span></span> </dl>        | <span data-ttu-id="42266-167">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="42266-167">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="42266-168">當按下時，請勿位移按鈕。</span><span class="sxs-lookup"><span data-stu-id="42266-168">Do not offset the button when pressed.</span></span> <span data-ttu-id="42266-169">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-169">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="42266-170"><dt>**TBCDRF \_ NOMARK**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-170"><dt>**TBCDRF\_NOMARK**</dt></span></span> </dl>          | <span data-ttu-id="42266-171">請勿繪製 [**\_ 標示了 TBSTATE**](toolbar-button-states.md)之專案的預設反白顯示。</span><span class="sxs-lookup"><span data-stu-id="42266-171">Do not draw default highlight of items that have the [**TBSTATE\_MARKED**](toolbar-button-states.md).</span></span> <span data-ttu-id="42266-172">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-172">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="42266-173"><dt>**TBCDRF \_ NOETCHEDEFFECT**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-173"><dt>**TBCDRF\_NOETCHEDEFFECT**</dt></span></span> </dl>  | <span data-ttu-id="42266-174">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="42266-174">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="42266-175">請勿針對停用的專案繪製蝕刻效果。</span><span class="sxs-lookup"><span data-stu-id="42266-175">Do not draw etched effect for disabled items.</span></span> <span data-ttu-id="42266-176">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="42266-176">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="42266-177"><dt>**TBCDRF \_ USECDCOLORS**</dt></span><span class="sxs-lookup"><span data-stu-id="42266-177"><dt>**TBCDRF\_USECDCOLORS**</dt></span></span> </dl>     | <span data-ttu-id="42266-178">[版本 6.00](common-control-versions.md)，僅限 **Windows Vista** 。</span><span class="sxs-lookup"><span data-stu-id="42266-178">[Version 6.00](common-control-versions.md), **Windows Vista** only.</span></span> <span data-ttu-id="42266-179">無論視覺化樣式為何，都可以使用自訂繪製色彩來轉譯文字。</span><span class="sxs-lookup"><span data-stu-id="42266-179">Use custom draw colors to render text regardless of visual style.</span></span><br/>                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="42266-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="42266-180">Requirements</span></span>



| <span data-ttu-id="42266-181">需求</span><span class="sxs-lookup"><span data-stu-id="42266-181">Requirement</span></span> | <span data-ttu-id="42266-182">值</span><span class="sxs-lookup"><span data-stu-id="42266-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42266-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42266-183">Minimum supported client</span></span><br/> | <span data-ttu-id="42266-184">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42266-184">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42266-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42266-185">Minimum supported server</span></span><br/> | <span data-ttu-id="42266-186">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42266-186">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42266-187">標頭</span><span class="sxs-lookup"><span data-stu-id="42266-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="42266-188"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="42266-188"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42266-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42266-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42266-190">使用自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="42266-190">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





