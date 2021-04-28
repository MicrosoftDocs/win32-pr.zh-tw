---
description: SystemConfig_LogDisk 類別-此類別是邏輯磁片設定事件的事件種類類別。
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
ms.openlocfilehash: 1d7ca8dc3f632e88c250715292a27e18ff36e3af
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106106"
---
# <a name="systemconfig_logdisk-class"></a><span data-ttu-id="41666-103">SystemConfig \_ LogDisk 類別</span><span class="sxs-lookup"><span data-stu-id="41666-103">SystemConfig\_LogDisk class</span></span>

<span data-ttu-id="41666-104">此類別是邏輯磁片設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="41666-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="41666-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="41666-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="41666-106">語法</span><span class="sxs-lookup"><span data-stu-id="41666-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="41666-107">成員</span><span class="sxs-lookup"><span data-stu-id="41666-107">Members</span></span>

<span data-ttu-id="41666-108">**SystemConfig \_ LogDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="41666-108">The **SystemConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="41666-109">屬性</span><span class="sxs-lookup"><span data-stu-id="41666-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41666-110">屬性</span><span class="sxs-lookup"><span data-stu-id="41666-110">Properties</span></span>

<span data-ttu-id="41666-111">**SystemConfig \_ LogDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="41666-111">The **SystemConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41666-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="41666-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41666-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41666-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-115">限定詞： **WmiDataId** (10) </span><span class="sxs-lookup"><span data-stu-id="41666-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="41666-116">每個磁區中實體磁片磁碟機的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="41666-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="41666-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="41666-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41666-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41666-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-120">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="41666-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="41666-121">包含此分割區之磁片的索引編號。</span><span class="sxs-lookup"><span data-stu-id="41666-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="41666-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="41666-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-123">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="41666-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="41666-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-125">限定詞： **WmiDataId** (6) 、 **Max** (4) 、 **Format ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="41666-125">Qualifiers: **WmiDataId** (6), **Max** (4), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="41666-126">磁片磁碟機號，格式為 " <letter> ："。</span><span class="sxs-lookup"><span data-stu-id="41666-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="41666-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="41666-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-128">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41666-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41666-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-130">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="41666-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="41666-131">磁片磁碟機的類型。</span><span class="sxs-lookup"><span data-stu-id="41666-131">Type of disk drive.</span></span> <span data-ttu-id="41666-132">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="41666-132">Possible values are:</span></span>



| <span data-ttu-id="41666-133">值</span><span class="sxs-lookup"><span data-stu-id="41666-133">Value</span></span>                                                                        | <span data-ttu-id="41666-134">意義</span><span class="sxs-lookup"><span data-stu-id="41666-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="41666-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="41666-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="41666-136">資料分割</span><span class="sxs-lookup"><span data-stu-id="41666-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="41666-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="41666-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="41666-138">磁碟區</span><span class="sxs-lookup"><span data-stu-id="41666-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="41666-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="41666-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="41666-140">多個磁片上的延伸磁碟分割</span><span class="sxs-lookup"><span data-stu-id="41666-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="41666-141">**檔**</span><span class="sxs-lookup"><span data-stu-id="41666-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-142">資料類型： **char16**</span><span class="sxs-lookup"><span data-stu-id="41666-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="41666-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-144">限定詞： **WmiDataId** (14) 、 **Max** (16) 、 **Format ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="41666-144">Qualifiers: **WmiDataId** (14), **Max** (16), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="41666-145">邏輯磁片上的檔案系統，例如 NTFS。</span><span class="sxs-lookup"><span data-stu-id="41666-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="41666-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="41666-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-147">資料類型： **sint64**</span><span class="sxs-lookup"><span data-stu-id="41666-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="41666-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-149">限定詞： **WmiDataId** (12) </span><span class="sxs-lookup"><span data-stu-id="41666-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="41666-150">指定磁片區中的可用群集數目。</span><span class="sxs-lookup"><span data-stu-id="41666-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="41666-151">**Pad1**</span><span class="sxs-lookup"><span data-stu-id="41666-151">**Pad1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41666-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41666-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-154">限定詞： **WmiDataId** (7) </span><span class="sxs-lookup"><span data-stu-id="41666-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="41666-155">未使用。</span><span class="sxs-lookup"><span data-stu-id="41666-155">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="41666-156">**Pad2**</span><span class="sxs-lookup"><span data-stu-id="41666-156">**Pad2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41666-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41666-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-159">限定詞： **WmiDataId** (11) </span><span class="sxs-lookup"><span data-stu-id="41666-159">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="41666-160">未使用。</span><span class="sxs-lookup"><span data-stu-id="41666-160">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="41666-161">**Pad3**</span><span class="sxs-lookup"><span data-stu-id="41666-161">**Pad3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41666-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41666-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-164">限定詞： **WmiDataId** (16) </span><span class="sxs-lookup"><span data-stu-id="41666-164">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="41666-165">未使用。</span><span class="sxs-lookup"><span data-stu-id="41666-165">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="41666-166">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="41666-166">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-167">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41666-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41666-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-169">限定詞： **WmiDataId** (8) </span><span class="sxs-lookup"><span data-stu-id="41666-169">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="41666-170">資料分割的索引編號。</span><span class="sxs-lookup"><span data-stu-id="41666-170">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="41666-171">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="41666-171">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-172">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="41666-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="41666-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-174">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="41666-174">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="41666-175">分割區的總大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="41666-175">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="41666-176">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="41666-176">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-177">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41666-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41666-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-179">限定詞： **WmiDataId** (9) </span><span class="sxs-lookup"><span data-stu-id="41666-179">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="41666-180">磁片區中的磁區數目。</span><span class="sxs-lookup"><span data-stu-id="41666-180">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="41666-181">**大小**</span><span class="sxs-lookup"><span data-stu-id="41666-181">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-182">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41666-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41666-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-184">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="41666-184">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="41666-185">磁片磁碟機的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="41666-185">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="41666-186">**Startoffset 位置**</span><span class="sxs-lookup"><span data-stu-id="41666-186">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-187">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="41666-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="41666-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-189">限定詞： **WmiDataId** (1) </span><span class="sxs-lookup"><span data-stu-id="41666-189">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="41666-190">從磁片開頭開始，資料分割的位移 (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="41666-190">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="41666-191">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="41666-191">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-192">資料類型： **sint64**</span><span class="sxs-lookup"><span data-stu-id="41666-192">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="41666-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-194">限定詞： **WmiDataId** (13) </span><span class="sxs-lookup"><span data-stu-id="41666-194">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="41666-195">磁片區中已使用和可用的叢集數目。</span><span class="sxs-lookup"><span data-stu-id="41666-195">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="41666-196">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="41666-196">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41666-197">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41666-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41666-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41666-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41666-199">限定詞： **WmiDataId** (15) </span><span class="sxs-lookup"><span data-stu-id="41666-199">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="41666-200">保留的。</span><span class="sxs-lookup"><span data-stu-id="41666-200">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41666-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="41666-201">Requirements</span></span>



| <span data-ttu-id="41666-202">需求</span><span class="sxs-lookup"><span data-stu-id="41666-202">Requirement</span></span> | <span data-ttu-id="41666-203">值</span><span class="sxs-lookup"><span data-stu-id="41666-203">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="41666-204">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41666-204">Minimum supported client</span></span><br/> | <span data-ttu-id="41666-205">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41666-205">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="41666-206">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41666-206">Minimum supported server</span></span><br/> | <span data-ttu-id="41666-207">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41666-207">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41666-208">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41666-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41666-209">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="41666-209">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




