---
description: SystemConfig_PhyDisk 類別-此類別是實體磁片設定事件的事件種類類別。
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
ms.openlocfilehash: 52ab249ab5087a1528317687d90f6d8fa665bc1a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106096"
---
# <a name="systemconfig_phydisk-class"></a><span data-ttu-id="aad0b-103">SystemConfig \_ PhyDisk 類別</span><span class="sxs-lookup"><span data-stu-id="aad0b-103">SystemConfig\_PhyDisk class</span></span>

<span data-ttu-id="aad0b-104">此類別是實體磁片設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="aad0b-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="aad0b-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="aad0b-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aad0b-106">語法</span><span class="sxs-lookup"><span data-stu-id="aad0b-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="aad0b-107">成員</span><span class="sxs-lookup"><span data-stu-id="aad0b-107">Members</span></span>

<span data-ttu-id="aad0b-108">**SystemConfig \_ PhyDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="aad0b-108">The **SystemConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="aad0b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="aad0b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aad0b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="aad0b-110">Properties</span></span>

<span data-ttu-id="aad0b-111">**SystemConfig \_ PhyDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="aad0b-111">The **SystemConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aad0b-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="aad0b-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-113">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="aad0b-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-115">限定詞： **WmiDataId** (14) 、 **Max** (3) 、 **Format ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="aad0b-115">Qualifiers: **WmiDataId** (14), **Max** (3), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-116">開機磁片磁碟機的磁碟機號，格式為 " <letter> ："。</span><span class="sxs-lookup"><span data-stu-id="aad0b-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="aad0b-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aad0b-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-120">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="aad0b-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-121">每個磁區中實體磁片磁碟機的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="aad0b-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-122">**缸**</span><span class="sxs-lookup"><span data-stu-id="aad0b-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-123">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="aad0b-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-125">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="aad0b-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-126">實體磁片磁碟機上的圓柱總數。</span><span class="sxs-lookup"><span data-stu-id="aad0b-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="aad0b-127">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="aad0b-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="aad0b-128">如果磁片磁碟機使用轉譯配置來支援高容量磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="aad0b-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="aad0b-129">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="aad0b-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="aad0b-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-131">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aad0b-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-133">限定詞： **WmiDataId** (1) </span><span class="sxs-lookup"><span data-stu-id="aad0b-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-134">包含此分割區之磁片的索引編號。</span><span class="sxs-lookup"><span data-stu-id="aad0b-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-135">**製造商**</span><span class="sxs-lookup"><span data-stu-id="aad0b-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-136">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="aad0b-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-138">限定詞： **WmiDataId** (10) ， **最大** (256) ， **格式 ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="aad0b-138">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-139">磁片磁碟機製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="aad0b-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-140">**墊**</span><span class="sxs-lookup"><span data-stu-id="aad0b-140">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-141">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="aad0b-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-143">限定詞： **WmiDataId** (13) </span><span class="sxs-lookup"><span data-stu-id="aad0b-143">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-144">未使用。</span><span class="sxs-lookup"><span data-stu-id="aad0b-144">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-145">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="aad0b-145">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aad0b-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-148">限定詞： **WmiDataId** (11) </span><span class="sxs-lookup"><span data-stu-id="aad0b-148">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-149">此實體磁片磁碟機上作業系統可辨識的磁碟分割數目。</span><span class="sxs-lookup"><span data-stu-id="aad0b-149">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-150">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="aad0b-150">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aad0b-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-153">限定詞： **WmiDataId** (9) </span><span class="sxs-lookup"><span data-stu-id="aad0b-153">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-154">Scsi 邏輯單元編號 (LUN) 的 SCSI 介面卡。</span><span class="sxs-lookup"><span data-stu-id="aad0b-154">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-155">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="aad0b-155">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-156">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aad0b-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-158">限定詞： **WmiDataId** (7) </span><span class="sxs-lookup"><span data-stu-id="aad0b-158">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-159">SCSI 介面卡的 SCSI 匯流排號碼。</span><span class="sxs-lookup"><span data-stu-id="aad0b-159">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-160">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="aad0b-160">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-161">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aad0b-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-163">限定詞： **WmiDataId** (6) </span><span class="sxs-lookup"><span data-stu-id="aad0b-163">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-164">SCSI 介面卡的 SCSI 號碼。</span><span class="sxs-lookup"><span data-stu-id="aad0b-164">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-165">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="aad0b-165">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-166">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aad0b-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-168">限定詞： **WmiDataId** (8) </span><span class="sxs-lookup"><span data-stu-id="aad0b-168">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-169">包含目標裝置的編號。</span><span class="sxs-lookup"><span data-stu-id="aad0b-169">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-170">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="aad0b-170">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-171">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aad0b-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-173">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="aad0b-173">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-174">此實體磁片磁碟機每個播放軌中的磁區數目。</span><span class="sxs-lookup"><span data-stu-id="aad0b-174">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-175">**備用**</span><span class="sxs-lookup"><span data-stu-id="aad0b-175">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-176">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="aad0b-176">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-178">限定詞： **WmiDataId** (15) 、 **Max** (2) 、 **Format ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="aad0b-178">Qualifiers: **WmiDataId** (15), **Max** (2), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-179">未使用。</span><span class="sxs-lookup"><span data-stu-id="aad0b-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-180">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="aad0b-180">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-181">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aad0b-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-183">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="aad0b-183">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-184">實體磁片磁碟機上每個圓柱的曲目數目。</span><span class="sxs-lookup"><span data-stu-id="aad0b-184">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="aad0b-185">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="aad0b-185">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="aad0b-186">如果磁片磁碟機使用轉譯配置來支援高容量磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="aad0b-186">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="aad0b-187">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="aad0b-187">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="aad0b-188">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="aad0b-188">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad0b-189">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="aad0b-189">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad0b-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad0b-191">限定詞： **WmiDataId** (12) </span><span class="sxs-lookup"><span data-stu-id="aad0b-191">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="aad0b-192">如果已啟用寫入快取，則為 True。</span><span class="sxs-lookup"><span data-stu-id="aad0b-192">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aad0b-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="aad0b-193">Requirements</span></span>



| <span data-ttu-id="aad0b-194">需求</span><span class="sxs-lookup"><span data-stu-id="aad0b-194">Requirement</span></span> | <span data-ttu-id="aad0b-195">值</span><span class="sxs-lookup"><span data-stu-id="aad0b-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aad0b-196">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aad0b-196">Minimum supported client</span></span><br/> | <span data-ttu-id="aad0b-197">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aad0b-197">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aad0b-198">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aad0b-198">Minimum supported server</span></span><br/> | <span data-ttu-id="aad0b-199">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aad0b-199">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aad0b-200">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aad0b-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad0b-201">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="aad0b-201">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




