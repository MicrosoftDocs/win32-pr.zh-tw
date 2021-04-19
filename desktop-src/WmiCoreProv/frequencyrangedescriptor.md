---
description: 表示支援之頻率範圍特性的容器。
ms.assetid: eb07c10b-8d92-40bb-8a93-ebc5db46cfd3
title: FrequencyRangeDescriptor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FrequencyRangeDescriptor
- FrequencyRangeDescriptor.Origin
- FrequencyRangeDescriptor.MinVSyncNumerator
- FrequencyRangeDescriptor.MinVSyncDenominator
- FrequencyRangeDescriptor.MaxVSyncNumerator
- FrequencyRangeDescriptor.MaxVSyncDenominator
- FrequencyRangeDescriptor.MinHSyncNumerator
- FrequencyRangeDescriptor.MinHSyncDenominator
- FrequencyRangeDescriptor.MaxHSyncNumerator
- FrequencyRangeDescriptor.MaxHSyncDenominator
- FrequencyRangeDescriptor.ConstraintType
- FrequencyRangeDescriptor.ActiveWidth
- FrequencyRangeDescriptor.ActiveHeight
- FrequencyRangeDescriptor.MaxPixelRate
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: d18bee8a69fd8663ea54973d6e4e8219f5f74e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972629"
---
# <a name="frequencyrangedescriptor-class"></a><span data-ttu-id="f1495-103">FrequencyRangeDescriptor 類別</span><span class="sxs-lookup"><span data-stu-id="f1495-103">FrequencyRangeDescriptor class</span></span>

<span data-ttu-id="f1495-104">**FrequencyRangeDescriptor** WMI 類別代表支援的頻率範圍之特性的容器。</span><span class="sxs-lookup"><span data-stu-id="f1495-104">The **FrequencyRangeDescriptor** WMI class represents a container for characteristics of a supported frequency range.</span></span> <span data-ttu-id="f1495-105">這個類別的實例是 [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md)中 **MonitorFreqRanges** 陣列的元素。</span><span class="sxs-lookup"><span data-stu-id="f1495-105">Instances of this class are elements of the **MonitorFreqRanges** array in [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1495-106">語法</span><span class="sxs-lookup"><span data-stu-id="f1495-106">Syntax</span></span>

``` syntax
class FrequencyRangeDescriptor
{
  uint8  Origin;
  uint32 MinVSyncNumerator;
  uint32 MinVSyncDenominator;
  uint32 MaxVSyncNumerator;
  uint32 MaxVSyncDenominator;
  uint32 MinHSyncNumerator;
  uint32 MinHSyncDenominator;
  uint32 MaxHSyncNumerator;
  uint32 MaxHSyncDenominator;
  uint32 ConstraintType;
  uint32 ActiveWidth;
  uint32 ActiveHeight;
  uint32 MaxPixelRate;
};
```

## <a name="members"></a><span data-ttu-id="f1495-107">成員</span><span class="sxs-lookup"><span data-stu-id="f1495-107">Members</span></span>

<span data-ttu-id="f1495-108">**FrequencyRangeDescriptor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f1495-108">The **FrequencyRangeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="f1495-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f1495-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1495-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f1495-110">Properties</span></span>

<span data-ttu-id="f1495-111">**FrequencyRangeDescriptor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f1495-111">The **FrequencyRangeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1495-112">**ActiveHeight**</span><span class="sxs-lookup"><span data-stu-id="f1495-112">**ActiveHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1495-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-115">現用影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="f1495-115">Height, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="f1495-116">**ActiveWidth**</span><span class="sxs-lookup"><span data-stu-id="f1495-116">**ActiveWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-117">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1495-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-119">現用影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="f1495-119">Width, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="f1495-120">**ConstraintType**</span><span class="sxs-lookup"><span data-stu-id="f1495-120">**ConstraintType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-121">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1495-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-123">頻率範圍的條件約束類型。</span><span class="sxs-lookup"><span data-stu-id="f1495-123">Constraint type for the frequency range.</span></span>

</dd> <dt>

<span data-ttu-id="f1495-124">**MaxHSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="f1495-124">**MaxHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-125">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1495-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-127">最大水準同步分母。</span><span class="sxs-lookup"><span data-stu-id="f1495-127">Maximum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="f1495-128">**MaxHSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="f1495-128">**MaxHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1495-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-131">千赫茲 (KHz) 的最大水準同步分子。</span><span class="sxs-lookup"><span data-stu-id="f1495-131">Maximum horizontal sync numerator in kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="f1495-132">**MaxPixelRate**</span><span class="sxs-lookup"><span data-stu-id="f1495-132">**MaxPixelRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1495-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-135">以赫茲為單位的最大圖元速率 (Hz) 。</span><span class="sxs-lookup"><span data-stu-id="f1495-135">Maximum pixel rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="f1495-136">**MaxVSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="f1495-136">**MaxVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1495-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-139">最大垂直同步分母。</span><span class="sxs-lookup"><span data-stu-id="f1495-139">Maximum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="f1495-140">**MaxVSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="f1495-140">**MaxVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-141">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1495-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-143">最大垂直同步分子，以赫茲 (Hz) 。</span><span class="sxs-lookup"><span data-stu-id="f1495-143">Maximum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="f1495-144">**MinHSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="f1495-144">**MinHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-145">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1495-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-147">水準同步分母的最小值。</span><span class="sxs-lookup"><span data-stu-id="f1495-147">Minimum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="f1495-148">**MinHSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="f1495-148">**MinHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1495-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-151">中的最小水準同步分子，千赫茲 (KHz) 。</span><span class="sxs-lookup"><span data-stu-id="f1495-151">Minimum horizontal sync numerator in, kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="f1495-152">**MinVSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="f1495-152">**MinVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-153">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1495-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-155">最低垂直同步分母。</span><span class="sxs-lookup"><span data-stu-id="f1495-155">Minimum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="f1495-156">**MinVSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="f1495-156">**MinVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1495-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-159">最小的垂直同步分子，以赫茲 (Hz) 。</span><span class="sxs-lookup"><span data-stu-id="f1495-159">Minimum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="f1495-160">**起源**</span><span class="sxs-lookup"><span data-stu-id="f1495-160">**Origin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1495-161">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="f1495-161">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f1495-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1495-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1495-163">起源。</span><span class="sxs-lookup"><span data-stu-id="f1495-163">Origin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1495-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1495-164">Requirements</span></span>



| <span data-ttu-id="f1495-165">需求</span><span class="sxs-lookup"><span data-stu-id="f1495-165">Requirement</span></span> | <span data-ttu-id="f1495-166">值</span><span class="sxs-lookup"><span data-stu-id="f1495-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1495-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1495-167">Minimum supported client</span></span><br/> | <span data-ttu-id="f1495-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1495-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f1495-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1495-169">Minimum supported server</span></span><br/> | <span data-ttu-id="f1495-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1495-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f1495-171">命名空間</span><span class="sxs-lookup"><span data-stu-id="f1495-171">Namespace</span></span><br/>                | <span data-ttu-id="f1495-172">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="f1495-172">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="f1495-173">MOF</span><span class="sxs-lookup"><span data-stu-id="f1495-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1495-174"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1495-174"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1495-175">DLL</span><span class="sxs-lookup"><span data-stu-id="f1495-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1495-176"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1495-176"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1495-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1495-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1495-178">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="f1495-178">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




