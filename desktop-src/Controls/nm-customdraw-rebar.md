---
title: 'NM_CUSTOMDRAW (Rebar) 通知碼 (Commctrl) '
description: 由 Rebar 控制項傳送，以通知其父視窗有關繪製作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 3ba9bb59-f297-4af1-a9a9-d8789def5bde
keywords:
- NM_CUSTOMDRAW (Rebar) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 329f3e9abfb20dbca8cebd3a6bf02673ad00f904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106625"
---
# <a name="nm_customdraw-rebar-notification-code"></a><span data-ttu-id="a700b-105">NM \_ CUSTOMDRAW (Rebar) 通知碼</span><span class="sxs-lookup"><span data-stu-id="a700b-105">NM\_CUSTOMDRAW (rebar) notification code</span></span>

<span data-ttu-id="a700b-106">由 Rebar 控制項傳送，以通知其父視窗有關繪製作業。</span><span class="sxs-lookup"><span data-stu-id="a700b-106">Sent by the rebar control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="a700b-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="a700b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a700b-108">參數</span><span class="sxs-lookup"><span data-stu-id="a700b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a700b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a700b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a700b-110">[**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a700b-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="a700b-111">此結構的 **dwItemSpec** 成員包含所繪製之帶狀的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a700b-111">The **dwItemSpec** member of this structure contains the identifier of the band being drawn.</span></span> <span data-ttu-id="a700b-112">此結構的 **lItemlParam** 成員包含所繪製之波段的 *lParam* 。</span><span class="sxs-lookup"><span data-stu-id="a700b-112">The **lItemlParam** member of this structure contains the *lParam* of the band being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a700b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a700b-113">Return value</span></span>

<span data-ttu-id="a700b-114">您的應用程式可以傳回的值取決於目前的繪圖階段。</span><span class="sxs-lookup"><span data-stu-id="a700b-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="a700b-115">相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。</span><span class="sxs-lookup"><span data-stu-id="a700b-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="a700b-116">您必須傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a700b-116">You must return one of the following values.</span></span>



| <span data-ttu-id="a700b-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a700b-117">Return code</span></span>                                                                                            | <span data-ttu-id="a700b-118">Description</span><span class="sxs-lookup"><span data-stu-id="a700b-118">Description</span></span>                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a700b-119"><dt>**CDRF \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="a700b-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="a700b-120">控制項將會自行繪製。</span><span class="sxs-lookup"><span data-stu-id="a700b-120">The control will draw itself.</span></span> <span data-ttu-id="a700b-121">它不會針對此繪製迴圈傳送任何額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="a700b-121">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notifications for this paint cycle.</span></span> <span data-ttu-id="a700b-122">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a700b-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="a700b-123"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="a700b-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="a700b-124">控制項將會通知任何專案相關繪圖作業的父系。</span><span class="sxs-lookup"><span data-stu-id="a700b-124">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="a700b-125">它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="a700b-125">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="a700b-126">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a700b-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="a700b-127"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="a700b-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="a700b-128">控制項將會在清除專案之後通知父代。</span><span class="sxs-lookup"><span data-stu-id="a700b-128">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="a700b-129">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a700b-129">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="a700b-130"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="a700b-130"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="a700b-131">控制項將會在繪製專案之後通知父系。</span><span class="sxs-lookup"><span data-stu-id="a700b-131">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="a700b-132">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a700b-132">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="a700b-133"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="a700b-133"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="a700b-134">控制項將會通知任何專案相關繪圖作業的父系。</span><span class="sxs-lookup"><span data-stu-id="a700b-134">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="a700b-135">它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="a700b-135">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="a700b-136">當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a700b-136">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="a700b-137"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="a700b-137"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="a700b-138">應用程式為專案指定了新的字型;控制項將會使用新的字型。</span><span class="sxs-lookup"><span data-stu-id="a700b-138">The application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="a700b-139">如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。</span><span class="sxs-lookup"><span data-stu-id="a700b-139">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="a700b-140">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a700b-140">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="a700b-141"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="a700b-141"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="a700b-142">應用程式會以手動方式繪製專案。</span><span class="sxs-lookup"><span data-stu-id="a700b-142">The application drew the item manually.</span></span> <span data-ttu-id="a700b-143">控制項不會繪製專案。</span><span class="sxs-lookup"><span data-stu-id="a700b-143">The control will not draw the item.</span></span> <span data-ttu-id="a700b-144">當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a700b-144">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="a700b-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="a700b-145">Requirements</span></span>



| <span data-ttu-id="a700b-146">需求</span><span class="sxs-lookup"><span data-stu-id="a700b-146">Requirement</span></span> | <span data-ttu-id="a700b-147">值</span><span class="sxs-lookup"><span data-stu-id="a700b-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a700b-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a700b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a700b-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a700b-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a700b-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a700b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a700b-151">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a700b-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a700b-152">標頭</span><span class="sxs-lookup"><span data-stu-id="a700b-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="a700b-153"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a700b-153"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a700b-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a700b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a700b-155">使用自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="a700b-155">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





