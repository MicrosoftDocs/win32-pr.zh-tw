---
title: 'NM_CUSTOMDRAW (標頭) 通知碼 (Commctrl) '
description: 由標題控制項傳送，以通知其父視窗有關繪製作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 44dab54b-45ef-4fba-93b8-2a3e35cda23f
keywords:
- NM_CUSTOMDRAW (標頭) 通知碼 Windows 控制項
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
ms.openlocfilehash: 89d6b35503aebed221da6cec212c6dbf614061f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967576"
---
# <a name="nm_customdraw-header-notification-code"></a><span data-ttu-id="427c2-105">NM \_ CUSTOMDRAW (標頭) 通知碼</span><span class="sxs-lookup"><span data-stu-id="427c2-105">NM\_CUSTOMDRAW (header) notification code</span></span>

<span data-ttu-id="427c2-106">由標題控制項傳送，以通知其父視窗有關繪製作業。</span><span class="sxs-lookup"><span data-stu-id="427c2-106">Sent by a header control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="427c2-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="427c2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="427c2-108">參數</span><span class="sxs-lookup"><span data-stu-id="427c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="427c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="427c2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="427c2-110">[**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="427c2-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="427c2-111">此結構的 **dwItemSpec** 成員包含所繪製專案的索引，而且此結構的 **lItemlParam** 成員包含該專案的 *lParam*。</span><span class="sxs-lookup"><span data-stu-id="427c2-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="427c2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="427c2-112">Return value</span></span>

<span data-ttu-id="427c2-113">您的應用程式可以傳回的值取決於目前的繪圖階段。</span><span class="sxs-lookup"><span data-stu-id="427c2-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="427c2-114">相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。</span><span class="sxs-lookup"><span data-stu-id="427c2-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="427c2-115">您必須傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="427c2-115">You must return one of the following values.</span></span>



| <span data-ttu-id="427c2-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="427c2-116">Return code</span></span>                                                                                            | <span data-ttu-id="427c2-117">Description</span><span class="sxs-lookup"><span data-stu-id="427c2-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="427c2-118"><dt>**CDRF \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="427c2-118"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="427c2-119">控制項將會自行繪製。</span><span class="sxs-lookup"><span data-stu-id="427c2-119">The control will draw itself.</span></span> <span data-ttu-id="427c2-120">它不會針對此繪製迴圈傳送任何額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="427c2-120">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) messages for this paint cycle.</span></span> <span data-ttu-id="427c2-121">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="427c2-121">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="427c2-122"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="427c2-122"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="427c2-123">控制項將會通知任何專案相關繪圖作業的父系。</span><span class="sxs-lookup"><span data-stu-id="427c2-123">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="427c2-124">它會 \_ 在繪製專案之前和之後傳送 NM CUSTOMDRAW 通知碼。</span><span class="sxs-lookup"><span data-stu-id="427c2-124">It will send NM\_CUSTOMDRAW notification codes before and after drawing items.</span></span> <span data-ttu-id="427c2-125">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="427c2-125">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="427c2-126"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="427c2-126"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="427c2-127">控制項將會在清除專案之後通知父代。</span><span class="sxs-lookup"><span data-stu-id="427c2-127">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="427c2-128">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="427c2-128">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="427c2-129"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="427c2-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="427c2-130">控制項將會在繪製專案之後通知父系。</span><span class="sxs-lookup"><span data-stu-id="427c2-130">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="427c2-131">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="427c2-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="427c2-132"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="427c2-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="427c2-133">[通用控制項版本](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="427c2-133">[Common Control Versions](common-control-versions.md).</span></span> <span data-ttu-id="427c2-134">當正在繪製清單視圖子項目時，控制項將會通知父代。</span><span class="sxs-lookup"><span data-stu-id="427c2-134">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="427c2-135">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="427c2-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="427c2-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="427c2-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="427c2-137">您的應用程式已為專案指定新字型;控制項將會使用新的字型。</span><span class="sxs-lookup"><span data-stu-id="427c2-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="427c2-138">如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。</span><span class="sxs-lookup"><span data-stu-id="427c2-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="427c2-139">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="427c2-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="427c2-140"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="427c2-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="427c2-141">您的應用程式會以手動方式繪製專案。</span><span class="sxs-lookup"><span data-stu-id="427c2-141">Your application drew the item manually.</span></span> <span data-ttu-id="427c2-142">控制項不會繪製專案。</span><span class="sxs-lookup"><span data-stu-id="427c2-142">The control will not draw the item.</span></span> <span data-ttu-id="427c2-143">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="427c2-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="427c2-144">備註</span><span class="sxs-lookup"><span data-stu-id="427c2-144">Remarks</span></span>

<span data-ttu-id="427c2-145">請參閱 [使用自訂繪製](custom-draw.md) 來進一步討論。</span><span class="sxs-lookup"><span data-stu-id="427c2-145">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="427c2-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="427c2-146">Requirements</span></span>



| <span data-ttu-id="427c2-147">需求</span><span class="sxs-lookup"><span data-stu-id="427c2-147">Requirement</span></span> | <span data-ttu-id="427c2-148">值</span><span class="sxs-lookup"><span data-stu-id="427c2-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="427c2-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="427c2-149">Minimum supported client</span></span><br/> | <span data-ttu-id="427c2-150">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="427c2-150">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="427c2-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="427c2-151">Minimum supported server</span></span><br/> | <span data-ttu-id="427c2-152">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="427c2-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="427c2-153">標頭</span><span class="sxs-lookup"><span data-stu-id="427c2-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="427c2-154"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="427c2-154"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





