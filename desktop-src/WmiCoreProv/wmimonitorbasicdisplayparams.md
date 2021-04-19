---
description: 代表電腦監視器的基本顯示功能。
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: WmiMonitorBasicDisplayParams 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984638"
---
# <a name="wmimonitorbasicdisplayparams-class"></a><span data-ttu-id="9ae77-103">WmiMonitorBasicDisplayParams 類別</span><span class="sxs-lookup"><span data-stu-id="9ae77-103">WmiMonitorBasicDisplayParams class</span></span>

<span data-ttu-id="9ae77-104">**WmiMonitorBasicDisplayParams** WMI 類別代表電腦監視器的基本顯示功能。</span><span class="sxs-lookup"><span data-stu-id="9ae77-104">The **WmiMonitorBasicDisplayParams** WMI class represents the basic display features of a computer monitor.</span></span> <span data-ttu-id="9ae77-105">**VideoInputType** 屬性的值會指出監視器是否為類比或數位。</span><span class="sxs-lookup"><span data-stu-id="9ae77-105">The value of the **VideoInputType** property indicates whether the monitor is analog or digital.</span></span> <span data-ttu-id="9ae77-106">此類別中的資料會對應到視頻電子產品標準關聯之基本顯示參數/功能區塊中的資料 () 增強的擴充顯示器識別資料 (E-EDID) 標準。</span><span class="sxs-lookup"><span data-stu-id="9ae77-106">Data in this class corresponds to data in the Basic Display Parameters/Features block of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae77-107">語法</span><span class="sxs-lookup"><span data-stu-id="9ae77-107">Syntax</span></span>

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a><span data-ttu-id="9ae77-108">成員</span><span class="sxs-lookup"><span data-stu-id="9ae77-108">Members</span></span>

<span data-ttu-id="9ae77-109">**WmiMonitorBasicDisplayParams** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9ae77-109">The **WmiMonitorBasicDisplayParams** class has these types of members:</span></span>

-   [<span data-ttu-id="9ae77-110">屬性</span><span class="sxs-lookup"><span data-stu-id="9ae77-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ae77-111">屬性</span><span class="sxs-lookup"><span data-stu-id="9ae77-111">Properties</span></span>

<span data-ttu-id="9ae77-112">**WmiMonitorBasicDisplayParams** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9ae77-112">The **WmiMonitorBasicDisplayParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ae77-113">**使用中**</span><span class="sxs-lookup"><span data-stu-id="9ae77-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae77-114">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9ae77-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ae77-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae77-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ae77-116">表示使用中的監視器。</span><span class="sxs-lookup"><span data-stu-id="9ae77-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="9ae77-117">**DisplayTransferCharacteristic**</span><span class="sxs-lookup"><span data-stu-id="9ae77-117">**DisplayTransferCharacteristic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae77-118">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9ae77-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ae77-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae77-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ae77-120">顯示傳輸特性 (100 \* Gamma-100) 。</span><span class="sxs-lookup"><span data-stu-id="9ae77-120">Display transfer characteristic (100\*Gamma-100).</span></span>

</dd> <dt>

<span data-ttu-id="9ae77-121">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="9ae77-121">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae77-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae77-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae77-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae77-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae77-124">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="9ae77-124">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9ae77-125">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ae77-125">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="9ae77-126">**MaxHorizontalImageSize**</span><span class="sxs-lookup"><span data-stu-id="9ae77-126">**MaxHorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae77-127">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9ae77-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ae77-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae77-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ae77-129">水準影像大小的最大值（以公分為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ae77-129">Maximum horizontal image size in centimeters.</span></span> <span data-ttu-id="9ae77-130">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="9ae77-130">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9ae77-131">**MaxVerticalImageSize**</span><span class="sxs-lookup"><span data-stu-id="9ae77-131">**MaxVerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae77-132">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9ae77-132">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ae77-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae77-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ae77-134">垂直影像大小的最大值（以公分為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ae77-134">Maximum vertical image size in centimeters.</span></span> <span data-ttu-id="9ae77-135">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="9ae77-135">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9ae77-136">**SupportedDisplayFeatures**</span><span class="sxs-lookup"><span data-stu-id="9ae77-136">**SupportedDisplayFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae77-137">資料類型： **[ **SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**</span><span class="sxs-lookup"><span data-stu-id="9ae77-137">Data type: **[**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**</span></span>
</dt> <dt>

<span data-ttu-id="9ae77-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae77-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ae77-139">顯示監視器支援的功能。</span><span class="sxs-lookup"><span data-stu-id="9ae77-139">Display features supported by the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="9ae77-140">**VideoInputType**</span><span class="sxs-lookup"><span data-stu-id="9ae77-140">**VideoInputType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae77-141">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9ae77-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ae77-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae77-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ae77-143">影片輸入類型。</span><span class="sxs-lookup"><span data-stu-id="9ae77-143">Video input type.</span></span>



| <span data-ttu-id="9ae77-144">值</span><span class="sxs-lookup"><span data-stu-id="9ae77-144">Value</span></span>                                                                              | <span data-ttu-id="9ae77-145">意義</span><span class="sxs-lookup"><span data-stu-id="9ae77-145">Meaning</span></span>            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="9ae77-146"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="9ae77-146"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9ae77-147">類比</span><span class="sxs-lookup"><span data-stu-id="9ae77-147">Analog</span></span><br/>  |
| <dl> <span data-ttu-id="9ae77-148"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="9ae77-148"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="9ae77-149">Digital</span><span class="sxs-lookup"><span data-stu-id="9ae77-149">Digital</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ae77-150">備註</span><span class="sxs-lookup"><span data-stu-id="9ae77-150">Remarks</span></span>

<span data-ttu-id="9ae77-151">**MaxHorizontalImageSize** 和 **MaxVerticalImageSize** 代表監視器可針對整組支援的計時和格式組合正確顯示的影像維度大小上限。</span><span class="sxs-lookup"><span data-stu-id="9ae77-151">**MaxHorizontalImageSize** and **MaxVerticalImageSize** represent the maximum image dimensions that the monitor can correctly display for the entire set of supported timing and format combinations.</span></span> <span data-ttu-id="9ae77-152">最大影像維度是由 VESA 影片影像區域定義所定義 (VIAD) 標準，並四捨五入至最接近的釐米。</span><span class="sxs-lookup"><span data-stu-id="9ae77-152">The maximum image dimension is defined by VESA Video Image Area Definition (VIAD) Standard and is rounded to the nearest centimeter.</span></span> <span data-ttu-id="9ae77-153">主機電腦系統可以使用此資料來選取影像大小和外觀比例，以允許適當調整的文字。</span><span class="sxs-lookup"><span data-stu-id="9ae77-153">The host computer system can use this data to select the image size and aspect ratio that will allow properly scaled text.</span></span> <span data-ttu-id="9ae77-154">請注意，如果其中一或兩個欄位都是零，則系統不會對顯示大小做出任何假設。</span><span class="sxs-lookup"><span data-stu-id="9ae77-154">Be aware that, if either or both of these fields are zero, then the system makes no assumptions about the display size.</span></span> <span data-ttu-id="9ae77-155">例如，投影顯示器的大小可能不確定。</span><span class="sxs-lookup"><span data-stu-id="9ae77-155">For example, the size of a projection display may be undetermined.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae77-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ae77-156">Requirements</span></span>



| <span data-ttu-id="9ae77-157">需求</span><span class="sxs-lookup"><span data-stu-id="9ae77-157">Requirement</span></span> | <span data-ttu-id="9ae77-158">值</span><span class="sxs-lookup"><span data-stu-id="9ae77-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae77-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ae77-159">Minimum supported client</span></span><br/> | <span data-ttu-id="9ae77-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ae77-160">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9ae77-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ae77-161">Minimum supported server</span></span><br/> | <span data-ttu-id="9ae77-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ae77-162">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9ae77-163">命名空間</span><span class="sxs-lookup"><span data-stu-id="9ae77-163">Namespace</span></span><br/>                | <span data-ttu-id="9ae77-164">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="9ae77-164">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="9ae77-165">MOF</span><span class="sxs-lookup"><span data-stu-id="9ae77-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ae77-166"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ae77-166"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ae77-167">DLL</span><span class="sxs-lookup"><span data-stu-id="9ae77-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ae77-168"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ae77-168"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ae77-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ae77-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ae77-170">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="9ae77-170">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




