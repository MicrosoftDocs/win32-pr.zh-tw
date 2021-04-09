---
title: 'NM_CUSTOMDRAW (樹狀檢視) 通知碼 (Commctrl) '
description: 由樹狀檢視控制項傳送，以通知其父視窗有關繪製作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- NM_CUSTOMDRAW (樹狀檢視) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 2bb3f7b44748c2ac9c5b9651c079a8b90df0c508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843088"
---
# <a name="nm_customdraw-tree-view-notification-code"></a><span data-ttu-id="97d27-105">NM \_ CUSTOMDRAW (樹狀檢視) 通知碼</span><span class="sxs-lookup"><span data-stu-id="97d27-105">NM\_CUSTOMDRAW (tree view) notification code</span></span>

<span data-ttu-id="97d27-106">由樹狀檢視控制項傳送，以通知其父視窗有關繪製作業。</span><span class="sxs-lookup"><span data-stu-id="97d27-106">Sent by a tree-view control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="97d27-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="97d27-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="97d27-108">參數</span><span class="sxs-lookup"><span data-stu-id="97d27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97d27-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97d27-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97d27-110">[**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw)結構的指標，其中包含和接收繪圖作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="97d27-110">Pointer to an [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure that contains and receives information about the drawing operation.</span></span> <span data-ttu-id="97d27-111">此結構之 **nmcd** 成員的 **dwItemSpec** 成員包含所繪製專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="97d27-111">The **dwItemSpec** member of the **nmcd** member of this structure contains the handle of the item being drawn.</span></span> <span data-ttu-id="97d27-112">此結構之 **nmcd** 成員的 **lItemlParam** 成員包含所繪製專案的 *lParam* 。</span><span class="sxs-lookup"><span data-stu-id="97d27-112">The **lItemlParam** member of the **nmcd** member of this structure contains the *lParam* of the item being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97d27-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="97d27-113">Return value</span></span>

<span data-ttu-id="97d27-114">您的應用程式可以傳回的值取決於目前的繪圖階段。</span><span class="sxs-lookup"><span data-stu-id="97d27-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="97d27-115">相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。</span><span class="sxs-lookup"><span data-stu-id="97d27-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="97d27-116">您必須傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="97d27-116">You must return one of the following values.</span></span>



| <span data-ttu-id="97d27-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="97d27-117">Return code</span></span>                                                                                            | <span data-ttu-id="97d27-118">Description</span><span class="sxs-lookup"><span data-stu-id="97d27-118">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="97d27-119"><dt>**CDRF \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="97d27-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="97d27-120">控制項會自行繪製。</span><span class="sxs-lookup"><span data-stu-id="97d27-120">The control draws itself.</span></span> <span data-ttu-id="97d27-121">它不會針對此繪製迴圈傳送任何額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 碼。</span><span class="sxs-lookup"><span data-stu-id="97d27-121">It does not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) codes for this paint cycle.</span></span> <span data-ttu-id="97d27-122">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="97d27-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="97d27-123"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="97d27-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="97d27-124">控制項會通知任何專案相關繪圖作業的父系。</span><span class="sxs-lookup"><span data-stu-id="97d27-124">The control notifies the parent of any item-related drawing operations.</span></span> <span data-ttu-id="97d27-125">它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="97d27-125">It sends [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="97d27-126">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="97d27-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                |
| <dl> <span data-ttu-id="97d27-127"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="97d27-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="97d27-128">控制項在清除專案之後，會通知父代。當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="97d27-128">The control notifies the parent after erasing an item.This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="97d27-129"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="97d27-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="97d27-130">控制項會在繪製專案之後通知父系。</span><span class="sxs-lookup"><span data-stu-id="97d27-130">The control notifies the parent after painting an item.</span></span> <span data-ttu-id="97d27-131">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="97d27-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="97d27-132"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="97d27-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | [<span data-ttu-id="97d27-133">版本4.71。</span><span class="sxs-lookup"><span data-stu-id="97d27-133">Version 4.71.</span></span>](common-control-versions.md) <span data-ttu-id="97d27-134">繪製清單視圖子項目時，控制項會通知父系。</span><span class="sxs-lookup"><span data-stu-id="97d27-134">The control notifies the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="97d27-135">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="97d27-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="97d27-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="97d27-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="97d27-137">您的應用程式已為專案指定新字型;控制項將會使用新的字型。</span><span class="sxs-lookup"><span data-stu-id="97d27-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="97d27-138">如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。</span><span class="sxs-lookup"><span data-stu-id="97d27-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="97d27-139">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="97d27-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="97d27-140"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="97d27-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="97d27-141">您的應用程式會以手動方式繪製專案。</span><span class="sxs-lookup"><span data-stu-id="97d27-141">Your application drew the item manually.</span></span> <span data-ttu-id="97d27-142">控制項不會繪製專案。</span><span class="sxs-lookup"><span data-stu-id="97d27-142">The control will not draw the item.</span></span> <span data-ttu-id="97d27-143">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="97d27-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="97d27-144">備註</span><span class="sxs-lookup"><span data-stu-id="97d27-144">Remarks</span></span>

[<span data-ttu-id="97d27-145">版本5.80。</span><span class="sxs-lookup"><span data-stu-id="97d27-145">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="97d27-146">如果您藉由傳回 [**CDRF \_ NEWFONT**](cdrf-constants.md)來變更字型，則樹狀檢視控制項可能會顯示裁剪的文字。</span><span class="sxs-lookup"><span data-stu-id="97d27-146">If you change the font by returning [**CDRF\_NEWFONT**](cdrf-constants.md), the tree-view control might display clipped text.</span></span> <span data-ttu-id="97d27-147">這是與舊版通用控制項的回溯相容性所需的行為。</span><span class="sxs-lookup"><span data-stu-id="97d27-147">This behavior is necessary for backward compatibility with earlier versions of the common controls.</span></span> <span data-ttu-id="97d27-148">如果您想要變更樹狀檢視控制項的字型，則在將任何專案加入至控制項之前，如果您將 *wParam* 值設定為5，則會得到更 [**好的結果 \_**](ccm-setversion.md) 。</span><span class="sxs-lookup"><span data-stu-id="97d27-148">If you want to change the font of a tree-view control, you will get better results if you send a [**CCM\_SETVERSION**](ccm-setversion.md) message with the *wParam* value set to 5 before adding any items to the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="97d27-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="97d27-149">Requirements</span></span>



| <span data-ttu-id="97d27-150">需求</span><span class="sxs-lookup"><span data-stu-id="97d27-150">Requirement</span></span> | <span data-ttu-id="97d27-151">值</span><span class="sxs-lookup"><span data-stu-id="97d27-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97d27-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97d27-152">Minimum supported client</span></span><br/> | <span data-ttu-id="97d27-153">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97d27-153">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97d27-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97d27-154">Minimum supported server</span></span><br/> | <span data-ttu-id="97d27-155">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97d27-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97d27-156">標頭</span><span class="sxs-lookup"><span data-stu-id="97d27-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="97d27-157"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="97d27-157"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97d27-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97d27-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d27-159">使用自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="97d27-159">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





