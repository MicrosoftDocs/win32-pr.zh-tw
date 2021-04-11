---
description: 表示用來指向顯示區域的裝置。
ms.assetid: ffc675c3-29bd-4c54-8e54-8b6212daf66d
title: 'CIM_PointingDevice 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.Resolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57cca8c81a2d363e9e31bfc958a75b71e1b910d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115985"
---
# <a name="cim_pointingdevice-class-hyper-v-management"></a><span data-ttu-id="9c54d-103">CIM_PointingDevice 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="9c54d-103">CIM_PointingDevice class (Hyper-V management)</span></span>

<span data-ttu-id="9c54d-104">表示用來指向顯示區域的裝置。</span><span class="sxs-lookup"><span data-stu-id="9c54d-104">Represents a device used to point to regions of a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c54d-105">語法</span><span class="sxs-lookup"><span data-stu-id="9c54d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
{
  uint16 PointingType;
  uint8  NumberOfButtons;
  uint16 Handedness;
  uint32 Resolution;
};
```

## <a name="members"></a><span data-ttu-id="9c54d-106">成員</span><span class="sxs-lookup"><span data-stu-id="9c54d-106">Members</span></span>

<span data-ttu-id="9c54d-107">**CIM \_ PointingDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9c54d-107">The **CIM\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="9c54d-108">屬性</span><span class="sxs-lookup"><span data-stu-id="9c54d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c54d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="9c54d-109">Properties</span></span>

<span data-ttu-id="9c54d-110">**CIM \_ PointingDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9c54d-110">The **CIM\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c54d-111">**Handedness**</span><span class="sxs-lookup"><span data-stu-id="9c54d-111">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c54d-112">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9c54d-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c54d-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c54d-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c54d-114">指出是否已針對右手或左手操作設定指向裝置。</span><span class="sxs-lookup"><span data-stu-id="9c54d-114">Indicates whether the pointing device is configured for right or left handed operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c54d-115">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="9c54d-115">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9c54d-116">**不適用** (1) </span><span class="sxs-lookup"><span data-stu-id="9c54d-116">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="9c54d-117">**右手操作** (2) </span><span class="sxs-lookup"><span data-stu-id="9c54d-117">**Right Handed Operation** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="9c54d-118">左手 **操作** (3) </span><span class="sxs-lookup"><span data-stu-id="9c54d-118">**Left Handed Operation** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9c54d-119">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="9c54d-119">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c54d-120">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9c54d-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9c54d-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c54d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c54d-122">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 指標裝置 \| 003.4」 ) </span><span class="sxs-lookup"><span data-stu-id="9c54d-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.4")</span></span>
</dt> </dl>

<span data-ttu-id="9c54d-123">裝置上的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="9c54d-123">The number of buttons on the device.</span></span> <span data-ttu-id="9c54d-124">如果指標裝置沒有任何按鈕，則此值應該設定為 "0"。</span><span class="sxs-lookup"><span data-stu-id="9c54d-124">If the pointing device has no buttons, this value should be set to "0".</span></span>

</dd> <dt>

<span data-ttu-id="9c54d-125">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="9c54d-125">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c54d-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9c54d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c54d-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c54d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c54d-128">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 指標裝置 \| 003.1」 ) </span><span class="sxs-lookup"><span data-stu-id="9c54d-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.1")</span></span>
</dt> </dl>

<span data-ttu-id="9c54d-129">指標裝置的型別。</span><span class="sxs-lookup"><span data-stu-id="9c54d-129">The type of the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9c54d-130">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="9c54d-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c54d-131">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="9c54d-131">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="9c54d-132">**滑鼠** (3) </span><span class="sxs-lookup"><span data-stu-id="9c54d-132">**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="9c54d-133">**追蹤球** (4) </span><span class="sxs-lookup"><span data-stu-id="9c54d-133">**Track Ball** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="9c54d-134">**追蹤點** (5) </span><span class="sxs-lookup"><span data-stu-id="9c54d-134">**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="9c54d-135">**滑行點** (6) </span><span class="sxs-lookup"><span data-stu-id="9c54d-135">**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="9c54d-136">**觸控板** (7) </span><span class="sxs-lookup"><span data-stu-id="9c54d-136">**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="9c54d-137">**觸控式螢幕** (8) </span><span class="sxs-lookup"><span data-stu-id="9c54d-137">**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="9c54d-138">**滑鼠-光學感應器** (9) </span><span class="sxs-lookup"><span data-stu-id="9c54d-138">**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9c54d-139">**解決方法**</span><span class="sxs-lookup"><span data-stu-id="9c54d-139">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c54d-140">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9c54d-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c54d-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c54d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c54d-142">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每英寸計數」 ) ， **PUnit** ( 「計數/英寸」 ) </span><span class="sxs-lookup"><span data-stu-id="9c54d-142">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Counts per Inch"), **PUnit** ("count / inch")</span></span>
</dt> </dl>

<span data-ttu-id="9c54d-143">指標裝置的追蹤解析度（以每英寸計數計算）。</span><span class="sxs-lookup"><span data-stu-id="9c54d-143">The tracking resolution of the pointing device, in counts per inch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c54d-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c54d-144">Requirements</span></span>



| <span data-ttu-id="9c54d-145">需求</span><span class="sxs-lookup"><span data-stu-id="9c54d-145">Requirement</span></span> | <span data-ttu-id="9c54d-146">值</span><span class="sxs-lookup"><span data-stu-id="9c54d-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c54d-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c54d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="9c54d-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c54d-148">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9c54d-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c54d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="9c54d-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c54d-150">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9c54d-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="9c54d-151">Namespace</span></span><br/>                | <span data-ttu-id="9c54d-152">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="9c54d-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9c54d-153">MOF</span><span class="sxs-lookup"><span data-stu-id="9c54d-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c54d-154"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9c54d-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c54d-155">DLL</span><span class="sxs-lookup"><span data-stu-id="9c54d-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c54d-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9c54d-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9c54d-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c54d-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c54d-158">**CIM \_ UserDevice**</span><span class="sxs-lookup"><span data-stu-id="9c54d-158">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

