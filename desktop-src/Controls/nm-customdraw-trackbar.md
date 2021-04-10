---
title: 'NM_CUSTOMDRAW (的)  (Commctrl 通知碼) '
description: 由 [資料提示] 控制項傳送，以通知其父視窗關於繪圖作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- NM_CUSTOMDRAW (的程式碼段) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 68ebbffd531fb44e2491d72954ce111db208f2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106620"
---
# <a name="nm_customdraw-trackbar-notification-code"></a><span data-ttu-id="bbf31-105">NM \_ CUSTOMDRAW (的) 通知碼</span><span class="sxs-lookup"><span data-stu-id="bbf31-105">NM\_CUSTOMDRAW (trackbar) notification code</span></span>

<span data-ttu-id="bbf31-106">由 [資料提示] 控制項傳送，以通知其父視窗關於繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="bbf31-106">Sent by a trackbar control to notify its parent windows about drawing operations.</span></span> <span data-ttu-id="bbf31-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="bbf31-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="bbf31-108">參數</span><span class="sxs-lookup"><span data-stu-id="bbf31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbf31-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbf31-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbf31-110">[**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bbf31-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="bbf31-111">此結構的 **dwItemSpec** 成員會包含其中一個 [自訂繪製值](custom-draw-values.md) ，指出正在繪製控制項的哪個部分。</span><span class="sxs-lookup"><span data-stu-id="bbf31-111">The **dwItemSpec** member of this structure will contain one of the [Custom Draw Values](custom-draw-values.md) that indicates which part of the control is being drawn.</span></span> <span data-ttu-id="bbf31-112">[可見度] 控制項會將下列值插入此結構的 **dwItemSpec** 成員，以識別所繪製之控制項的部分：</span><span class="sxs-lookup"><span data-stu-id="bbf31-112">Trackbar controls insert the following values into the **dwItemSpec** member of this structure to identify the portion of the control being drawn:</span></span>



| <span data-ttu-id="bbf31-113">值</span><span class="sxs-lookup"><span data-stu-id="bbf31-113">Value</span></span>                                                                                                                                                      | <span data-ttu-id="bbf31-114">意義</span><span class="sxs-lookup"><span data-stu-id="bbf31-114">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="bbf31-115"><dt>**TBCD \_ 通道**</dt></span><span class="sxs-lookup"><span data-stu-id="bbf31-115"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="bbf31-116">識別 [對齊程式] 控制項的 thumb 標記所投影的通道。</span><span class="sxs-lookup"><span data-stu-id="bbf31-116">Identifies the channel that the trackbar control's thumb marker slides along.</span></span> <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="bbf31-117"><dt>**TBCD \_ THUMB**</dt></span><span class="sxs-lookup"><span data-stu-id="bbf31-117"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="bbf31-118">識別 [資料指標] 控制項的 [thumb] 標記。</span><span class="sxs-lookup"><span data-stu-id="bbf31-118">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="bbf31-119">這是使用者移動之控制項的部分。</span><span class="sxs-lookup"><span data-stu-id="bbf31-119">This is the portion of the control that the user moves.</span></span> <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="bbf31-120"><dt>**TBCD \_ TICS**</dt></span><span class="sxs-lookup"><span data-stu-id="bbf31-120"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="bbf31-121">識別出現在 [側邊] 控制項邊緣的遞增刻度。</span><span class="sxs-lookup"><span data-stu-id="bbf31-121">Identifies the increment tick marks that appear along the edge of the trackbar control.</span></span> <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbf31-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbf31-122">Return value</span></span>

<span data-ttu-id="bbf31-123">您的應用程式可以傳回的值取決於目前的繪圖階段。</span><span class="sxs-lookup"><span data-stu-id="bbf31-123">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="bbf31-124">相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。</span><span class="sxs-lookup"><span data-stu-id="bbf31-124">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="bbf31-125">您必須傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bbf31-125">You must return one of the following values.</span></span>



| <span data-ttu-id="bbf31-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bbf31-126">Return code</span></span>                                                                                            | <span data-ttu-id="bbf31-127">Description</span><span class="sxs-lookup"><span data-stu-id="bbf31-127">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bbf31-128"><dt>**CDRF \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="bbf31-128"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="bbf31-129">控制項將會自行繪製。</span><span class="sxs-lookup"><span data-stu-id="bbf31-129">The control will draw itself.</span></span> <span data-ttu-id="bbf31-130">它不會針對此繪製迴圈傳送任何額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="bbf31-130">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="bbf31-131">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bbf31-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="bbf31-132"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="bbf31-132"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="bbf31-133">控制項將會通知任何專案相關繪圖作業的父系。</span><span class="sxs-lookup"><span data-stu-id="bbf31-133">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="bbf31-134">它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="bbf31-134">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="bbf31-135">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bbf31-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                         |
| <dl> <span data-ttu-id="bbf31-136"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="bbf31-136"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="bbf31-137">控制項將會在清除專案之後通知父代。</span><span class="sxs-lookup"><span data-stu-id="bbf31-137">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="bbf31-138">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bbf31-138">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="bbf31-139"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="bbf31-139"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="bbf31-140">控制項將會在繪製專案之後通知父系。</span><span class="sxs-lookup"><span data-stu-id="bbf31-140">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="bbf31-141">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bbf31-141">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="bbf31-142"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="bbf31-142"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="bbf31-143">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="bbf31-143">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="bbf31-144">當正在繪製清單視圖子項目時，控制項將會通知父代。</span><span class="sxs-lookup"><span data-stu-id="bbf31-144">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="bbf31-145">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bbf31-145">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="bbf31-146"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="bbf31-146"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="bbf31-147">您的應用程式已為專案指定新字型;控制項將會使用新的字型。</span><span class="sxs-lookup"><span data-stu-id="bbf31-147">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="bbf31-148">如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。</span><span class="sxs-lookup"><span data-stu-id="bbf31-148">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="bbf31-149">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bbf31-149">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="bbf31-150"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="bbf31-150"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="bbf31-151">您的應用程式會以手動方式繪製專案。</span><span class="sxs-lookup"><span data-stu-id="bbf31-151">Your application drew the item manually.</span></span> <span data-ttu-id="bbf31-152">控制項不會繪製專案。</span><span class="sxs-lookup"><span data-stu-id="bbf31-152">The control will not draw the item.</span></span> <span data-ttu-id="bbf31-153">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bbf31-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="bbf31-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbf31-154">Requirements</span></span>



| <span data-ttu-id="bbf31-155">需求</span><span class="sxs-lookup"><span data-stu-id="bbf31-155">Requirement</span></span> | <span data-ttu-id="bbf31-156">值</span><span class="sxs-lookup"><span data-stu-id="bbf31-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf31-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbf31-157">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf31-158">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbf31-158">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbf31-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbf31-159">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf31-160">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbf31-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbf31-161">標頭</span><span class="sxs-lookup"><span data-stu-id="bbf31-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbf31-162"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bbf31-162"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbf31-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbf31-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf31-164">使用自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="bbf31-164">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





