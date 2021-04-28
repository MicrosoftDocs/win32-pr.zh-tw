---
description: SystemConfig_Video 類別-此類別是影片設定事件的事件種類類別。
ms.assetid: ddb5924b-70d9-4693-bf68-0536c3c3fa8d
title: SystemConfig_Video 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Video
- SystemConfig_Video.MemorySize
- SystemConfig_Video.XResolution
- SystemConfig_Video.YResolution
- SystemConfig_Video.BitsPerPixel
- SystemConfig_Video.VRefresh
- SystemConfig_Video.ChipType
- SystemConfig_Video.DACType
- SystemConfig_Video.AdapterString
- SystemConfig_Video.BiosString
- SystemConfig_Video.DeviceId
- SystemConfig_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 716194eb9ceb67b609f886482393795eaef2ef09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105896"
---
# <a name="systemconfig_video-class"></a><span data-ttu-id="8f608-103">SystemConfig \_ 影片類別</span><span class="sxs-lookup"><span data-stu-id="8f608-103">SystemConfig\_Video class</span></span>

<span data-ttu-id="8f608-104">此類別是影片設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="8f608-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="8f608-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="8f608-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f608-106">語法</span><span class="sxs-lookup"><span data-stu-id="8f608-106">Syntax</span></span>

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_Video : SystemConfig
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a><span data-ttu-id="8f608-107">成員</span><span class="sxs-lookup"><span data-stu-id="8f608-107">Members</span></span>

<span data-ttu-id="8f608-108">**SystemConfig \_ Video** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8f608-108">The **SystemConfig\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="8f608-109">屬性</span><span class="sxs-lookup"><span data-stu-id="8f608-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f608-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8f608-110">Properties</span></span>

<span data-ttu-id="8f608-111">**SystemConfig \_ Video** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8f608-111">The **SystemConfig\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f608-112">**AdapterString**</span><span class="sxs-lookup"><span data-stu-id="8f608-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-113">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f608-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f608-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f608-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-115">限定詞： **WmiDataId** (8) ， **最大** (256) ， **格式 ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="8f608-115">Qualifiers: **WmiDataId** (8), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="8f608-116">介面卡的名稱或描述。</span><span class="sxs-lookup"><span data-stu-id="8f608-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8f608-117">**BiosString**</span><span class="sxs-lookup"><span data-stu-id="8f608-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-118">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f608-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f608-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f608-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-120">限定詞： **WmiDataId** (9) ， **最大** (256) ， **格式 ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="8f608-120">Qualifiers: **WmiDataId** (9), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="8f608-121">介面卡的 BIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="8f608-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8f608-122">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="8f608-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-123">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f608-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f608-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f608-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-125">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="8f608-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="8f608-126">用來顯示每個圖元的位數。</span><span class="sxs-lookup"><span data-stu-id="8f608-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="8f608-127">**ChipType**</span><span class="sxs-lookup"><span data-stu-id="8f608-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-128">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f608-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f608-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f608-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-130">限定詞： **WmiDataId** (6) ， **最大** (256) ， **格式 ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="8f608-130">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="8f608-131">介面卡的晶片名稱。</span><span class="sxs-lookup"><span data-stu-id="8f608-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8f608-132">**DACType**</span><span class="sxs-lookup"><span data-stu-id="8f608-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-133">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f608-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f608-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f608-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-135">限定詞： **WmiDataId** (7) ， **最大** (256) ， **格式 ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="8f608-135">Qualifiers: **WmiDataId** (7), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="8f608-136">數位轉類比轉換器 (DAC 的介面卡) 晶片名稱。</span><span class="sxs-lookup"><span data-stu-id="8f608-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8f608-137">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="8f608-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-138">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f608-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f608-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f608-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-140">限定詞： **WmiDataId** (10) ， **最大** (256) ， **格式 ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="8f608-140">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="8f608-141">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="8f608-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="8f608-142">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="8f608-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-143">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f608-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f608-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f608-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-145">限定詞： **WmiDataId** (1) </span><span class="sxs-lookup"><span data-stu-id="8f608-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="8f608-146">支援的最大記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8f608-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8f608-147">**StateFlags**</span><span class="sxs-lookup"><span data-stu-id="8f608-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-148">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f608-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f608-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f608-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-150">限定詞： **WmiDataId** (11) ， **格式 ( "x" )**</span><span class="sxs-lookup"><span data-stu-id="8f608-150">Qualifiers: **WmiDataId** (11), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="8f608-151">裝置狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="8f608-151">Device state flags.</span></span> <span data-ttu-id="8f608-152">它可以是下列任何合理的組合。</span><span class="sxs-lookup"><span data-stu-id="8f608-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="8f608-153">值</span><span class="sxs-lookup"><span data-stu-id="8f608-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="8f608-154">意義</span><span class="sxs-lookup"><span data-stu-id="8f608-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="8f608-155"><dt>**顯示 \_\_連接 \_ 到 \_ 桌面**</dt> <dt>1 (0x1)</dt>的裝置</span><span class="sxs-lookup"><span data-stu-id="8f608-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="8f608-156">裝置是桌面的一部分。</span><span class="sxs-lookup"><span data-stu-id="8f608-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="8f608-157"><dt>**顯示 \_裝置 \_ 鏡像 \_ 驅動程式**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="8f608-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="8f608-158">代表用來鏡像應用程式繪圖以連接到遠端電腦或其他用途的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="8f608-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="8f608-159">不可見的虛擬監視器與此裝置相關聯。</span><span class="sxs-lookup"><span data-stu-id="8f608-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="8f608-160">例如，NetMeeting 會使用它。</span><span class="sxs-lookup"><span data-stu-id="8f608-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="8f608-161"><dt>**顯示 \_裝置 \_ MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="8f608-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="8f608-162">裝置的顯示模式比輸出裝置支援的還多。</span><span class="sxs-lookup"><span data-stu-id="8f608-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="8f608-163"><dt>**顯示 \_裝置 \_ 主要 \_ 裝置**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="8f608-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="8f608-164">主要桌面在裝置上。</span><span class="sxs-lookup"><span data-stu-id="8f608-164">The primary desktop is on the device.</span></span> <span data-ttu-id="8f608-165">針對具有單一顯示配接器的系統，一律會設定此設定。</span><span class="sxs-lookup"><span data-stu-id="8f608-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="8f608-166">針對具有多個顯示配接器的系統，只有一部裝置可以有此組。</span><span class="sxs-lookup"><span data-stu-id="8f608-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="8f608-167"><dt>**顯示 \_裝置 \_ 可移動**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="8f608-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="8f608-168">裝置為可移動;它不能是主顯示器。</span><span class="sxs-lookup"><span data-stu-id="8f608-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="8f608-169"><dt>**顯示 \_裝置 \_ VGA \_ 相容**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="8f608-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="8f608-170">裝置與 VGA 相容。</span><span class="sxs-lookup"><span data-stu-id="8f608-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="8f608-171">**VRefresh**</span><span class="sxs-lookup"><span data-stu-id="8f608-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-172">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f608-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f608-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f608-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-174">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="8f608-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="8f608-175">目前的重新整理速率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="8f608-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="8f608-176">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="8f608-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-177">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f608-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f608-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f608-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-179">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="8f608-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="8f608-180">目前的水準圖元數目。</span><span class="sxs-lookup"><span data-stu-id="8f608-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8f608-181">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="8f608-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-182">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f608-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f608-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f608-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-184">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="8f608-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="8f608-185">目前的垂直圖元數目。</span><span class="sxs-lookup"><span data-stu-id="8f608-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f608-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f608-186">Requirements</span></span>



| <span data-ttu-id="8f608-187">需求</span><span class="sxs-lookup"><span data-stu-id="8f608-187">Requirement</span></span> | <span data-ttu-id="8f608-188">值</span><span class="sxs-lookup"><span data-stu-id="8f608-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8f608-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f608-189">Minimum supported client</span></span><br/> | <span data-ttu-id="8f608-190">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f608-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8f608-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f608-191">Minimum supported server</span></span><br/> | <span data-ttu-id="8f608-192">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f608-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f608-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f608-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f608-194">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="8f608-194">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




