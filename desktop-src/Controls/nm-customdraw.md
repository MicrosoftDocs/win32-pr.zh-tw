---
title: 'NM_CUSTOMDRAW (Commctrl 的通知碼) '
description: 通知控制項的父視窗有關自訂繪圖作業的相關資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- NM_CUSTOMDRAW 通知碼 Windows 控制項
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
ms.openlocfilehash: d5f91f5197c7ecaf0ae4356fe00c48221a83ebd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464268"
---
# <a name="nm_customdraw-notification-code"></a><span data-ttu-id="d763d-105">NM \_ CUSTOMDRAW 通知碼</span><span class="sxs-lookup"><span data-stu-id="d763d-105">NM\_CUSTOMDRAW notification code</span></span>

<span data-ttu-id="d763d-106">通知控制項的父視窗有關自訂繪圖作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d763d-106">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="d763d-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="d763d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a><span data-ttu-id="d763d-108">參數</span><span class="sxs-lookup"><span data-stu-id="d763d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d763d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d763d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d763d-110">自訂繪圖相關結構的指標，其中包含繪圖作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d763d-110">A pointer to a custom draw-related structure that contains information about the drawing operation.</span></span> <span data-ttu-id="d763d-111">下列清單指定控制項及其相關聯的結構。</span><span class="sxs-lookup"><span data-stu-id="d763d-111">The following list specifies the controls and their associated structures.</span></span>



| <span data-ttu-id="d763d-112">控制</span><span class="sxs-lookup"><span data-stu-id="d763d-112">Control</span></span>                     | <span data-ttu-id="d763d-113">自訂繪圖結構</span><span class="sxs-lookup"><span data-stu-id="d763d-113">Custom Draw Structure</span></span>                    |
|-----------------------------|------------------------------------------|
| <span data-ttu-id="d763d-114">Rebar、標題和標頭</span><span class="sxs-lookup"><span data-stu-id="d763d-114">Rebar, trackbar, and header</span></span> | [<span data-ttu-id="d763d-115">**NMCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="d763d-115">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| <span data-ttu-id="d763d-116">清單檢視</span><span class="sxs-lookup"><span data-stu-id="d763d-116">List view</span></span>                   | [<span data-ttu-id="d763d-117">**NMLVCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="d763d-117">**NMLVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| <span data-ttu-id="d763d-118">工具提示</span><span class="sxs-lookup"><span data-stu-id="d763d-118">Tooltip</span></span>                     | [<span data-ttu-id="d763d-119">**NMTTCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="d763d-119">**NMTTCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| <span data-ttu-id="d763d-120">樹狀檢視</span><span class="sxs-lookup"><span data-stu-id="d763d-120">Tree view</span></span>                   | [<span data-ttu-id="d763d-121">**NMTVCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="d763d-121">**NMTVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| <span data-ttu-id="d763d-122">工具列</span><span class="sxs-lookup"><span data-stu-id="d763d-122">Toolbar</span></span>                     | [<span data-ttu-id="d763d-123">**NMTBCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="d763d-123">**NMTBCUSTOMDRAW**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d763d-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="d763d-124">Return value</span></span>

<span data-ttu-id="d763d-125">您的應用程式可以傳回的值取決於目前的繪圖階段。</span><span class="sxs-lookup"><span data-stu-id="d763d-125">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="d763d-126">相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。</span><span class="sxs-lookup"><span data-stu-id="d763d-126">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="d763d-127">您必須傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d763d-127">You must return one of the following values.</span></span>



| <span data-ttu-id="d763d-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d763d-128">Return code</span></span>                                                                                            | <span data-ttu-id="d763d-129">Description</span><span class="sxs-lookup"><span data-stu-id="d763d-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d763d-130"><dt>**CDRF \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="d763d-130"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="d763d-131">控制項將會自行繪製。</span><span class="sxs-lookup"><span data-stu-id="d763d-131">The control will draw itself.</span></span> <span data-ttu-id="d763d-132">它不會為此繪製迴圈傳送額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="d763d-132">It will not send additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="d763d-133">此旗標不可與任何其他旗標一起使用。</span><span class="sxs-lookup"><span data-stu-id="d763d-133">This flag cannot be used with any other flag.</span></span> <br/>                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="d763d-134"><dt>**CDRF \_ DOERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="d763d-134"><dt>**CDRF\_DOERASE**</dt></span></span> </dl>           | <span data-ttu-id="d763d-135">控制項只會繪製背景。</span><span class="sxs-lookup"><span data-stu-id="d763d-135">The control will only draw the background.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="d763d-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="d763d-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="d763d-137">您的應用程式已為專案指定新字型;控制項將會使用新的字型。</span><span class="sxs-lookup"><span data-stu-id="d763d-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="d763d-138">如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。</span><span class="sxs-lookup"><span data-stu-id="d763d-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="d763d-139">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d763d-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="d763d-140"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="d763d-140"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="d763d-141">控制項將會通知任何專案相關繪圖作業的父系。</span><span class="sxs-lookup"><span data-stu-id="d763d-141">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="d763d-142">它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="d763d-142">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="d763d-143">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d763d-143">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="d763d-144"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="d763d-144"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="d763d-145">控制項將會在清除專案之後通知父代。</span><span class="sxs-lookup"><span data-stu-id="d763d-145">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="d763d-146">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d763d-146">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="d763d-147"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="d763d-147"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="d763d-148">當整個控制項的繪製迴圈完成時，控制項將傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="d763d-148">The control will send an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code when the painting cycle for the entire control is complete.</span></span> <span data-ttu-id="d763d-149">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d763d-149">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="d763d-150"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="d763d-150"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="d763d-151">您的應用程式將會在[ \_ ](nm-customdraw.md)  \_ \| \_ 繪製每個清單視圖子集合之前，收到 CUSTOMDRAW 通知碼，其中 dwDrawStage 設定為 CDDS ITEMPREPAINT CDDS 子。</span><span class="sxs-lookup"><span data-stu-id="d763d-151">Your application will receive an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code with **dwDrawStage** set to CDDS\_ITEMPREPAINT \| CDDS\_SUBITEM before each list-view subitem is drawn.</span></span> <span data-ttu-id="d763d-152">然後，您可以分別為每個子項指定字型和色彩，或針對預設處理傳回 [**CDRF \_ DODEFAULT**](cdrf-constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="d763d-152">You can then specify font and color for each subitem separately or return [**CDRF\_DODEFAULT**](cdrf-constants.md) for default processing.</span></span> <span data-ttu-id="d763d-153">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d763d-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="d763d-154"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="d763d-154"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="d763d-155">您的應用程式會以手動方式繪製專案。</span><span class="sxs-lookup"><span data-stu-id="d763d-155">Your application drew the item manually.</span></span> <span data-ttu-id="d763d-156">控制項不會繪製專案。</span><span class="sxs-lookup"><span data-stu-id="d763d-156">The control will not draw the item.</span></span> <span data-ttu-id="d763d-157">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d763d-157">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="d763d-158"><dt>**CDRF \_ SKIPPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="d763d-158"><dt>**CDRF\_SKIPPOSTPAINT**</dt></span></span> </dl>     | <span data-ttu-id="d763d-159">控制項不會在專案周圍繪製焦點矩形。</span><span class="sxs-lookup"><span data-stu-id="d763d-159">The control will not draw the focus rectangle around an item.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="d763d-160">備註</span><span class="sxs-lookup"><span data-stu-id="d763d-160">Remarks</span></span>

<span data-ttu-id="d763d-161">目前，下列控制項支援自訂繪製功能：標頭、清單視圖、Rebar、工具列、工具提示、標題和樹狀檢視。</span><span class="sxs-lookup"><span data-stu-id="d763d-161">Currently, the following controls support custom draw functionality: header, list view, rebar, toolbar, tooltip, trackbar, and tree view.</span></span> <span data-ttu-id="d763d-162">如果您有應用程式資訊清單，以確保 Comctl32.dll 版本6可供使用，則按鈕控制項也支援自訂繪製。</span><span class="sxs-lookup"><span data-stu-id="d763d-162">Custom draw is also supported for button controls if you have an application manifest to ensure that Comctl32.dll version 6 is available.</span></span>

<span data-ttu-id="d763d-163">如果在對話程式中處理此訊息，您必須先將傳回值設定為視窗資料的一部分，然後再傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d763d-163">If this message is handled in a dialog procedure, you must set the return value as part of the window data before returning **TRUE**.</span></span> <span data-ttu-id="d763d-164">如需詳細資訊，請參閱 [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc)。</span><span class="sxs-lookup"><span data-stu-id="d763d-164">For more information, see [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span></span>

## <a name="requirements"></a><span data-ttu-id="d763d-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="d763d-165">Requirements</span></span>



| <span data-ttu-id="d763d-166">需求</span><span class="sxs-lookup"><span data-stu-id="d763d-166">Requirement</span></span> | <span data-ttu-id="d763d-167">值</span><span class="sxs-lookup"><span data-stu-id="d763d-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d763d-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d763d-168">Minimum supported client</span></span><br/> | <span data-ttu-id="d763d-169">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d763d-169">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d763d-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d763d-170">Minimum supported server</span></span><br/> | <span data-ttu-id="d763d-171">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d763d-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d763d-172">標頭</span><span class="sxs-lookup"><span data-stu-id="d763d-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="d763d-173"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d763d-173"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d763d-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d763d-174">See also</span></span>

<dl> <dt>

<span data-ttu-id="d763d-175">**概念**</span><span class="sxs-lookup"><span data-stu-id="d763d-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d763d-176">自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="d763d-176">Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

