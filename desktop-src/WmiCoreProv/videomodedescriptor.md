---
description: 包含 WmiMonitorListedSupportedSourceModes 類別中 MonitorSourceModes 陣列的模式描述項元素。
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: VideoModeDescriptor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 06094b24b6b8197eab89b65cd5a9a83f46b39f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320347"
---
# <a name="videomodedescriptor-class"></a><span data-ttu-id="9d29e-103">VideoModeDescriptor 類別</span><span class="sxs-lookup"><span data-stu-id="9d29e-103">VideoModeDescriptor class</span></span>

<span data-ttu-id="9d29e-104">**VideoModeDescriptorVideo** WMI 類別包含 [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md)類別中 **MonitorSourceModes** 陣列的模式描述項元素。</span><span class="sxs-lookup"><span data-stu-id="9d29e-104">The **VideoModeDescriptorVideo** WMI class contains mode descriptor elements for the **MonitorSourceModes** array in the [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) class.</span></span> <span data-ttu-id="9d29e-105">這些元素包括監視功能，例如重新整理速率、圖元特性或影像大小。</span><span class="sxs-lookup"><span data-stu-id="9d29e-105">These elements include monitor features such as refresh rate, pixel characteristics, or image size.</span></span> <span data-ttu-id="9d29e-106">**VideoModeDescriptorVideo** 類別包含的資訊，是已建立、標準和詳細計時區塊可用之資料的超集合。</span><span class="sxs-lookup"><span data-stu-id="9d29e-106">The **VideoModeDescriptorVideo** class contains information that is a superset of the data available from established, standard, and detailed timing blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d29e-107">語法</span><span class="sxs-lookup"><span data-stu-id="9d29e-107">Syntax</span></span>

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a><span data-ttu-id="9d29e-108">成員</span><span class="sxs-lookup"><span data-stu-id="9d29e-108">Members</span></span>

<span data-ttu-id="9d29e-109">**VideoModeDescriptor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9d29e-109">The **VideoModeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="9d29e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="9d29e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d29e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="9d29e-111">Properties</span></span>

<span data-ttu-id="9d29e-112">**VideoModeDescriptor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9d29e-112">The **VideoModeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d29e-113">**CompositePolarityType**</span><span class="sxs-lookup"><span data-stu-id="9d29e-113">**CompositePolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-114">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9d29e-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-116">複合極性類型。</span><span class="sxs-lookup"><span data-stu-id="9d29e-116">Composite polarity type.</span></span> <span data-ttu-id="9d29e-117">這是在垂直同步之外的水準同步跳動的極性。</span><span class="sxs-lookup"><span data-stu-id="9d29e-117">This is polarity of horizontal sync pulses outside of vertical sync.</span></span>



| <span data-ttu-id="9d29e-118">值</span><span class="sxs-lookup"><span data-stu-id="9d29e-118">Value</span></span>                                                                              | <span data-ttu-id="9d29e-119">意義</span><span class="sxs-lookup"><span data-stu-id="9d29e-119">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d29e-120"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-120"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9d29e-121">複合極性是正面的。</span><span class="sxs-lookup"><span data-stu-id="9d29e-121">Composite polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="9d29e-122"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-122"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="9d29e-123">複合極性為負數。</span><span class="sxs-lookup"><span data-stu-id="9d29e-123">Composite polarity is negative.</span></span><br/>                                 |
| <dl> <span data-ttu-id="9d29e-124"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-124"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="9d29e-125">不適用。</span><span class="sxs-lookup"><span data-stu-id="9d29e-125">Not applicable.</span></span> <span data-ttu-id="9d29e-126">信號同步類型必須是數位複合。</span><span class="sxs-lookup"><span data-stu-id="9d29e-126">The signal sync type must be digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9d29e-127">**HorizontalActivePixels**</span><span class="sxs-lookup"><span data-stu-id="9d29e-127">**HorizontalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-128">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-130">水準作用中圖元的數目。</span><span class="sxs-lookup"><span data-stu-id="9d29e-130">Number of horizontally active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-131">**HorizontalBlankingPixels**</span><span class="sxs-lookup"><span data-stu-id="9d29e-131">**HorizontalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-132">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-134">水準消隱圖元的數目</span><span class="sxs-lookup"><span data-stu-id="9d29e-134">Number of horizontally blanking pixels</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-135">**HorizontalBorder**</span><span class="sxs-lookup"><span data-stu-id="9d29e-135">**HorizontalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-136">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-138">水準框線。</span><span class="sxs-lookup"><span data-stu-id="9d29e-138">Horizontal border.</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-139">**HorizontalImageSize**</span><span class="sxs-lookup"><span data-stu-id="9d29e-139">**HorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-140">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-142">水準影像大小，以毫米 (mm) 。</span><span class="sxs-lookup"><span data-stu-id="9d29e-142">Horizontal image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-143">**HorizontalPolarityType**</span><span class="sxs-lookup"><span data-stu-id="9d29e-143">**HorizontalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-144">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9d29e-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-146">水準極性類型。</span><span class="sxs-lookup"><span data-stu-id="9d29e-146">Horizontal polarity type.</span></span>



| <span data-ttu-id="9d29e-147">值</span><span class="sxs-lookup"><span data-stu-id="9d29e-147">Value</span></span>                                                                              | <span data-ttu-id="9d29e-148">意義</span><span class="sxs-lookup"><span data-stu-id="9d29e-148">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d29e-149"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-149"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9d29e-150">水準極性是正面的。</span><span class="sxs-lookup"><span data-stu-id="9d29e-150">Horizontal polarity is positive.</span></span><br/>                               |
| <dl> <span data-ttu-id="9d29e-151"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-151"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="9d29e-152">水準極性為負數。</span><span class="sxs-lookup"><span data-stu-id="9d29e-152">Horizontal polarity is negative.</span></span><br/>                               |
| <dl> <span data-ttu-id="9d29e-153"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-153"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="9d29e-154">不適用。</span><span class="sxs-lookup"><span data-stu-id="9d29e-154">Not applicable.</span></span> <span data-ttu-id="9d29e-155">信號同步類型必須是數位分開的。</span><span class="sxs-lookup"><span data-stu-id="9d29e-155">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9d29e-156">**HorizontalRefreshRateDenominator**</span><span class="sxs-lookup"><span data-stu-id="9d29e-156">**HorizontalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-157">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-159">水準重新整理率分母。</span><span class="sxs-lookup"><span data-stu-id="9d29e-159">Horizontal refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-160">**HorizontalRefreshRateNumerator**</span><span class="sxs-lookup"><span data-stu-id="9d29e-160">**HorizontalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-161">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-163">以赫茲為單位的水準重新整理速率分子 (Hz) 。</span><span class="sxs-lookup"><span data-stu-id="9d29e-163">Horizontal refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-164">**HorizontalSyncOffset**</span><span class="sxs-lookup"><span data-stu-id="9d29e-164">**HorizontalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-165">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-167">水準同步位移。</span><span class="sxs-lookup"><span data-stu-id="9d29e-167">Horizontal sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-168">**HorizontalSyncPulseWidth**</span><span class="sxs-lookup"><span data-stu-id="9d29e-168">**HorizontalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-169">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-171">水準同步脈衝寬度。</span><span class="sxs-lookup"><span data-stu-id="9d29e-171">Horizontal sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-172">**IsInterlaced**</span><span class="sxs-lookup"><span data-stu-id="9d29e-172">**IsInterlaced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-173">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9d29e-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-175">指出顯示模式是否為交錯式。</span><span class="sxs-lookup"><span data-stu-id="9d29e-175">Indicates whether the display mode is interlaced.</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-176">**IsSerrationRequired**</span><span class="sxs-lookup"><span data-stu-id="9d29e-176">**IsSerrationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-177">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9d29e-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-179">指出需要何種類型的 serration （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="9d29e-179">Indicates what type of serration is required, if appropriate.</span></span>



| <span data-ttu-id="9d29e-180">值</span><span class="sxs-lookup"><span data-stu-id="9d29e-180">Value</span></span>                                                                              | <span data-ttu-id="9d29e-181">意義</span><span class="sxs-lookup"><span data-stu-id="9d29e-181">Meaning</span></span>                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d29e-182"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9d29e-183">控制器應該在垂直同步期間提供水準同步處理。</span><span class="sxs-lookup"><span data-stu-id="9d29e-183">Controller shall supply horizontal sync during vertical sync.</span></span><br/>                                 |
| <dl> <span data-ttu-id="9d29e-184"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="9d29e-185">控制器不應該在垂直同步期間提供水準同步處理。</span><span class="sxs-lookup"><span data-stu-id="9d29e-185">Controller shall not supply horizontal sync during vertical sync.</span></span><br/>                             |
| <dl> <span data-ttu-id="9d29e-186"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-186"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="9d29e-187">不適用。</span><span class="sxs-lookup"><span data-stu-id="9d29e-187">Not applicable.</span></span> <span data-ttu-id="9d29e-188">信號同步類型必須是極性、類比複合或數位複合。</span><span class="sxs-lookup"><span data-stu-id="9d29e-188">The signal sync type must be bipolar, analog composite, or digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9d29e-189">**IsSyncOnRGB**</span><span class="sxs-lookup"><span data-stu-id="9d29e-189">**IsSyncOnRGB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-190">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9d29e-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-192">指出應該同步處理的視訊訊號行（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="9d29e-192">Indicates which video signal lines should be synchronized, if appropriate.</span></span>



| <span data-ttu-id="9d29e-193">值</span><span class="sxs-lookup"><span data-stu-id="9d29e-193">Value</span></span>                                                                              | <span data-ttu-id="9d29e-194">意義</span><span class="sxs-lookup"><span data-stu-id="9d29e-194">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d29e-195"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-195"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9d29e-196">同步脈衝應該會出現在所有3個視訊訊號線上。</span><span class="sxs-lookup"><span data-stu-id="9d29e-196">Sync pulse should appear on all 3 video signal lines.</span></span><br/>                  |
| <dl> <span data-ttu-id="9d29e-197"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-197"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="9d29e-198">同步脈衝應只出現在綠色的視訊訊號線上。</span><span class="sxs-lookup"><span data-stu-id="9d29e-198">Sync pulse should only appear on the green video signal line.</span></span><br/>          |
| <dl> <span data-ttu-id="9d29e-199"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-199"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="9d29e-200">不適用。</span><span class="sxs-lookup"><span data-stu-id="9d29e-200">Not applicable.</span></span> <span data-ttu-id="9d29e-201">信號同步類型必須是極性類比複合。</span><span class="sxs-lookup"><span data-stu-id="9d29e-201">The signal sync type must be bipolar analog composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9d29e-202">**PixelClockRate**</span><span class="sxs-lookup"><span data-stu-id="9d29e-202">**PixelClockRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-203">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9d29e-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-205">以赫茲為單位的圖元頻率速率 (Hz) 。</span><span class="sxs-lookup"><span data-stu-id="9d29e-205">Pixel clock rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-206">**StereoModeType**</span><span class="sxs-lookup"><span data-stu-id="9d29e-206">**StereoModeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-207">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9d29e-207">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-209">身歷聲模式類型。</span><span class="sxs-lookup"><span data-stu-id="9d29e-209">Stereo mode type.</span></span> <span data-ttu-id="9d29e-210">下表列出可能的值。</span><span class="sxs-lookup"><span data-stu-id="9d29e-210">The following table lists the possible values.</span></span>



| <span data-ttu-id="9d29e-211">值</span><span class="sxs-lookup"><span data-stu-id="9d29e-211">Value</span></span>                                                                              | <span data-ttu-id="9d29e-212">意義</span><span class="sxs-lookup"><span data-stu-id="9d29e-212">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d29e-213"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-213"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9d29e-214">沒有身歷聲。</span><span class="sxs-lookup"><span data-stu-id="9d29e-214">No stereo.</span></span><br/>                                               |
| <dl> <span data-ttu-id="9d29e-215"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-215"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="9d29e-216">在身歷聲同步上具有右影像的欄位順序身歷聲。</span><span class="sxs-lookup"><span data-stu-id="9d29e-216">Field sequential stereo with right image on stereo sync.</span></span><br/> |
| <dl> <span data-ttu-id="9d29e-217"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-217"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="9d29e-218">具有左邊影像的欄位連續身歷聲（身歷聲同步）。</span><span class="sxs-lookup"><span data-stu-id="9d29e-218">Field sequential stereo with left image on stereo sync.</span></span><br/>  |
| <dl> <span data-ttu-id="9d29e-219"><dt>3 (0x3) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-219"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="9d29e-220">雙向交錯身歷聲，在偶數線條上有右影像。</span><span class="sxs-lookup"><span data-stu-id="9d29e-220">2-way Interleaved Stereo with Right Image on Even Lines.</span></span><br/> |
| <dl> <span data-ttu-id="9d29e-221"><dt>4 (0x4) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-221"><dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="9d29e-222">雙向交錯的身歷聲，在偶數行上具有左邊的影像。</span><span class="sxs-lookup"><span data-stu-id="9d29e-222">2-way Interleaved Stereo with Left Image on Even Lines.</span></span><br/>  |
| <dl> <span data-ttu-id="9d29e-223"><dt>5 (0x5) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-223"><dt>5 (0x5)</dt></span></span> </dl> | <span data-ttu-id="9d29e-224">4向交錯式身歷聲。</span><span class="sxs-lookup"><span data-stu-id="9d29e-224">4-way Interleaved Stereo.</span></span><br/>                                |
| <dl> <span data-ttu-id="9d29e-225"><dt>6 (0x6) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-225"><dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="9d29e-226">並列交錯身歷聲。</span><span class="sxs-lookup"><span data-stu-id="9d29e-226">Side-by-Side Interleaved Stereo.</span></span><br/>                         |



 

</dd> <dt>

<span data-ttu-id="9d29e-227">**SyncSignalType**</span><span class="sxs-lookup"><span data-stu-id="9d29e-227">**SyncSignalType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-228">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9d29e-228">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-230">信號同步處理類型。</span><span class="sxs-lookup"><span data-stu-id="9d29e-230">Signal sync type.</span></span> <span data-ttu-id="9d29e-231">下表列出可能的值。</span><span class="sxs-lookup"><span data-stu-id="9d29e-231">The following table lists the possible values.</span></span>



| <span data-ttu-id="9d29e-232">值</span><span class="sxs-lookup"><span data-stu-id="9d29e-232">Value</span></span>                                                                              | <span data-ttu-id="9d29e-233">意義</span><span class="sxs-lookup"><span data-stu-id="9d29e-233">Meaning</span></span>                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="9d29e-234"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-234"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9d29e-235">類比複合</span><span class="sxs-lookup"><span data-stu-id="9d29e-235">Analog Composite</span></span><br/>         |
| <dl> <span data-ttu-id="9d29e-236"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-236"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="9d29e-237">極性類比複合</span><span class="sxs-lookup"><span data-stu-id="9d29e-237">Bipolar Analog Composite</span></span><br/> |
| <dl> <span data-ttu-id="9d29e-238"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-238"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="9d29e-239">數位複合</span><span class="sxs-lookup"><span data-stu-id="9d29e-239">Digital Composite</span></span><br/>        |
| <dl> <span data-ttu-id="9d29e-240"><dt>3 (0x3) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-240"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="9d29e-241">數位分開</span><span class="sxs-lookup"><span data-stu-id="9d29e-241">Digital Separate</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="9d29e-242">**VerticalActivePixels**</span><span class="sxs-lookup"><span data-stu-id="9d29e-242">**VerticalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-243">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-245">垂直現用圖元的數目。</span><span class="sxs-lookup"><span data-stu-id="9d29e-245">Number of vertically active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-246">**VerticalBlankingPixels**</span><span class="sxs-lookup"><span data-stu-id="9d29e-246">**VerticalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-247">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-249">垂直消隱圖元的數目。</span><span class="sxs-lookup"><span data-stu-id="9d29e-249">Number of vertically blanking pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-250">**VerticalBorder**</span><span class="sxs-lookup"><span data-stu-id="9d29e-250">**VerticalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-251">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-253">垂直框線。</span><span class="sxs-lookup"><span data-stu-id="9d29e-253">Vertical border.</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-254">**VerticalImageSize**</span><span class="sxs-lookup"><span data-stu-id="9d29e-254">**VerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-255">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-257">垂直影像大小，以毫米 (mm) 。</span><span class="sxs-lookup"><span data-stu-id="9d29e-257">Vertical image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-258">**VerticalPolarityType**</span><span class="sxs-lookup"><span data-stu-id="9d29e-258">**VerticalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-259">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9d29e-259">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-261">垂直極性類型。</span><span class="sxs-lookup"><span data-stu-id="9d29e-261">Vertical polarity type.</span></span>



| <span data-ttu-id="9d29e-262">值</span><span class="sxs-lookup"><span data-stu-id="9d29e-262">Value</span></span>                                                                              | <span data-ttu-id="9d29e-263">意義</span><span class="sxs-lookup"><span data-stu-id="9d29e-263">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d29e-264"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-264"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9d29e-265">垂直極性是正面的。</span><span class="sxs-lookup"><span data-stu-id="9d29e-265">Vertical polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="9d29e-266"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-266"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="9d29e-267">垂直極性為負數</span><span class="sxs-lookup"><span data-stu-id="9d29e-267">Vertical polarity is negative</span></span><br/>                                  |
| <dl> <span data-ttu-id="9d29e-268"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-268"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="9d29e-269">不適用。</span><span class="sxs-lookup"><span data-stu-id="9d29e-269">Not applicable.</span></span> <span data-ttu-id="9d29e-270">信號同步類型必須是數位分開的。</span><span class="sxs-lookup"><span data-stu-id="9d29e-270">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9d29e-271">**VerticalRefreshRateDenominator**</span><span class="sxs-lookup"><span data-stu-id="9d29e-271">**VerticalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-272">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-274">垂直重新整理率分母。</span><span class="sxs-lookup"><span data-stu-id="9d29e-274">Vertical refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-275">**VerticalRefreshRateNumerator**</span><span class="sxs-lookup"><span data-stu-id="9d29e-275">**VerticalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-276">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-278">以赫茲為單位的垂直重新整理率分子 (Hz) 。</span><span class="sxs-lookup"><span data-stu-id="9d29e-278">Vertical refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-279">**VerticalSyncOffset**</span><span class="sxs-lookup"><span data-stu-id="9d29e-279">**VerticalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-280">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-282">垂直同步位移。</span><span class="sxs-lookup"><span data-stu-id="9d29e-282">Vertical sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-283">**VerticalSyncPulseWidth**</span><span class="sxs-lookup"><span data-stu-id="9d29e-283">**VerticalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-284">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9d29e-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-286">垂直同步脈衝寬度。</span><span class="sxs-lookup"><span data-stu-id="9d29e-286">Vertical sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="9d29e-287">VideoStandardType</span><span class="sxs-lookup"><span data-stu-id="9d29e-287">VideoStandardType</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d29e-288">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9d29e-288">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9d29e-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9d29e-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d29e-290">影片標準類型。</span><span class="sxs-lookup"><span data-stu-id="9d29e-290">Video standard type.</span></span>



| <span data-ttu-id="9d29e-291">值</span><span class="sxs-lookup"><span data-stu-id="9d29e-291">Value</span></span>                                                                                | <span data-ttu-id="9d29e-292">意義</span><span class="sxs-lookup"><span data-stu-id="9d29e-292">Meaning</span></span>                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d29e-293"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-293"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="9d29e-294">其他</span><span class="sxs-lookup"><span data-stu-id="9d29e-294">Other</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="9d29e-295"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-295"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="9d29e-296">VESA DMT。</span><span class="sxs-lookup"><span data-stu-id="9d29e-296">VESA DMT.</span></span> <span data-ttu-id="9d29e-297">從視頻電子產品標準關聯 (VESA) 顯示監視時間規格。</span><span class="sxs-lookup"><span data-stu-id="9d29e-297">From Video Electronics Standard Association (VESA) Display Monitor Timings specification.</span></span><br/> |
| <dl> <span data-ttu-id="9d29e-298"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-298"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="9d29e-299">VESA GTF。</span><span class="sxs-lookup"><span data-stu-id="9d29e-299">VESA GTF.</span></span> <span data-ttu-id="9d29e-300">從 VESA 一般化計時公式標準。</span><span class="sxs-lookup"><span data-stu-id="9d29e-300">From VESA Generalized Timing Formula standard.</span></span><br/>                                            |
| <dl> <span data-ttu-id="9d29e-301"><dt>3 (0x3) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-301"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="9d29e-302">VESA CVT/來自 VESA 協調的影片計時標準。</span><span class="sxs-lookup"><span data-stu-id="9d29e-302">VESA CVT/ From VESA Coordinated Video Timings standard.</span></span><br/>                                             |
| <dl> <span data-ttu-id="9d29e-303"><dt>4 (0x4) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-303"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="9d29e-304">IBM</span><span class="sxs-lookup"><span data-stu-id="9d29e-304">IBM</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="9d29e-305"><dt>5 (0x5) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-305"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="9d29e-306">蘋果</span><span class="sxs-lookup"><span data-stu-id="9d29e-306">APPLE</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="9d29e-307"><dt>6 (0x6) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-307"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="9d29e-308">NTSC M</span><span class="sxs-lookup"><span data-stu-id="9d29e-308">NTSC M</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="9d29e-309"><dt>7 (0x7) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-309"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="9d29e-310">NTSC J</span><span class="sxs-lookup"><span data-stu-id="9d29e-310">NTSC J</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="9d29e-311"><dt>8 (0x8) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-311"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="9d29e-312">NTSC 433</span><span class="sxs-lookup"><span data-stu-id="9d29e-312">NTSC 433</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="9d29e-313"><dt>9 (0x9) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-313"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="9d29e-314">PAL B</span><span class="sxs-lookup"><span data-stu-id="9d29e-314">PAL B</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="9d29e-315"><dt>10 (0xA) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-315"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="9d29e-316">PAL B1</span><span class="sxs-lookup"><span data-stu-id="9d29e-316">PAL B1</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="9d29e-317"><dt>11 (0xB) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-317"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="9d29e-318">PAL G</span><span class="sxs-lookup"><span data-stu-id="9d29e-318">PAL G</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="9d29e-319"><dt>12 (0xC) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-319"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="9d29e-320">PAL H</span><span class="sxs-lookup"><span data-stu-id="9d29e-320">PAL H</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="9d29e-321"><dt>13 (0xD) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-321"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="9d29e-322">PAL I</span><span class="sxs-lookup"><span data-stu-id="9d29e-322">PAL I</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="9d29e-323"><dt>14 (0xE) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-323"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="9d29e-324">PAL D</span><span class="sxs-lookup"><span data-stu-id="9d29e-324">PAL D</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="9d29e-325"><dt>15 (0xF) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-325"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="9d29e-326">PAL N</span><span class="sxs-lookup"><span data-stu-id="9d29e-326">PAL N</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="9d29e-327"><dt>16 (0x10) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-327"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="9d29e-328">PAL NC</span><span class="sxs-lookup"><span data-stu-id="9d29e-328">PAL NC</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="9d29e-329"><dt>17 (0x11) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-329"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="9d29e-330">SECAM B</span><span class="sxs-lookup"><span data-stu-id="9d29e-330">SECAM B</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="9d29e-331"><dt>18 (0x12) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-331"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="9d29e-332">SECAM D</span><span class="sxs-lookup"><span data-stu-id="9d29e-332">SECAM D</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="9d29e-333"><dt>19 (0x13) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-333"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="9d29e-334">SECAM G</span><span class="sxs-lookup"><span data-stu-id="9d29e-334">SECAM G</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="9d29e-335"><dt>20 (0x14) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-335"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="9d29e-336">SECAM H</span><span class="sxs-lookup"><span data-stu-id="9d29e-336">SECAM H</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="9d29e-337"><dt>21 (0x15) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-337"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="9d29e-338">SECAM K</span><span class="sxs-lookup"><span data-stu-id="9d29e-338">SECAM K</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="9d29e-339"><dt>22 (0x16) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-339"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="9d29e-340">SECAM 版 K1</span><span class="sxs-lookup"><span data-stu-id="9d29e-340">SECAM K1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="9d29e-341"><dt>23 (0x17) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-341"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="9d29e-342">SECAM L</span><span class="sxs-lookup"><span data-stu-id="9d29e-342">SECAM L</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="9d29e-343"><dt>24 (0x18) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-343"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="9d29e-344">SECAM L1</span><span class="sxs-lookup"><span data-stu-id="9d29e-344">SECAM L1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="9d29e-345"><dt>25 (0x19) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-345"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="9d29e-346">EIA861</span><span class="sxs-lookup"><span data-stu-id="9d29e-346">EIA861</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="9d29e-347"><dt>26 (0x1A) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-347"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="9d29e-348">EIA861A</span><span class="sxs-lookup"><span data-stu-id="9d29e-348">EIA861A</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="9d29e-349"><dt>27 (0x1B) </dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-349"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="9d29e-350">EIA861B</span><span class="sxs-lookup"><span data-stu-id="9d29e-350">EIA861B</span></span><br/>                                                                                             |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d29e-351">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d29e-351">Requirements</span></span>



| <span data-ttu-id="9d29e-352">需求</span><span class="sxs-lookup"><span data-stu-id="9d29e-352">Requirement</span></span> | <span data-ttu-id="9d29e-353">值</span><span class="sxs-lookup"><span data-stu-id="9d29e-353">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d29e-354">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d29e-354">Minimum supported client</span></span><br/> | <span data-ttu-id="9d29e-355">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d29e-355">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9d29e-356">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d29e-356">Minimum supported server</span></span><br/> | <span data-ttu-id="9d29e-357">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d29e-357">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9d29e-358">命名空間</span><span class="sxs-lookup"><span data-stu-id="9d29e-358">Namespace</span></span><br/>                | <span data-ttu-id="9d29e-359">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="9d29e-359">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="9d29e-360">MOF</span><span class="sxs-lookup"><span data-stu-id="9d29e-360">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d29e-361"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-361"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d29e-362">DLL</span><span class="sxs-lookup"><span data-stu-id="9d29e-362">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d29e-363"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d29e-363"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d29e-364">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d29e-364">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d29e-365">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="9d29e-365">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




