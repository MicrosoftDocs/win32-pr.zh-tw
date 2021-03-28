---
description: 此類別是實體磁片設定事件的事件種類類別。
ms.assetid: 850a6b2c-69e6-47ae-95ff-585fcc70c1c8
title: SystemConfig_PhyDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PhyDisk
- SystemConfig_PhyDisk.DiskNumber
- SystemConfig_PhyDisk.BytesPerSector
- SystemConfig_PhyDisk.SectorsPerTrack
- SystemConfig_PhyDisk.TracksPerCylinder
- SystemConfig_PhyDisk.Cylinders
- SystemConfig_PhyDisk.SCSIPort
- SystemConfig_PhyDisk.SCSIPath
- SystemConfig_PhyDisk.SCSITarget
- SystemConfig_PhyDisk.SCSILun
- SystemConfig_PhyDisk.Manufacturer
- SystemConfig_PhyDisk.PartitionCount
- SystemConfig_PhyDisk.WriteCacheEnabled
- SystemConfig_PhyDisk.Pad
- SystemConfig_PhyDisk.BootDriveLetter
- SystemConfig_PhyDisk.Spare
api_type:
- NA
api_location: ''
ms.openlocfilehash: d868e3943f22a71b4513f4f77841ddea9204ffea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972112"
---
# <a name="systemconfig_phydisk-class"></a><span data-ttu-id="67ca4-103">SystemConfig \_ PhyDisk 類別</span><span class="sxs-lookup"><span data-stu-id="67ca4-103">SystemConfig\_PhyDisk class</span></span>

<span data-ttu-id="67ca4-104">此類別是實體磁片設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="67ca4-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="67ca4-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="67ca4-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ca4-106">語法</span><span class="sxs-lookup"><span data-stu-id="67ca4-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_PhyDisk : SystemConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  char16 Manufacturer[];
  uint32 PartitionCount;
  uint8  WriteCacheEnabled;
  uint8  Pad;
  char16 BootDriveLetter[];
  char16 Spare[];
};
```

## <a name="members"></a><span data-ttu-id="67ca4-107">成員</span><span class="sxs-lookup"><span data-stu-id="67ca4-107">Members</span></span>

<span data-ttu-id="67ca4-108">**SystemConfig \_ PhyDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="67ca4-108">The **SystemConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="67ca4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="67ca4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67ca4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="67ca4-110">Properties</span></span>

<span data-ttu-id="67ca4-111">**SystemConfig \_ PhyDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="67ca4-111">The **SystemConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67ca4-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="67ca4-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-113">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="67ca4-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-115">限定詞： **WmiDataId** (14) 、 **Max** (3) 、 **Format ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="67ca4-115">Qualifiers: **WmiDataId** (14), **Max** (3), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-116">開機磁片磁碟機的磁碟機號，格式為 " <letter> ："。</span><span class="sxs-lookup"><span data-stu-id="67ca4-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="67ca4-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="67ca4-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-120">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="67ca4-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-121">每個磁區中實體磁片磁碟機的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="67ca4-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-122">**缸**</span><span class="sxs-lookup"><span data-stu-id="67ca4-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-123">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="67ca4-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-125">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="67ca4-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-126">實體磁片磁碟機上的圓柱總數。</span><span class="sxs-lookup"><span data-stu-id="67ca4-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="67ca4-127">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="67ca4-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="67ca4-128">如果磁片磁碟機使用轉譯配置來支援高容量磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="67ca4-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="67ca4-129">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="67ca4-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="67ca4-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-131">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="67ca4-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-133">限定詞： **WmiDataId** (1) </span><span class="sxs-lookup"><span data-stu-id="67ca4-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-134">包含此分割區之磁片的索引編號。</span><span class="sxs-lookup"><span data-stu-id="67ca4-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-135">**製造商**</span><span class="sxs-lookup"><span data-stu-id="67ca4-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-136">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="67ca4-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-138">限定詞： **WmiDataId** (10) ， **最大** (256) ， **格式 ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="67ca4-138">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-139">磁片磁碟機製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="67ca4-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-140">**墊**</span><span class="sxs-lookup"><span data-stu-id="67ca4-140">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-141">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="67ca4-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-143">限定詞： **WmiDataId** (13) </span><span class="sxs-lookup"><span data-stu-id="67ca4-143">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-144">未使用。</span><span class="sxs-lookup"><span data-stu-id="67ca4-144">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-145">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="67ca4-145">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="67ca4-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-148">限定詞： **WmiDataId** (11) </span><span class="sxs-lookup"><span data-stu-id="67ca4-148">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-149">此實體磁片磁碟機上作業系統可辨識的磁碟分割數目。</span><span class="sxs-lookup"><span data-stu-id="67ca4-149">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-150">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="67ca4-150">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="67ca4-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-153">限定詞： **WmiDataId** (9) </span><span class="sxs-lookup"><span data-stu-id="67ca4-153">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-154">Scsi 邏輯單元編號 (LUN) 的 SCSI 介面卡。</span><span class="sxs-lookup"><span data-stu-id="67ca4-154">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-155">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="67ca4-155">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-156">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="67ca4-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-158">限定詞： **WmiDataId** (7) </span><span class="sxs-lookup"><span data-stu-id="67ca4-158">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-159">SCSI 介面卡的 SCSI 匯流排號碼。</span><span class="sxs-lookup"><span data-stu-id="67ca4-159">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-160">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="67ca4-160">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-161">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="67ca4-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-163">限定詞： **WmiDataId** (6) </span><span class="sxs-lookup"><span data-stu-id="67ca4-163">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-164">SCSI 介面卡的 SCSI 號碼。</span><span class="sxs-lookup"><span data-stu-id="67ca4-164">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-165">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="67ca4-165">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-166">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="67ca4-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-168">限定詞： **WmiDataId** (8) </span><span class="sxs-lookup"><span data-stu-id="67ca4-168">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-169">包含目標裝置的編號。</span><span class="sxs-lookup"><span data-stu-id="67ca4-169">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-170">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="67ca4-170">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-171">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="67ca4-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-173">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="67ca4-173">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-174">此實體磁片磁碟機每個播放軌中的磁區數目。</span><span class="sxs-lookup"><span data-stu-id="67ca4-174">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-175">**備用**</span><span class="sxs-lookup"><span data-stu-id="67ca4-175">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-176">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="67ca4-176">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-178">限定詞： **WmiDataId** (15) 、 **Max** (2) 、 **Format ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="67ca4-178">Qualifiers: **WmiDataId** (15), **Max** (2), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-179">未使用。</span><span class="sxs-lookup"><span data-stu-id="67ca4-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-180">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="67ca4-180">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-181">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="67ca4-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-183">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="67ca4-183">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-184">實體磁片磁碟機上每個圓柱的曲目數目。</span><span class="sxs-lookup"><span data-stu-id="67ca4-184">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="67ca4-185">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="67ca4-185">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="67ca4-186">如果磁片磁碟機使用轉譯配置來支援高容量磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="67ca4-186">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="67ca4-187">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="67ca4-187">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="67ca4-188">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="67ca4-188">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ca4-189">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="67ca4-189">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ca4-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ca4-191">限定詞： **WmiDataId** (12) </span><span class="sxs-lookup"><span data-stu-id="67ca4-191">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="67ca4-192">如果已啟用寫入快取，則為 True。</span><span class="sxs-lookup"><span data-stu-id="67ca4-192">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67ca4-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="67ca4-193">Requirements</span></span>



| <span data-ttu-id="67ca4-194">需求</span><span class="sxs-lookup"><span data-stu-id="67ca4-194">Requirement</span></span> | <span data-ttu-id="67ca4-195">值</span><span class="sxs-lookup"><span data-stu-id="67ca4-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="67ca4-196">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67ca4-196">Minimum supported client</span></span><br/> | <span data-ttu-id="67ca4-197">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67ca4-197">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="67ca4-198">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67ca4-198">Minimum supported server</span></span><br/> | <span data-ttu-id="67ca4-199">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67ca4-199">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67ca4-200">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67ca4-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ca4-201">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="67ca4-201">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




