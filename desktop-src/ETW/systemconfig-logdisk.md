---
description: 此類別是邏輯磁片設定事件的事件種類類別。
ms.assetid: a11a8245-8ace-4061-b6c7-938002d8b9fc
title: SystemConfig_LogDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_LogDisk
- SystemConfig_LogDisk.StartOffset
- SystemConfig_LogDisk.PartitionSize
- SystemConfig_LogDisk.DiskNumber
- SystemConfig_LogDisk.Size
- SystemConfig_LogDisk.DriveType
- SystemConfig_LogDisk.DriveLetterString
- SystemConfig_LogDisk.Pad1
- SystemConfig_LogDisk.PartitionNumber
- SystemConfig_LogDisk.SectorsPerCluster
- SystemConfig_LogDisk.BytesPerSector
- SystemConfig_LogDisk.Pad2
- SystemConfig_LogDisk.NumberOfFreeClusters
- SystemConfig_LogDisk.TotalNumberOfClusters
- SystemConfig_LogDisk.FileSystem
- SystemConfig_LogDisk.VolumeExt
- SystemConfig_LogDisk.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3bff1cf526dfb7bf1ddd36fcb887e8a4b837be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972165"
---
# <a name="systemconfig_logdisk-class"></a><span data-ttu-id="ef109-103">SystemConfig \_ LogDisk 類別</span><span class="sxs-lookup"><span data-stu-id="ef109-103">SystemConfig\_LogDisk class</span></span>

<span data-ttu-id="ef109-104">此類別是邏輯磁片設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="ef109-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="ef109-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="ef109-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef109-106">語法</span><span class="sxs-lookup"><span data-stu-id="ef109-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_LogDisk : SystemConfig
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad1;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  uint32 Pad2;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
  uint32 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="ef109-107">成員</span><span class="sxs-lookup"><span data-stu-id="ef109-107">Members</span></span>

<span data-ttu-id="ef109-108">**SystemConfig \_ LogDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ef109-108">The **SystemConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="ef109-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ef109-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef109-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ef109-110">Properties</span></span>

<span data-ttu-id="ef109-111">**SystemConfig \_ LogDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ef109-111">The **SystemConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef109-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="ef109-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef109-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-115">限定詞： **WmiDataId** (10) </span><span class="sxs-lookup"><span data-stu-id="ef109-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-116">每個磁區中實體磁片磁碟機的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ef109-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="ef109-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef109-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-120">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="ef109-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-121">包含此分割區之磁片的索引編號。</span><span class="sxs-lookup"><span data-stu-id="ef109-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="ef109-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-123">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ef109-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="ef109-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-125">限定詞： **WmiDataId** (6) 、 **Max** (4) 、 **Format ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="ef109-125">Qualifiers: **WmiDataId** (6), **Max** (4), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="ef109-126">磁片磁碟機號，格式為 " <letter> ："。</span><span class="sxs-lookup"><span data-stu-id="ef109-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="ef109-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="ef109-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-128">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef109-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-130">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="ef109-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-131">磁片磁碟機的類型。</span><span class="sxs-lookup"><span data-stu-id="ef109-131">Type of disk drive.</span></span> <span data-ttu-id="ef109-132">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="ef109-132">Possible values are:</span></span>



| <span data-ttu-id="ef109-133">值</span><span class="sxs-lookup"><span data-stu-id="ef109-133">Value</span></span>                                                                        | <span data-ttu-id="ef109-134">意義</span><span class="sxs-lookup"><span data-stu-id="ef109-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="ef109-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ef109-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="ef109-136">資料分割</span><span class="sxs-lookup"><span data-stu-id="ef109-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="ef109-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ef109-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="ef109-138">磁碟區</span><span class="sxs-lookup"><span data-stu-id="ef109-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="ef109-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ef109-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="ef109-140">多個磁片上的延伸磁碟分割</span><span class="sxs-lookup"><span data-stu-id="ef109-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ef109-141">**檔**</span><span class="sxs-lookup"><span data-stu-id="ef109-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-142">資料類型： **char16**</span><span class="sxs-lookup"><span data-stu-id="ef109-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-144">限定詞： **WmiDataId** (14) 、 **Max** (16) 、 **Format ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="ef109-144">Qualifiers: **WmiDataId** (14), **Max** (16), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="ef109-145">邏輯磁片上的檔案系統，例如 NTFS。</span><span class="sxs-lookup"><span data-stu-id="ef109-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="ef109-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-147">資料類型： **sint64**</span><span class="sxs-lookup"><span data-stu-id="ef109-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-149">限定詞： **WmiDataId** (12) </span><span class="sxs-lookup"><span data-stu-id="ef109-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-150">指定磁片區中的可用群集數目。</span><span class="sxs-lookup"><span data-stu-id="ef109-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-151">**Pad1**</span><span class="sxs-lookup"><span data-stu-id="ef109-151">**Pad1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef109-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-154">限定詞： **WmiDataId** (7) </span><span class="sxs-lookup"><span data-stu-id="ef109-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-155">未使用。</span><span class="sxs-lookup"><span data-stu-id="ef109-155">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-156">**Pad2**</span><span class="sxs-lookup"><span data-stu-id="ef109-156">**Pad2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef109-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-159">限定詞： **WmiDataId** (11) </span><span class="sxs-lookup"><span data-stu-id="ef109-159">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-160">未使用。</span><span class="sxs-lookup"><span data-stu-id="ef109-160">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-161">**Pad3**</span><span class="sxs-lookup"><span data-stu-id="ef109-161">**Pad3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef109-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-164">限定詞： **WmiDataId** (16) </span><span class="sxs-lookup"><span data-stu-id="ef109-164">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-165">未使用。</span><span class="sxs-lookup"><span data-stu-id="ef109-165">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-166">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="ef109-166">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-167">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef109-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-169">限定詞： **WmiDataId** (8) </span><span class="sxs-lookup"><span data-stu-id="ef109-169">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-170">資料分割的索引編號。</span><span class="sxs-lookup"><span data-stu-id="ef109-170">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-171">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="ef109-171">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-172">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ef109-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-174">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="ef109-174">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-175">分割區的總大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef109-175">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-176">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="ef109-176">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-177">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef109-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-179">限定詞： **WmiDataId** (9) </span><span class="sxs-lookup"><span data-stu-id="ef109-179">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-180">磁片區中的磁區數目。</span><span class="sxs-lookup"><span data-stu-id="ef109-180">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-181">**大小**</span><span class="sxs-lookup"><span data-stu-id="ef109-181">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-182">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef109-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-184">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="ef109-184">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-185">磁片磁碟機的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef109-185">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-186">**Startoffset 位置**</span><span class="sxs-lookup"><span data-stu-id="ef109-186">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-187">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ef109-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-189">限定詞： **WmiDataId** (1) </span><span class="sxs-lookup"><span data-stu-id="ef109-189">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-190">從磁片開頭開始，資料分割的位移 (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="ef109-190">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-191">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="ef109-191">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-192">資料類型： **sint64**</span><span class="sxs-lookup"><span data-stu-id="ef109-192">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-194">限定詞： **WmiDataId** (13) </span><span class="sxs-lookup"><span data-stu-id="ef109-194">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-195">磁片區中已使用和可用的叢集數目。</span><span class="sxs-lookup"><span data-stu-id="ef109-195">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="ef109-196">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="ef109-196">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef109-197">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef109-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef109-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef109-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef109-199">限定詞： **WmiDataId** (15) </span><span class="sxs-lookup"><span data-stu-id="ef109-199">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="ef109-200">保留的。</span><span class="sxs-lookup"><span data-stu-id="ef109-200">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef109-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef109-201">Requirements</span></span>



| <span data-ttu-id="ef109-202">需求</span><span class="sxs-lookup"><span data-stu-id="ef109-202">Requirement</span></span> | <span data-ttu-id="ef109-203">值</span><span class="sxs-lookup"><span data-stu-id="ef109-203">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ef109-204">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef109-204">Minimum supported client</span></span><br/> | <span data-ttu-id="ef109-205">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef109-205">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ef109-206">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef109-206">Minimum supported server</span></span><br/> | <span data-ttu-id="ef109-207">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef109-207">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef109-208">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef109-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef109-209">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="ef109-209">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




