---
title: 'NM_CUSTOMDRAW (工具提示) 通知碼 (Commctrl) '
description: 由工具提示控制項傳送，以通知其父視窗有關繪製作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- NM_CUSTOMDRAW (工具提示) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 9ce1047f63c8580051f7d57abf3308bde37238a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686667"
---
# <a name="nm_customdraw-tooltip-notification-code"></a><span data-ttu-id="6c498-105">NM \_ CUSTOMDRAW (工具提示) 通知碼</span><span class="sxs-lookup"><span data-stu-id="6c498-105">NM\_CUSTOMDRAW (tooltip) notification code</span></span>

<span data-ttu-id="6c498-106">由工具提示控制項傳送，以通知其父視窗有關繪製作業。</span><span class="sxs-lookup"><span data-stu-id="6c498-106">Sent by a tooltip control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="6c498-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="6c498-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6c498-108">參數</span><span class="sxs-lookup"><span data-stu-id="6c498-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c498-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c498-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c498-110">[**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6c498-110">Pointer to an [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) structure that contains information about the drawing operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c498-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c498-111">Return value</span></span>

<span data-ttu-id="6c498-112">您的應用程式可以傳回的值取決於目前的繪圖階段。</span><span class="sxs-lookup"><span data-stu-id="6c498-112">The value that your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="6c498-113">相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。</span><span class="sxs-lookup"><span data-stu-id="6c498-113">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="6c498-114">您必須傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6c498-114">You must return one of the following values.</span></span>



| <span data-ttu-id="6c498-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6c498-115">Return code</span></span>                                                                                            | <span data-ttu-id="6c498-116">Description</span><span class="sxs-lookup"><span data-stu-id="6c498-116">Description</span></span>                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c498-117"><dt>**CDRF \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="6c498-117"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="6c498-118">控制項將會自行繪製。</span><span class="sxs-lookup"><span data-stu-id="6c498-118">The control will draw itself.</span></span> <span data-ttu-id="6c498-119">它不會針對此繪製迴圈傳送任何額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="6c498-119">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="6c498-120">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6c498-120">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="6c498-121"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="6c498-121"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="6c498-122">控制項將會通知任何專案相關繪圖作業的父系。</span><span class="sxs-lookup"><span data-stu-id="6c498-122">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="6c498-123">它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="6c498-123">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="6c498-124">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6c498-124">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                            |
| <dl> <span data-ttu-id="6c498-125"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="6c498-125"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="6c498-126">控制項將會在清除專案之後通知父代。</span><span class="sxs-lookup"><span data-stu-id="6c498-126">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="6c498-127">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6c498-127">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="6c498-128"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="6c498-128"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="6c498-129">控制項將會在繪製專案之後通知父系。</span><span class="sxs-lookup"><span data-stu-id="6c498-129">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="6c498-130">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6c498-130">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="6c498-131"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="6c498-131"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="6c498-132">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="6c498-132">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="6c498-133">當正在繪製清單視圖子項目時，控制項將會通知父代。</span><span class="sxs-lookup"><span data-stu-id="6c498-133">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="6c498-134">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6c498-134">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="6c498-135"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="6c498-135"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="6c498-136">您的應用程式為專案指定了新的字型。</span><span class="sxs-lookup"><span data-stu-id="6c498-136">Your application specified a new font for the item.</span></span> <span data-ttu-id="6c498-137">控制項將會使用新的字型。</span><span class="sxs-lookup"><span data-stu-id="6c498-137">The control will use the new font.</span></span> <span data-ttu-id="6c498-138">如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。</span><span class="sxs-lookup"><span data-stu-id="6c498-138">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="6c498-139">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6c498-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="6c498-140"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="6c498-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="6c498-141">您的應用程式會以手動方式繪製專案。</span><span class="sxs-lookup"><span data-stu-id="6c498-141">Your application drew the item manually.</span></span> <span data-ttu-id="6c498-142">控制項不會繪製專案。</span><span class="sxs-lookup"><span data-stu-id="6c498-142">The control will not draw the item.</span></span> <span data-ttu-id="6c498-143">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6c498-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="6c498-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c498-144">Requirements</span></span>



| <span data-ttu-id="6c498-145">需求</span><span class="sxs-lookup"><span data-stu-id="6c498-145">Requirement</span></span> | <span data-ttu-id="6c498-146">值</span><span class="sxs-lookup"><span data-stu-id="6c498-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c498-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c498-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6c498-148">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c498-148">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c498-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c498-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6c498-150">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c498-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c498-151">標頭</span><span class="sxs-lookup"><span data-stu-id="6c498-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c498-152"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c498-152"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c498-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c498-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c498-154">使用自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="6c498-154">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





