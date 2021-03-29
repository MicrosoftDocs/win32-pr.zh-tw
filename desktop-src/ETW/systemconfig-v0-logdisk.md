---
description: 此類別是邏輯磁片設定事件的事件種類類別。
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: SystemConfig_V0_LogDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: dbc1ee189bae1fe71f42267f38bd40763764dea2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973645"
---
# <a name="systemconfig_v0_logdisk-class"></a><span data-ttu-id="a7593-103">SystemConfig \_ V0 \_ LogDisk 類別</span><span class="sxs-lookup"><span data-stu-id="a7593-103">SystemConfig\_V0\_LogDisk class</span></span>

<span data-ttu-id="a7593-104">此類別是邏輯磁片設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="a7593-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="a7593-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="a7593-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7593-106">語法</span><span class="sxs-lookup"><span data-stu-id="a7593-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a><span data-ttu-id="a7593-107">成員</span><span class="sxs-lookup"><span data-stu-id="a7593-107">Members</span></span>

<span data-ttu-id="a7593-108">**SystemConfig \_ V0 \_ LogDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a7593-108">The **SystemConfig\_V0\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="a7593-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a7593-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7593-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a7593-110">Properties</span></span>

<span data-ttu-id="a7593-111">**SystemConfig \_ V0 \_ LogDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a7593-111">The **SystemConfig\_V0\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7593-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="a7593-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a7593-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-115">限定詞： **WmiDataId** (10) </span><span class="sxs-lookup"><span data-stu-id="a7593-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-116">每個磁區中實體磁片磁碟機的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="a7593-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="a7593-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="a7593-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a7593-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-120">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="a7593-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-121">包含此分割區之磁片的索引編號。</span><span class="sxs-lookup"><span data-stu-id="a7593-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="a7593-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="a7593-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-123">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a7593-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="a7593-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-125">限定詞： **WmiDataId** (6) ， **最大** (4) </span><span class="sxs-lookup"><span data-stu-id="a7593-125">Qualifiers: **WmiDataId** (6), **Max** (4)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-126">磁片磁碟機號，格式為 " <letter> ："。</span><span class="sxs-lookup"><span data-stu-id="a7593-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="a7593-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="a7593-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-128">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a7593-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-130">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="a7593-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-131">磁片磁碟機的類型。</span><span class="sxs-lookup"><span data-stu-id="a7593-131">Type of disk drive.</span></span> <span data-ttu-id="a7593-132">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="a7593-132">Possible values are:</span></span>



| <span data-ttu-id="a7593-133">值</span><span class="sxs-lookup"><span data-stu-id="a7593-133">Value</span></span>                                                                        | <span data-ttu-id="a7593-134">意義</span><span class="sxs-lookup"><span data-stu-id="a7593-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="a7593-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a7593-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a7593-136">資料分割</span><span class="sxs-lookup"><span data-stu-id="a7593-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="a7593-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a7593-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a7593-138">磁碟區</span><span class="sxs-lookup"><span data-stu-id="a7593-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="a7593-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a7593-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="a7593-140">多個磁片上的延伸磁碟分割</span><span class="sxs-lookup"><span data-stu-id="a7593-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a7593-141">**檔**</span><span class="sxs-lookup"><span data-stu-id="a7593-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-142">資料類型： **char16**</span><span class="sxs-lookup"><span data-stu-id="a7593-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-144">限定詞： **WmiDataId** (13) ， **最大** (16) </span><span class="sxs-lookup"><span data-stu-id="a7593-144">Qualifiers: **WmiDataId** (13), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-145">邏輯磁片上的檔案系統，例如 NTFS。</span><span class="sxs-lookup"><span data-stu-id="a7593-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="a7593-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="a7593-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-147">資料類型： **sint64**</span><span class="sxs-lookup"><span data-stu-id="a7593-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-149">限定詞： **WmiDataId** (11) </span><span class="sxs-lookup"><span data-stu-id="a7593-149">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-150">指定磁片區中的可用群集數目。</span><span class="sxs-lookup"><span data-stu-id="a7593-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="a7593-151">**墊**</span><span class="sxs-lookup"><span data-stu-id="a7593-151">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a7593-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-154">限定詞： **WmiDataId** (7) </span><span class="sxs-lookup"><span data-stu-id="a7593-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-155">保留的。</span><span class="sxs-lookup"><span data-stu-id="a7593-155">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a7593-156">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="a7593-156">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a7593-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-159">限定詞： **WmiDataId** (8) </span><span class="sxs-lookup"><span data-stu-id="a7593-159">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-160">資料分割的索引編號。</span><span class="sxs-lookup"><span data-stu-id="a7593-160">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="a7593-161">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="a7593-161">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-162">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a7593-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-164">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="a7593-164">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-165">分割區的總大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a7593-165">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a7593-166">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="a7593-166">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-167">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a7593-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-169">限定詞： **WmiDataId** (9) </span><span class="sxs-lookup"><span data-stu-id="a7593-169">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-170">磁片區中的磁區數目。</span><span class="sxs-lookup"><span data-stu-id="a7593-170">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="a7593-171">**大小**</span><span class="sxs-lookup"><span data-stu-id="a7593-171">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-172">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a7593-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-174">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="a7593-174">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-175">磁片磁碟機的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a7593-175">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a7593-176">**Startoffset 位置**</span><span class="sxs-lookup"><span data-stu-id="a7593-176">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-177">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a7593-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-179">限定詞： **WmiDataId** (1) </span><span class="sxs-lookup"><span data-stu-id="a7593-179">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-180">從磁片開頭開始，資料分割的位移 (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="a7593-180">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="a7593-181">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="a7593-181">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-182">資料類型： **sint64**</span><span class="sxs-lookup"><span data-stu-id="a7593-182">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-184">限定詞： **WmiDataId** (12) </span><span class="sxs-lookup"><span data-stu-id="a7593-184">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-185">磁片區中已使用和可用的叢集數目。</span><span class="sxs-lookup"><span data-stu-id="a7593-185">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="a7593-186">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="a7593-186">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7593-187">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a7593-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7593-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7593-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7593-189">限定詞： **WmiDataId** (14) </span><span class="sxs-lookup"><span data-stu-id="a7593-189">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="a7593-190">保留的。</span><span class="sxs-lookup"><span data-stu-id="a7593-190">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7593-191">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7593-191">Requirements</span></span>



| <span data-ttu-id="a7593-192">需求</span><span class="sxs-lookup"><span data-stu-id="a7593-192">Requirement</span></span> | <span data-ttu-id="a7593-193">值</span><span class="sxs-lookup"><span data-stu-id="a7593-193">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a7593-194">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7593-194">Minimum supported client</span></span><br/> | <span data-ttu-id="a7593-195">都不支援</span><span class="sxs-lookup"><span data-stu-id="a7593-195">None supported</span></span><br/>                            |
| <span data-ttu-id="a7593-196">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7593-196">Minimum supported server</span></span><br/> | <span data-ttu-id="a7593-197">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7593-197">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7593-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7593-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7593-199">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="a7593-199">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




