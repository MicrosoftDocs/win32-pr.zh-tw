---
title: 指標裝置變更
description: 可以在 WM_POINTERDEVICECHANGE 訊息的 wParam 參數中傳遞的值。
ms.assetid: B95191D7-820B-445A-A3A4-811F9F1A8C4F
topic_type:
- apiref
api_name:
- PDC_ARRIVAL
- PDC_REMOVAL
- PDC_ORIENTATION_0
- PDC_ORIENTATION_90
- PDC_ORIENTATION_180
- PDC_ORIENTATION_270
- PDC_MODE_DEFAULT
- PDC_MODE_CENTERED
- PDC_MAPPING_CHANGE
- PDC_RESOLUTION
- PDC_ORIGIN
- PDC_MODE_ASPECTRATIOPRESERVED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5e4b85c17adcd2db7c0f2f672e27ca467b346b0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934746"
---
# <a name="pointer-device-change"></a><span data-ttu-id="352e4-103">指標裝置變更</span><span class="sxs-lookup"><span data-stu-id="352e4-103">Pointer Device Change</span></span>

<span data-ttu-id="352e4-104">可以在 [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md)訊息的 *wParam* 參數中傳遞的值。</span><span class="sxs-lookup"><span data-stu-id="352e4-104">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span>

<dl> <dt>

<span data-ttu-id="352e4-105"><span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**</span><span class="sxs-lookup"><span data-stu-id="352e4-105"><span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="352e4-106">0x001</span><span class="sxs-lookup"><span data-stu-id="352e4-106">0x001</span></span>
</dt> <dt>



<span data-ttu-id="352e4-107">已附加新的裝置。</span><span class="sxs-lookup"><span data-stu-id="352e4-107">A new device is attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="352e4-108"><span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**</span><span class="sxs-lookup"><span data-stu-id="352e4-108"><span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="352e4-109">0x002</span><span class="sxs-lookup"><span data-stu-id="352e4-109">0x002</span></span>
</dt> <dt>



<span data-ttu-id="352e4-110">裝置已卸離。</span><span class="sxs-lookup"><span data-stu-id="352e4-110">A device has been detached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="352e4-111"><span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**</span><span class="sxs-lookup"><span data-stu-id="352e4-111"><span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="352e4-112">0x004</span><span class="sxs-lookup"><span data-stu-id="352e4-112">0x004</span></span>
</dt> <dt>



<span data-ttu-id="352e4-113">裝置的方向。</span><span class="sxs-lookup"><span data-stu-id="352e4-113">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="352e4-114"><span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**</span><span class="sxs-lookup"><span data-stu-id="352e4-114"><span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="352e4-115">0x008</span><span class="sxs-lookup"><span data-stu-id="352e4-115">0x008</span></span>
</dt> <dt>



<span data-ttu-id="352e4-116">裝置的方向。</span><span class="sxs-lookup"><span data-stu-id="352e4-116">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="352e4-117"><span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**</span><span class="sxs-lookup"><span data-stu-id="352e4-117"><span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="352e4-118">0x010</span><span class="sxs-lookup"><span data-stu-id="352e4-118">0x010</span></span>
</dt> <dt>



<span data-ttu-id="352e4-119">裝置的方向。</span><span class="sxs-lookup"><span data-stu-id="352e4-119">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="352e4-120"><span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**</span><span class="sxs-lookup"><span data-stu-id="352e4-120"><span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="352e4-121">0x020</span><span class="sxs-lookup"><span data-stu-id="352e4-121">0x020</span></span>
</dt> <dt>



<span data-ttu-id="352e4-122">裝置的方向。</span><span class="sxs-lookup"><span data-stu-id="352e4-122">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="352e4-123"><span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="352e4-123"><span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="352e4-124">0x040</span><span class="sxs-lookup"><span data-stu-id="352e4-124">0x040</span></span>
</dt> <dt>



<span data-ttu-id="352e4-125">預設顯示模式。</span><span class="sxs-lookup"><span data-stu-id="352e4-125">The default display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="352e4-126"><span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**</span><span class="sxs-lookup"><span data-stu-id="352e4-126"><span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="352e4-127">0x080</span><span class="sxs-lookup"><span data-stu-id="352e4-127">0x080</span></span>
</dt> <dt>



<span data-ttu-id="352e4-128">居中顯示模式。</span><span class="sxs-lookup"><span data-stu-id="352e4-128">Centered display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="352e4-129"><span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="352e4-129"><span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="352e4-130">0x100</span><span class="sxs-lookup"><span data-stu-id="352e4-130">0x100</span></span>
</dt> <dt>



<span data-ttu-id="352e4-131">顯示為數字板對應的變更。</span><span class="sxs-lookup"><span data-stu-id="352e4-131">The change in display to digitizer mapping.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="352e4-132"><span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**</span><span class="sxs-lookup"><span data-stu-id="352e4-132"><span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="352e4-133">0x200</span><span class="sxs-lookup"><span data-stu-id="352e4-133">0x200</span></span>
</dt> <dt>



<span data-ttu-id="352e4-134">顯示解析度。</span><span class="sxs-lookup"><span data-stu-id="352e4-134">Display resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="352e4-135"><span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**</span><span class="sxs-lookup"><span data-stu-id="352e4-135"><span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="352e4-136">0x400</span><span class="sxs-lookup"><span data-stu-id="352e4-136">0x400</span></span>
</dt> <dt>



<span data-ttu-id="352e4-137">顯示來源。</span><span class="sxs-lookup"><span data-stu-id="352e4-137">The display origin.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="352e4-138"><span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**</span><span class="sxs-lookup"><span data-stu-id="352e4-138"><span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="352e4-139">0x800</span><span class="sxs-lookup"><span data-stu-id="352e4-139">0x800</span></span>
</dt> <dt>



<span data-ttu-id="352e4-140">顯示外觀比例。</span><span class="sxs-lookup"><span data-stu-id="352e4-140">The display aspect ratio.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="352e4-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="352e4-141">Requirements</span></span>



| <span data-ttu-id="352e4-142">需求</span><span class="sxs-lookup"><span data-stu-id="352e4-142">Requirement</span></span> | <span data-ttu-id="352e4-143">值</span><span class="sxs-lookup"><span data-stu-id="352e4-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="352e4-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="352e4-144">Minimum supported client</span></span><br/> | <span data-ttu-id="352e4-145">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="352e4-145">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="352e4-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="352e4-146">Minimum supported server</span></span><br/> | <span data-ttu-id="352e4-147">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="352e4-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="352e4-148">標頭</span><span class="sxs-lookup"><span data-stu-id="352e4-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="352e4-149"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="352e4-149"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="352e4-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="352e4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="352e4-151">常數</span><span class="sxs-lookup"><span data-stu-id="352e4-151">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="352e4-152">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="352e4-152">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





