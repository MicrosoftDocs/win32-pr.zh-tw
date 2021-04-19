---
title: 'RF 常數 (CommCtrl .h) '
description: 這些常數會由控制項用來作為傳回值，以回應 NM \_ CUSTOMDRAW 通知碼。
ms.assetid: 6b05e27e-5d18-46f2-b326-2a5148597852
topic_type:
- apiref
api_name:
- CDRF_DODEFAULT
- CDRF_NEWFONT
- CDRF_SKIPDEFAULT
- CDRF_DOERASE
- CDRF_NOTIFYPOSTPAINT
- CDRF_NOTIFYITEMDRAW
- CDRF_NOTIFYSUBITEMDRAW
- CDRF_NOTIFYPOSTERASE
- CDRF_SKIPPOSTPAINT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15ec83b8f8238e4236bbee3f7091c228c552efb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999349"
---
# <a name="rf-constants"></a><span data-ttu-id="de9bc-103">RF 常數</span><span class="sxs-lookup"><span data-stu-id="de9bc-103">RF Constants</span></span>

<span data-ttu-id="de9bc-104">這些常數會由控制項用來作為傳回值，以回應 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="de9bc-104">These constants are used as return values by a control in response to an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code.</span></span>



| <span data-ttu-id="de9bc-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="de9bc-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="de9bc-106">Description</span><span class="sxs-lookup"><span data-stu-id="de9bc-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CDRF_DODEFAULT"></span><span id="cdrf_dodefault"></span><dl> <span data-ttu-id="de9bc-107"><dt>**CDRF \_DODEFAULT**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="de9bc-107"><dt>**CDRF\_DODEFAULT**</dt> <dt>0x00000000</dt></span></span> </dl>                         | <span data-ttu-id="de9bc-108">控制項將會自行繪製。</span><span class="sxs-lookup"><span data-stu-id="de9bc-108">The control will draw itself.</span></span> <span data-ttu-id="de9bc-109">它不會針對此繪製迴圈傳送任何額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="de9bc-109">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="de9bc-110">當 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="de9bc-110">This occurs when the **dwDrawStage** of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                               |
| <span id="CDRF_NEWFONT"></span><span id="cdrf_newfont"></span><dl> <span data-ttu-id="de9bc-111"><dt>**CDRF \_NEWFONT**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="de9bc-111"><dt>**CDRF\_NEWFONT**</dt> <dt>0x00000002</dt></span></span> </dl>                               | <span data-ttu-id="de9bc-112">應用程式為專案指定了新的字型;控制項將會使用新的字型。</span><span class="sxs-lookup"><span data-stu-id="de9bc-112">The application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="de9bc-113">如需變更字型的詳細資訊，請參閱變更字型和色彩。</span><span class="sxs-lookup"><span data-stu-id="de9bc-113">For more information about changing fonts, see Changing fonts and colors.</span></span> <span data-ttu-id="de9bc-114">當 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="de9bc-114">This occurs when the **dwDrawStage** of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                      |
| <span id="CDRF_SKIPDEFAULT"></span><span id="cdrf_skipdefault"></span><dl> <span data-ttu-id="de9bc-115"><dt>**CDRF \_SKIPDEFAULT**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="de9bc-115"><dt>**CDRF\_SKIPDEFAULT**</dt> <dt>0x00000004</dt></span></span> </dl>                   | <span data-ttu-id="de9bc-116">應用程式會以手動方式繪製專案。</span><span class="sxs-lookup"><span data-stu-id="de9bc-116">The application drew the item manually.</span></span> <span data-ttu-id="de9bc-117">控制項不會繪製專案。</span><span class="sxs-lookup"><span data-stu-id="de9bc-117">The control will not draw the item.</span></span> <span data-ttu-id="de9bc-118">當 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="de9bc-118">This occurs when the **dwDrawStage** of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="CDRF_DOERASE"></span><span id="cdrf_doerase"></span><dl> <span data-ttu-id="de9bc-119"><dt>**CDRF \_DOERASE**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="de9bc-119"><dt>**CDRF\_DOERASE**</dt> <dt>0x00000008</dt></span></span> </dl>                               | <span data-ttu-id="de9bc-120">**Windows Vista （含）以後版本。**</span><span class="sxs-lookup"><span data-stu-id="de9bc-120">**Windows Vista and later.**</span></span> <span data-ttu-id="de9bc-121">控制項將會繪製背景。</span><span class="sxs-lookup"><span data-stu-id="de9bc-121">The control will draw the background.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CDRF_NOTIFYPOSTPAINT"></span><span id="cdrf_notifypostpaint"></span><dl> <span data-ttu-id="de9bc-122"><dt>**CDRF \_NOTIFYPOSTPAINT**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="de9bc-122"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt> <dt>0x00000010</dt></span></span> </dl>       | <span data-ttu-id="de9bc-123">控制項將會在繪製專案之後通知父系。</span><span class="sxs-lookup"><span data-stu-id="de9bc-123">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="de9bc-124">當 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="de9bc-124">This occurs when the **dwDrawStage** of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                                               |
| <span id="CDRF_NOTIFYITEMDRAW"></span><span id="cdrf_notifyitemdraw"></span><dl> <span data-ttu-id="de9bc-125"><dt>**CDRF \_NOTIFYITEMDRAW**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="de9bc-125"><dt>**CDRF\_NOTIFYITEMDRAW**</dt> <dt>0x00000020</dt></span></span> </dl>          | <span data-ttu-id="de9bc-126">控制項將會通知任何專案相關繪圖作業的父系。</span><span class="sxs-lookup"><span data-stu-id="de9bc-126">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="de9bc-127">它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="de9bc-127">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="de9bc-128">當 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="de9bc-128">This occurs when the **dwDrawStage** of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                           |
| <span id="CDRF_NOTIFYSUBITEMDRAW"></span><span id="cdrf_notifysubitemdraw"></span><dl> <span data-ttu-id="de9bc-129"><dt>**CDRF \_NOTIFYSUBITEMDRAW**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="de9bc-129"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="de9bc-130">**Internet Explorer 4.0 和更新版本。**</span><span class="sxs-lookup"><span data-stu-id="de9bc-130">**Internet Explorer 4.0 and later.**</span></span> <span data-ttu-id="de9bc-131">控制項將會通知任何專案相關繪圖作業的父系。</span><span class="sxs-lookup"><span data-stu-id="de9bc-131">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="de9bc-132">它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="de9bc-132">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="de9bc-133">當 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="de9bc-133">This occurs when the **dwDrawStage** of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure equals CDDS\_PREPAINT.</span></span> <span data-ttu-id="de9bc-134">此旗標與 **CDRF \_ NOTIFYITEMDRAW** 相同，且其用途與內容相關。</span><span class="sxs-lookup"><span data-stu-id="de9bc-134">This flag is identical to **CDRF\_NOTIFYITEMDRAW** and its use is context-dependent.</span></span><br/> |
| <span id="CDRF_NOTIFYPOSTERASE"></span><span id="cdrf_notifyposterase"></span><dl> <span data-ttu-id="de9bc-135"><dt>**CDRF \_NOTIFYPOSTERASE**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="de9bc-135"><dt>**CDRF\_NOTIFYPOSTERASE**</dt> <dt>0x00000040</dt></span></span> </dl>       | <span data-ttu-id="de9bc-136">控制項將會在清除專案之後通知父代。</span><span class="sxs-lookup"><span data-stu-id="de9bc-136">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="de9bc-137">當 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="de9bc-137">This occurs when the **dwDrawStage** of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                                                |
| <span id="CDRF_SKIPPOSTPAINT"></span><span id="cdrf_skippostpaint"></span><dl> <span data-ttu-id="de9bc-138"><dt>**CDRF \_SKIPPOSTPAINT**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="de9bc-138"><dt>**CDRF\_SKIPPOSTPAINT**</dt> <dt>0x00000100</dt></span></span> </dl>             | <span data-ttu-id="de9bc-139">**Windows Vista （含）以後版本。**</span><span class="sxs-lookup"><span data-stu-id="de9bc-139">**Windows Vista and later.**</span></span> <span data-ttu-id="de9bc-140">控制項不會繪製焦點矩形。</span><span class="sxs-lookup"><span data-stu-id="de9bc-140">The control will not draw the focus rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="de9bc-141">備註</span><span class="sxs-lookup"><span data-stu-id="de9bc-141">Remarks</span></span>

<span data-ttu-id="de9bc-142">這些常數定義于 Commctrl 中。</span><span class="sxs-lookup"><span data-stu-id="de9bc-142">These constants are defined in Commctrl.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="de9bc-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="de9bc-143">Requirements</span></span>



| <span data-ttu-id="de9bc-144">需求</span><span class="sxs-lookup"><span data-stu-id="de9bc-144">Requirement</span></span> | <span data-ttu-id="de9bc-145">值</span><span class="sxs-lookup"><span data-stu-id="de9bc-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de9bc-146">標頭</span><span class="sxs-lookup"><span data-stu-id="de9bc-146">Header</span></span><br/> | <dl> <span data-ttu-id="de9bc-147"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="de9bc-147"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de9bc-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de9bc-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9bc-149">使用自訂繪圖自訂控制項的外觀</span><span class="sxs-lookup"><span data-stu-id="de9bc-149">Customizing a Control's Appearance Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





