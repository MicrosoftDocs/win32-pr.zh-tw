---
title: 'NM_CUSTOMDRAW (清單視圖) 通知碼 (Commctrl) '
description: 由清單視圖控制項傳送，以通知其父視窗關於繪圖作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 4e9b91e3-d042-4fd0-b063-a9e6ea9ad564
keywords:
- NM_CUSTOMDRAW (清單視圖) 通知碼 Windows 控制項
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
ms.openlocfilehash: 19d8927006f3a6a7e5543f2b072d24469a73a7ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106632"
---
# <a name="nm_customdraw-list-view-notification-code"></a><span data-ttu-id="f9d9d-105">NM \_ CUSTOMDRAW (清單視圖) 通知碼</span><span class="sxs-lookup"><span data-stu-id="f9d9d-105">NM\_CUSTOMDRAW (list view) notification code</span></span>

<span data-ttu-id="f9d9d-106">由清單視圖控制項傳送，以通知其父視窗關於繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-106">Sent by a list-view control to notify its parent windows about drawing operations.</span></span> <span data-ttu-id="f9d9d-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f9d9d-108">參數</span><span class="sxs-lookup"><span data-stu-id="f9d9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9d9d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9d9d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9d9d-110">[**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-110">Pointer to a [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="f9d9d-111">此結構（ **nmcd**）的第一個成員是指向 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-111">The first member of this structure, **nmcd**, is a pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure.</span></span> <span data-ttu-id="f9d9d-112">**Nmcd** 所指向之結構的 **dwItemSpec** 成員包含所繪製專案的識別碼，而 **lItemlParam** 成員包含其應用程式定義的資料。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-112">The **dwItemSpec** member of the structure pointed to by **nmcd** contains the identifier of the item being drawn and the **lItemlParam** member contains its application-defined data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9d9d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9d9d-113">Return value</span></span>

<span data-ttu-id="f9d9d-114">您的應用程式可以傳回的值取決於目前的繪圖階段。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="f9d9d-115">相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="f9d9d-116">您必須傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-116">You must return one of the following values.</span></span>



| <span data-ttu-id="f9d9d-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f9d9d-117">Return code</span></span>                                                                                            | <span data-ttu-id="f9d9d-118">Description</span><span class="sxs-lookup"><span data-stu-id="f9d9d-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9d9d-119"><dt>**CDRF \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="f9d9d-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="f9d9d-120">控制項將會自行繪製。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-120">The control will draw itself.</span></span> <span data-ttu-id="f9d9d-121">它不會針對此繪製迴圈傳送任何額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-121">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="f9d9d-122">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="f9d9d-123"><dt>**CDRF \_ DOERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="f9d9d-123"><dt>**CDRF\_DOERASE**</dt></span></span> </dl>           | <span data-ttu-id="f9d9d-124">Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-124">Windows Vista.</span></span> <span data-ttu-id="f9d9d-125">控制項不會在專案周圍繪製焦點矩形。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-125">The control will not draw the focus rectangle around an item.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="f9d9d-126"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="f9d9d-126"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="f9d9d-127">控制項將會通知任何專案相關繪圖作業的父系。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-127">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="f9d9d-128">它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-128">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="f9d9d-129">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-129">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="f9d9d-130"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="f9d9d-130"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="f9d9d-131">控制項將會在清除專案之後通知父代。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-131">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="f9d9d-132">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-132">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="f9d9d-133"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="f9d9d-133"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="f9d9d-134">控制項將會在繪製專案之後通知父系。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-134">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="f9d9d-135">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="f9d9d-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="f9d9d-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="f9d9d-137">應用程式為專案指定了新的字型;控制項將會使用新的字型。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-137">The application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="f9d9d-138">如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-138">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="f9d9d-139">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="f9d9d-140"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="f9d9d-140"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | [<span data-ttu-id="f9d9d-141">版本4.71。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-141">Version 4.71.</span></span>](common-control-versions.md) <span data-ttu-id="f9d9d-142">您的應用程式將會在 [ \_ ](nm-customdraw.md) \_ \| \_ 繪製每個清單視圖子集合之前，收到具有 dwDrawStage 設定為 CDDS ITEMPREPAINT CDDS 子工作的 NM CUSTOMDRAW 控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-142">Your application will receive an [NM\_CUSTOMDRAW](nm-customdraw.md) control code with **dwDrawStage** set to CDDS\_ITEMPREPAINT \| CDDS\_SUBITEM before each list-view subitem is drawn.</span></span> <span data-ttu-id="f9d9d-143">然後，您可以分別為每個子項指定字型和色彩，或針對預設處理傳回 [**CDRF \_ DODEFAULT**](cdrf-constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-143">You can then specify font and color for each subitem separately or return [**CDRF\_DODEFAULT**](cdrf-constants.md) for default processing.</span></span> <span data-ttu-id="f9d9d-144">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-144">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="f9d9d-145"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="f9d9d-145"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="f9d9d-146">應用程式會以手動方式繪製專案。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-146">The application drew the item manually.</span></span> <span data-ttu-id="f9d9d-147">控制項不會繪製專案。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-147">The control will not draw the item.</span></span> <span data-ttu-id="f9d9d-148">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-148">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="f9d9d-149"><dt>**CDRF \_ SKIPPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="f9d9d-149"><dt>**CDRF\_SKIPPOSTPAINT**</dt></span></span> </dl>     | <span data-ttu-id="f9d9d-150">Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-150">Windows Vista.</span></span> <span data-ttu-id="f9d9d-151">控制項只會繪製背景。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-151">The control will only paint the background.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="f9d9d-152">備註</span><span class="sxs-lookup"><span data-stu-id="f9d9d-152">Remarks</span></span>

[<span data-ttu-id="f9d9d-153">版本5.80。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-153">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="f9d9d-154">如果您藉由傳回 [**CDRF \_ NEWFONT**](cdrf-constants.md)來變更字型，則清單視圖控制項可能會顯示已裁剪的文字。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-154">If you change the font by returning [**CDRF\_NEWFONT**](cdrf-constants.md), the list-view control might display clipped text.</span></span> <span data-ttu-id="f9d9d-155">這是與舊版通用控制項的回溯相容性所需的行為。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-155">This behavior is necessary for backward compatibility with earlier versions of the common controls.</span></span> <span data-ttu-id="f9d9d-156">如果您想要變更清單視圖控制項的字型，則在將任何專案加入至控制項之前，如果您將 *wParam* 值設定為5，則會得到更 [**好的結果 \_**](ccm-setversion.md) 。</span><span class="sxs-lookup"><span data-stu-id="f9d9d-156">If you want to change the font of a list-view control, you will get better results if you send a [**CCM\_SETVERSION**](ccm-setversion.md) message with the *wParam* value set to 5 before adding any items to the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d9d-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9d9d-157">Requirements</span></span>



| <span data-ttu-id="f9d9d-158">需求</span><span class="sxs-lookup"><span data-stu-id="f9d9d-158">Requirement</span></span> | <span data-ttu-id="f9d9d-159">值</span><span class="sxs-lookup"><span data-stu-id="f9d9d-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d9d-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9d9d-160">Minimum supported client</span></span><br/> | <span data-ttu-id="f9d9d-161">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9d9d-161">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9d9d-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9d9d-162">Minimum supported server</span></span><br/> | <span data-ttu-id="f9d9d-163">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9d9d-163">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9d9d-164">標頭</span><span class="sxs-lookup"><span data-stu-id="f9d9d-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9d9d-165"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f9d9d-165"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





