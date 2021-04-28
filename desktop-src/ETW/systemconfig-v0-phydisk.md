---
description: SystemConfig_V0_PhyDisk 類別-此類別是實體磁片設定事件的事件種類類別。
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: SystemConfig_V0_PhyDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_PhyDisk
- SystemConfig_V0_PhyDisk.DiskNumber
- SystemConfig_V0_PhyDisk.BytesPerSector
- SystemConfig_V0_PhyDisk.SectorsPerTrack
- SystemConfig_V0_PhyDisk.TracksPerCylinder
- SystemConfig_V0_PhyDisk.Cylinders
- SystemConfig_V0_PhyDisk.SCSIPort
- SystemConfig_V0_PhyDisk.SCSIPath
- SystemConfig_V0_PhyDisk.SCSITarget
- SystemConfig_V0_PhyDisk.SCSILun
- SystemConfig_V0_PhyDisk.Manufacturer
- SystemConfig_V0_PhyDisk.PartitionCount
- SystemConfig_V0_PhyDisk.WriteCacheEnabled
- SystemConfig_V0_PhyDisk.BootDriveLetter
api_type:
- NA
api_location: ''
ms.openlocfilehash: fdb12fac8b2b902f21258fd4c7cfe9846d0456eb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105956"
---
# <a name="systemconfig_v0_phydisk-class"></a><span data-ttu-id="6caec-103">SystemConfig \_ V0 \_ PhyDisk 類別</span><span class="sxs-lookup"><span data-stu-id="6caec-103">SystemConfig\_V0\_PhyDisk class</span></span>

<span data-ttu-id="6caec-104">此類別是實體磁片設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="6caec-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="6caec-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="6caec-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6caec-106">語法</span><span class="sxs-lookup"><span data-stu-id="6caec-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_V0_PhyDisk : SystemConfig_V0
{
  uint32  DiskNumber;
  uint32  BytesPerSector;
  uint32  SectorsPerTrack;
  uint32  TracksPerCylinder;
  uint64  Cylinders;
  uint32  SCSIPort;
  uint32  SCSIPath;
  uint32  SCSITarget;
  uint32  SCSILun;
  char16  Manufacturer[];
  uint32  PartitionCount;
  boolean WriteCacheEnabled;
  char16  BootDriveLetter[];
};
```

## <a name="members"></a><span data-ttu-id="6caec-107">成員</span><span class="sxs-lookup"><span data-stu-id="6caec-107">Members</span></span>

<span data-ttu-id="6caec-108">**SystemConfig \_ V0 \_ PhyDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6caec-108">The **SystemConfig\_V0\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="6caec-109">屬性</span><span class="sxs-lookup"><span data-stu-id="6caec-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6caec-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6caec-110">Properties</span></span>

<span data-ttu-id="6caec-111">**SystemConfig \_ V0 \_ PhyDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6caec-111">The **SystemConfig\_V0\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6caec-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="6caec-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-113">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="6caec-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="6caec-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-115">限定詞： **WmiDataId** (13) ， **最大** (3) </span><span class="sxs-lookup"><span data-stu-id="6caec-115">Qualifiers: **WmiDataId** (13), **Max** (3)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-116">開機磁片磁碟機的磁碟機號，格式為 " <letter> ："。</span><span class="sxs-lookup"><span data-stu-id="6caec-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="6caec-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="6caec-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6caec-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6caec-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-120">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="6caec-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-121">每個磁區中實體磁片磁碟機的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="6caec-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="6caec-122">**缸**</span><span class="sxs-lookup"><span data-stu-id="6caec-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-123">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="6caec-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6caec-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-125">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="6caec-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-126">實體磁片磁碟機上的圓柱總數。</span><span class="sxs-lookup"><span data-stu-id="6caec-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="6caec-127">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="6caec-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="6caec-128">如果磁片磁碟機使用轉譯配置來支援高容量磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="6caec-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="6caec-129">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="6caec-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="6caec-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="6caec-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-131">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6caec-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6caec-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-133">限定詞： **WmiDataId** (1) </span><span class="sxs-lookup"><span data-stu-id="6caec-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-134">包含此分割區之磁片的索引編號。</span><span class="sxs-lookup"><span data-stu-id="6caec-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="6caec-135">**製造商**</span><span class="sxs-lookup"><span data-stu-id="6caec-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-136">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="6caec-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="6caec-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-138">限定詞： **WmiDataId** (10) ， **最大** (256) </span><span class="sxs-lookup"><span data-stu-id="6caec-138">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-139">磁片磁碟機製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="6caec-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="6caec-140">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="6caec-140">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-141">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6caec-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6caec-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-143">限定詞： **WmiDataId** (11) </span><span class="sxs-lookup"><span data-stu-id="6caec-143">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-144">此實體磁片磁碟機上作業系統可辨識的磁碟分割數目。</span><span class="sxs-lookup"><span data-stu-id="6caec-144">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="6caec-145">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="6caec-145">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6caec-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6caec-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-148">限定詞： **WmiDataId** (9) </span><span class="sxs-lookup"><span data-stu-id="6caec-148">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-149">Scsi 邏輯單元編號 (LUN) 的 SCSI 介面卡。</span><span class="sxs-lookup"><span data-stu-id="6caec-149">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6caec-150">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="6caec-150">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6caec-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6caec-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-153">限定詞： **WmiDataId** (7) </span><span class="sxs-lookup"><span data-stu-id="6caec-153">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-154">SCSI 介面卡的 SCSI 匯流排號碼。</span><span class="sxs-lookup"><span data-stu-id="6caec-154">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6caec-155">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="6caec-155">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-156">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6caec-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6caec-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-158">限定詞： **WmiDataId** (6) </span><span class="sxs-lookup"><span data-stu-id="6caec-158">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-159">SCSI 介面卡的 SCSI 號碼。</span><span class="sxs-lookup"><span data-stu-id="6caec-159">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6caec-160">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="6caec-160">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-161">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6caec-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6caec-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-163">限定詞： **WmiDataId** (8) </span><span class="sxs-lookup"><span data-stu-id="6caec-163">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-164">包含目標裝置的編號。</span><span class="sxs-lookup"><span data-stu-id="6caec-164">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="6caec-165">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="6caec-165">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-166">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6caec-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6caec-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-168">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="6caec-168">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-169">此實體磁片磁碟機每個播放軌中的磁區數目。</span><span class="sxs-lookup"><span data-stu-id="6caec-169">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="6caec-170">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="6caec-170">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-171">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6caec-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6caec-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-173">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="6caec-173">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-174">實體磁片磁碟機上每個圓柱的曲目數目。</span><span class="sxs-lookup"><span data-stu-id="6caec-174">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="6caec-175">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="6caec-175">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="6caec-176">如果磁片磁碟機使用轉譯配置來支援高容量磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="6caec-176">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="6caec-177">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="6caec-177">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="6caec-178">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="6caec-178">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6caec-179">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6caec-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6caec-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6caec-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6caec-181">限定詞： **WmiDataId** (12) </span><span class="sxs-lookup"><span data-stu-id="6caec-181">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="6caec-182">如果已啟用寫入快取，則為 True。</span><span class="sxs-lookup"><span data-stu-id="6caec-182">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6caec-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="6caec-183">Requirements</span></span>



| <span data-ttu-id="6caec-184">需求</span><span class="sxs-lookup"><span data-stu-id="6caec-184">Requirement</span></span> | <span data-ttu-id="6caec-185">值</span><span class="sxs-lookup"><span data-stu-id="6caec-185">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6caec-186">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6caec-186">Minimum supported client</span></span><br/> | <span data-ttu-id="6caec-187">都不支援</span><span class="sxs-lookup"><span data-stu-id="6caec-187">None supported</span></span><br/>                            |
| <span data-ttu-id="6caec-188">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6caec-188">Minimum supported server</span></span><br/> | <span data-ttu-id="6caec-189">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6caec-189">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6caec-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6caec-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6caec-191">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="6caec-191">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




