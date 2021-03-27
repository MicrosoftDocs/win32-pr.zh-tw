---
description: HWConfig \_ PhyDisk 類別是實體磁片設定事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: HWConfig_PhyDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: 453f06ae11bb8b1e11c9efddd6f63bffd38540e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972200"
---
# <a name="hwconfig_phydisk-class"></a><span data-ttu-id="25284-104">HWConfig \_ PhyDisk 類別</span><span class="sxs-lookup"><span data-stu-id="25284-104">HWConfig\_PhyDisk class</span></span>

<span data-ttu-id="25284-105">**HWConfig \_ PhyDisk** 類別是實體磁片設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="25284-105">The **HWConfig\_PhyDisk** class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="25284-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="25284-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="25284-107">語法</span><span class="sxs-lookup"><span data-stu-id="25284-107">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
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
  string Manufacturer;
};
```

## <a name="members"></a><span data-ttu-id="25284-108">成員</span><span class="sxs-lookup"><span data-stu-id="25284-108">Members</span></span>

<span data-ttu-id="25284-109">**HWConfig \_ PhyDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="25284-109">The **HWConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="25284-110">屬性</span><span class="sxs-lookup"><span data-stu-id="25284-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25284-111">屬性</span><span class="sxs-lookup"><span data-stu-id="25284-111">Properties</span></span>

<span data-ttu-id="25284-112">**HWConfig \_ PhyDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="25284-112">The **HWConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25284-113">BytesPerSector</span><span class="sxs-lookup"><span data-stu-id="25284-113">BytesPerSector</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25284-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="25284-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25284-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25284-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25284-116">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="25284-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="25284-117">每個磁區中實體磁片磁碟機的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="25284-117">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="25284-118">缸</span><span class="sxs-lookup"><span data-stu-id="25284-118">Cylinders</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25284-119">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="25284-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="25284-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25284-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25284-121">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="25284-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="25284-122">實體磁片磁碟機上的圓柱總數。</span><span class="sxs-lookup"><span data-stu-id="25284-122">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="25284-123">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="25284-123">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="25284-124">如果磁片磁碟機使用轉譯配置來支援高容量磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="25284-124">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="25284-125">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="25284-125">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="25284-126">DiskNumber</span><span class="sxs-lookup"><span data-stu-id="25284-126">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25284-127">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="25284-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25284-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25284-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25284-129">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="25284-129">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="25284-130">包含此分割區之磁片的索引編號。</span><span class="sxs-lookup"><span data-stu-id="25284-130">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="25284-131">製造商</span><span class="sxs-lookup"><span data-stu-id="25284-131">Manufacturer</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25284-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="25284-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25284-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25284-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25284-134">限定詞： WmiDataId (10) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="25284-134">Qualifiers: WmiDataId(10), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="25284-135">磁片磁碟機製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="25284-135">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="25284-136">SCSILun</span><span class="sxs-lookup"><span data-stu-id="25284-136">SCSILun</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25284-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="25284-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25284-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25284-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25284-139">限定詞： WmiDataId (9) </span><span class="sxs-lookup"><span data-stu-id="25284-139">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="25284-140">Scsi 邏輯單元編號 (LUN) 的 SCSI 介面卡。</span><span class="sxs-lookup"><span data-stu-id="25284-140">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="25284-141">SCSIPath</span><span class="sxs-lookup"><span data-stu-id="25284-141">SCSIPath</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25284-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="25284-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25284-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25284-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25284-144">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="25284-144">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="25284-145">SCSI 介面卡的 SCSI 匯流排號碼。</span><span class="sxs-lookup"><span data-stu-id="25284-145">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="25284-146">SCSIPort</span><span class="sxs-lookup"><span data-stu-id="25284-146">SCSIPort</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25284-147">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="25284-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25284-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25284-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25284-149">限定詞： WmiDataId (6) </span><span class="sxs-lookup"><span data-stu-id="25284-149">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="25284-150">SCSI 介面卡的 SCSI 號碼。</span><span class="sxs-lookup"><span data-stu-id="25284-150">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="25284-151">SCSITarget</span><span class="sxs-lookup"><span data-stu-id="25284-151">SCSITarget</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25284-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="25284-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25284-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25284-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25284-154">限定詞： WmiDataId (8) </span><span class="sxs-lookup"><span data-stu-id="25284-154">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="25284-155">包含目標裝置的編號。</span><span class="sxs-lookup"><span data-stu-id="25284-155">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="25284-156">SectorsPerTrack</span><span class="sxs-lookup"><span data-stu-id="25284-156">SectorsPerTrack</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25284-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="25284-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25284-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25284-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25284-159">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="25284-159">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="25284-160">此實體磁片磁碟機每個播放軌中的磁區數目。</span><span class="sxs-lookup"><span data-stu-id="25284-160">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="25284-161">TracksPerCylinder</span><span class="sxs-lookup"><span data-stu-id="25284-161">TracksPerCylinder</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25284-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="25284-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25284-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25284-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25284-164">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="25284-164">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="25284-165">實體磁片磁碟機上每個圓柱的曲目數目。</span><span class="sxs-lookup"><span data-stu-id="25284-165">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="25284-166">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="25284-166">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="25284-167">如果磁片磁碟機使用轉譯配置來支援高容量磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="25284-167">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="25284-168">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="25284-168">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25284-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="25284-169">Requirements</span></span>



| <span data-ttu-id="25284-170">需求</span><span class="sxs-lookup"><span data-stu-id="25284-170">Requirement</span></span> | <span data-ttu-id="25284-171">值</span><span class="sxs-lookup"><span data-stu-id="25284-171">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="25284-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25284-172">Minimum supported client</span></span><br/> | <span data-ttu-id="25284-173">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25284-173">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="25284-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25284-174">Minimum supported server</span></span><br/> | <span data-ttu-id="25284-175">都不支援</span><span class="sxs-lookup"><span data-stu-id="25284-175">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="25284-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25284-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25284-177">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="25284-177">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




