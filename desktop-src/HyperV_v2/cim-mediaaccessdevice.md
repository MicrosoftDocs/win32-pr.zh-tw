---
description: 代表可以使用媒體來儲存和取出資料的裝置。
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: 'CIM_MediaAccessDevice 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 616148f6749f3ec00d019a903e8f9046d3aba602
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986435"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a><span data-ttu-id="86c5f-103">CIM_MediaAccessDevice 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="86c5f-103">CIM_MediaAccessDevice class (Hyper-V management)</span></span>

<span data-ttu-id="86c5f-104">代表可以使用媒體來儲存和取出資料的裝置。</span><span class="sxs-lookup"><span data-stu-id="86c5f-104">Represents a device that can use media to store and retrieve data.</span></span>

## <a name="syntax"></a><span data-ttu-id="86c5f-105">語法</span><span class="sxs-lookup"><span data-stu-id="86c5f-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a><span data-ttu-id="86c5f-106">成員</span><span class="sxs-lookup"><span data-stu-id="86c5f-106">Members</span></span>

<span data-ttu-id="86c5f-107">**CIM \_ MediaAccessDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="86c5f-107">The **CIM\_MediaAccessDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="86c5f-108">方法</span><span class="sxs-lookup"><span data-stu-id="86c5f-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="86c5f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="86c5f-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="86c5f-110">方法</span><span class="sxs-lookup"><span data-stu-id="86c5f-110">Methods</span></span>

<span data-ttu-id="86c5f-111">**CIM \_ MediaAccessDevice** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="86c5f-111">The **CIM\_MediaAccessDevice** class has these methods.</span></span>



| <span data-ttu-id="86c5f-112">方法</span><span class="sxs-lookup"><span data-stu-id="86c5f-112">Method</span></span>                                               | <span data-ttu-id="86c5f-113">描述</span><span class="sxs-lookup"><span data-stu-id="86c5f-113">Description</span></span>                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="86c5f-114">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="86c5f-114">**LockMedia**</span></span>](cim-mediaaccessdevice-lockmedia.md) | <span data-ttu-id="86c5f-115">鎖定和解除鎖定媒體存取裝置中的卸載式媒體。</span><span class="sxs-lookup"><span data-stu-id="86c5f-115">Locks and unlocks removable media in a media access device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="86c5f-116">屬性</span><span class="sxs-lookup"><span data-stu-id="86c5f-116">Properties</span></span>

<span data-ttu-id="86c5f-117">**CIM \_ MediaAccessDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="86c5f-117">The **CIM\_MediaAccessDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="86c5f-118">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="86c5f-118">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-119">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="86c5f-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-121">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 儲存裝置 \| 001.9 "，" MIF。DMTF \| 儲存裝置 \| 001.11 "，" MIF。DMTF \| 儲存裝置 \| 001.12 "，" MIF。DMTF \| 磁片 \| 003.7 "，" MIF。DMTF \| 主機磁片 \| 001.2 "，" MIF。DMTF \| 主機磁片 \| 001.4 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="86c5f-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7", "MIF.DMTF\|Host Disk\|001.2", "MIF.DMTF\|Host Disk\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-122">陣列，其中包含媒體存取裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="86c5f-122">An array that contains the capabilities of the media access device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="86c5f-123">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="86c5f-123">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="86c5f-124">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="86c5f-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="86c5f-125">**順序存取** (2) </span><span class="sxs-lookup"><span data-stu-id="86c5f-125">**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="86c5f-126">**隨機存取** (3) </span><span class="sxs-lookup"><span data-stu-id="86c5f-126">**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="86c5f-127">**支援寫入** (4) </span><span class="sxs-lookup"><span data-stu-id="86c5f-127">**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="86c5f-128">**加密** (5) </span><span class="sxs-lookup"><span data-stu-id="86c5f-128">**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="86c5f-129">**壓縮** (6) </span><span class="sxs-lookup"><span data-stu-id="86c5f-129">**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="86c5f-130">**支援卸除式媒體** (7) </span><span class="sxs-lookup"><span data-stu-id="86c5f-130">**Supports Removeable Media** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="86c5f-131">**手動清除** (8) </span><span class="sxs-lookup"><span data-stu-id="86c5f-131">**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="86c5f-132">**自動清除** (9) </span><span class="sxs-lookup"><span data-stu-id="86c5f-132">**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="86c5f-133">**智慧型通知** (10) </span><span class="sxs-lookup"><span data-stu-id="86c5f-133">**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="86c5f-134">**支援雙側媒體** (11) </span><span class="sxs-lookup"><span data-stu-id="86c5f-134">**Supports Dual Sided Media** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="86c5f-135">**不需要 Predismount 退出** (12) </span><span class="sxs-lookup"><span data-stu-id="86c5f-135">**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="86c5f-136">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="86c5f-136">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-137">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="86c5f-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-139">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ MediaAccessDevice**。**功能**") </span><span class="sxs-lookup"><span data-stu-id="86c5f-139">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-140">**功能** 陣列中專案的功能描述陣列。</span><span class="sxs-lookup"><span data-stu-id="86c5f-140">An array of feature descriptions for the items in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-141">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="86c5f-141">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86c5f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-144">裝置用來支援壓縮的演算法或工具的名稱。</span><span class="sxs-lookup"><span data-stu-id="86c5f-144">The name of the algorithm or tool used by the device to support compression.</span></span>

<span data-ttu-id="86c5f-145">如果未指定壓縮類型，則可以使用下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="86c5f-145">If a compression type is not specified, one of the following values can be used:</span></span>

-   <span data-ttu-id="86c5f-146">「未知」壓縮支援不明或未指定。</span><span class="sxs-lookup"><span data-stu-id="86c5f-146">"Unknown"   compression support is unknown or not specified.</span></span>
-   <span data-ttu-id="86c5f-147">支援「壓縮」壓縮，但類型未知或未指定。</span><span class="sxs-lookup"><span data-stu-id="86c5f-147">"Compressed"   compression is supported but the type is unknown or unspecified.</span></span>
-   <span data-ttu-id="86c5f-148">「未壓縮」裝置不支援壓縮功能。</span><span class="sxs-lookup"><span data-stu-id="86c5f-148">"Not Compressed"   the device does not support compression capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-149">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="86c5f-149">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-150">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="86c5f-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-152">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) </span><span class="sxs-lookup"><span data-stu-id="86c5f-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-153">裝置的預設區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="86c5f-153">The default block size, in bytes, for the device.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-154">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="86c5f-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86c5f-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-157">裝置支援的錯誤偵測類型和修正。</span><span class="sxs-lookup"><span data-stu-id="86c5f-157">The type of error detection and correction supported by the device.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-158">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="86c5f-158">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-159">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="86c5f-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-161">上次清除裝置的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="86c5f-161">The date and time when the device was last cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-162">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="86c5f-162">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-163">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="86c5f-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-165">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) ， **PUnit** ( "第 \* 10 ^-3" ) </span><span class="sxs-lookup"><span data-stu-id="86c5f-165">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-166">裝置在裝置開始載入後，能夠讀取或寫入媒體所花費的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="86c5f-166">The time it takes, in milliseconds, for the device to be able to read or write a media after the device starts loading.</span></span> <span data-ttu-id="86c5f-167">例如，對於磁片磁碟機而言，這是磁片未切換至磁片的間隔，可供讀取/寫入作業。</span><span class="sxs-lookup"><span data-stu-id="86c5f-167">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write operations.</span></span> <span data-ttu-id="86c5f-168">針對磁帶機，這會在插入媒體時啟動，並在磁片磁碟機回報應用程式準備好時結束。</span><span class="sxs-lookup"><span data-stu-id="86c5f-168">For tape drives, this starts when media is inserted and ends when the drive reports that it is ready for an application.</span></span> <span data-ttu-id="86c5f-169">這通常是磁帶的磁帶 (BOT) 區域。</span><span class="sxs-lookup"><span data-stu-id="86c5f-169">This is usually at the tape's beginning-of-tape (BOT) area.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-170">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="86c5f-170">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-171">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="86c5f-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-173">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) ， **PUnit** ( "第 \* 10 ^-3" ) </span><span class="sxs-lookup"><span data-stu-id="86c5f-173">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-174">媒體的最大存取時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="86c5f-174">The maximum access time of the media, in milliseconds.</span></span> <span data-ttu-id="86c5f-175">若是磁片磁碟機，這代表完整的搜尋和完整的旋轉延遲。</span><span class="sxs-lookup"><span data-stu-id="86c5f-175">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="86c5f-176">針對磁帶機，這代表從磁帶開頭到最遠距離點的搜尋。</span><span class="sxs-lookup"><span data-stu-id="86c5f-176">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-177">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="86c5f-177">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-178">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="86c5f-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-180">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) </span><span class="sxs-lookup"><span data-stu-id="86c5f-180">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-181">裝置所存取媒體的最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="86c5f-181">The maximum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-182">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="86c5f-182">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-183">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="86c5f-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-185">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 順序存取裝置 \| 001.2 "，" MIF。DMTF \| 主機磁片 \| 001.5」 ) </span><span class="sxs-lookup"><span data-stu-id="86c5f-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2", "MIF.DMTF\|Host Disk\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-186">此裝置支援的媒體大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="86c5f-186">The maximum size, in kilobytes, of media supported by this device.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-187">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="86c5f-187">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-188">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="86c5f-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-190">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ MediaAccessDevice**.**UnitsDescription**") </span><span class="sxs-lookup"><span data-stu-id="86c5f-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-191">可以在裝置清理之前使用的單位數目上限。</span><span class="sxs-lookup"><span data-stu-id="86c5f-191">The maximum number of units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="86c5f-192">**UnitsDescription** 會定義單位類型。</span><span class="sxs-lookup"><span data-stu-id="86c5f-192">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-193">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="86c5f-193">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-194">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="86c5f-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-196">如果媒體在裝置中鎖定且無法取出則為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="86c5f-196">**true** if the media is locked in the device and can not be ejected; otherwise, **false**.</span></span> <span data-ttu-id="86c5f-197">若為非卸載式裝置，此值應為 **true**。</span><span class="sxs-lookup"><span data-stu-id="86c5f-197">For non-removable devices, this value should be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-198">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="86c5f-198">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-199">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="86c5f-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-201">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) </span><span class="sxs-lookup"><span data-stu-id="86c5f-201">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-202">裝置所存取媒體的最社區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="86c5f-202">The minimum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-203">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="86c5f-203">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-204">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="86c5f-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-206">限定詞： **計數器**</span><span class="sxs-lookup"><span data-stu-id="86c5f-206">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-207">裝載媒體以進行資料傳輸或清除裝置的次數。</span><span class="sxs-lookup"><span data-stu-id="86c5f-207">The number of times that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="86c5f-208">如果裝置不支援卸載式媒體，則應該將此屬性設定為零。</span><span class="sxs-lookup"><span data-stu-id="86c5f-208">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-209">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="86c5f-209">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-210">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="86c5f-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-212">如果裝置需要清除，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="86c5f-212">**true** if the device needs cleaning; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="86c5f-213">[ **功能** ] 屬性會指出是否可以手動或自動清除。</span><span class="sxs-lookup"><span data-stu-id="86c5f-213">The **Capabilities** property indicates whether manual or automatic cleaning is possible.</span></span>

 

</dd> <dt>

<span data-ttu-id="86c5f-214">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="86c5f-214">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-215">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86c5f-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-217">如果裝置支援多個個別媒體，則這個屬性會定義可支援或插入的最大數目。</span><span class="sxs-lookup"><span data-stu-id="86c5f-217">If the device supports multiple individual media, this property defines the maximum number which can be supported or inserted.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-218">**安全性**</span><span class="sxs-lookup"><span data-stu-id="86c5f-218">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-219">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="86c5f-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-221">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 磁片 \| 003.22 ") </span><span class="sxs-lookup"><span data-stu-id="86c5f-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Disks\|003.22")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-222">裝置的營運安全性。</span><span class="sxs-lookup"><span data-stu-id="86c5f-222">The operational security for the device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="86c5f-223">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="86c5f-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="86c5f-224">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="86c5f-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="86c5f-225">**無** (3) </span><span class="sxs-lookup"><span data-stu-id="86c5f-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

<span data-ttu-id="86c5f-226">**唯讀** (4) </span><span class="sxs-lookup"><span data-stu-id="86c5f-226">**Read Only** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

<span data-ttu-id="86c5f-227">**鎖定** (5) </span><span class="sxs-lookup"><span data-stu-id="86c5f-227">**Locked Out** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="86c5f-228">**開機略過** (6) </span><span class="sxs-lookup"><span data-stu-id="86c5f-228">**Boot Bypass** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

<span data-ttu-id="86c5f-229">**開機略過和唯讀** (7) </span><span class="sxs-lookup"><span data-stu-id="86c5f-229">**Boot Bypass and Read Only** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="86c5f-230">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="86c5f-230">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-231">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="86c5f-231">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-233">在裝置上掛接媒體的最新日期和時間。</span><span class="sxs-lookup"><span data-stu-id="86c5f-233">The most recent date and time when media was mounted on the device.</span></span> <span data-ttu-id="86c5f-234">只有支援卸載式媒體的裝置會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="86c5f-234">This property is only used by devices that support removable media.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-235">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="86c5f-235">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-236">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="86c5f-236">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-238">載入媒體以進行資料傳輸或清除裝置的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="86c5f-238">The time, in seconds, that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="86c5f-239">如果裝置不支援卸載式媒體，則應該將此屬性設定為零。</span><span class="sxs-lookup"><span data-stu-id="86c5f-239">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-240">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="86c5f-240">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-241">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86c5f-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-243">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒的 kb」 ) ， **PUnit** ( "byte/Second \* 10 ^ 3" ) </span><span class="sxs-lookup"><span data-stu-id="86c5f-243">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes per Second"), **PUnit** ("byte / second \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-244">裝置可以讀取和寫入媒體的持續性資料傳輸速率（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="86c5f-244">The sustained data transfer rate in kilobytes at which the device can read and write to a media.</span></span> <span data-ttu-id="86c5f-245">這是持續性的原始資料費率。</span><span class="sxs-lookup"><span data-stu-id="86c5f-245">This is a sustained, raw data rate.</span></span> <span data-ttu-id="86c5f-246">此屬性不應回報最大速率或使用壓縮的速率。</span><span class="sxs-lookup"><span data-stu-id="86c5f-246">Maximum rates or rates with compression should not be reported in this property.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-247">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="86c5f-247">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-248">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86c5f-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-250">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**"，"**CIM \_ MediaAccessDevice**.**UnitsUsed**") </span><span class="sxs-lookup"><span data-stu-id="86c5f-250">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**", "**CIM\_MediaAccessDevice**.**UnitsUsed**")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-251">描述 **MaxUnitsBeforeCleaning** 和 **UnitsUsed** 屬性的單位類型。</span><span class="sxs-lookup"><span data-stu-id="86c5f-251">Describes the unit type of the **MaxUnitsBeforeCleaning** and **UnitsUsed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-252">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="86c5f-252">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-253">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="86c5f-253">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-255">限定詞：量測 [**計、**](/windows/desktop/WmiSdk/standard-qualifiers) [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (」**CIM \_ MediaAccessDevice**。**UnitsDescription**"，"**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**") </span><span class="sxs-lookup"><span data-stu-id="86c5f-255">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**", "**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-256">裝置使用的單位數。</span><span class="sxs-lookup"><span data-stu-id="86c5f-256">The number of units used by the device.</span></span> <span data-ttu-id="86c5f-257">這個屬性是用來決定何時應該清除裝置。</span><span class="sxs-lookup"><span data-stu-id="86c5f-257">This property is used to determine when the device should be cleaned.</span></span> <span data-ttu-id="86c5f-258">**UnitsDescription** 會定義單位類型。</span><span class="sxs-lookup"><span data-stu-id="86c5f-258">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="86c5f-259">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="86c5f-259">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86c5f-260">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="86c5f-260">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86c5f-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86c5f-262">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) ， **PUnit** ( "第 \* 10 ^-3" ) </span><span class="sxs-lookup"><span data-stu-id="86c5f-262">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="86c5f-263">裝置從讀取或寫入媒體轉換成卸載時所花費的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="86c5f-263">The time it takes, in milliseconds, for the device to transition from reading or writing media to unloading.</span></span> <span data-ttu-id="86c5f-264">例如，對於磁片磁碟機而言，這是磁片在具有名義速度和沒有旋轉磁片之間的間隔時間。</span><span class="sxs-lookup"><span data-stu-id="86c5f-264">For example, for disk drives, this is the interval between a disk spinning at nominal speeds and a disk not spinning.</span></span> <span data-ttu-id="86c5f-265">針對磁帶機，這是媒體從其 BOT 進入完全退出並可供選擇器元素或人類操作的時間。</span><span class="sxs-lookup"><span data-stu-id="86c5f-265">For tape drives, this is the time for a media to go from its BOT to being fully ejected and accessible to a picker element or human operator.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86c5f-266">規格需求</span><span class="sxs-lookup"><span data-stu-id="86c5f-266">Requirements</span></span>



| <span data-ttu-id="86c5f-267">需求</span><span class="sxs-lookup"><span data-stu-id="86c5f-267">Requirement</span></span> | <span data-ttu-id="86c5f-268">值</span><span class="sxs-lookup"><span data-stu-id="86c5f-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c5f-269">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86c5f-269">Minimum supported client</span></span><br/> | <span data-ttu-id="86c5f-270">Windows 8</span><span class="sxs-lookup"><span data-stu-id="86c5f-270">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="86c5f-271">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86c5f-271">Minimum supported server</span></span><br/> | <span data-ttu-id="86c5f-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="86c5f-272">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="86c5f-273">命名空間</span><span class="sxs-lookup"><span data-stu-id="86c5f-273">Namespace</span></span><br/>                | <span data-ttu-id="86c5f-274">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="86c5f-274">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="86c5f-275">MOF</span><span class="sxs-lookup"><span data-stu-id="86c5f-275">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86c5f-276"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="86c5f-276"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="86c5f-277">DLL</span><span class="sxs-lookup"><span data-stu-id="86c5f-277">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86c5f-278"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="86c5f-278"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="86c5f-279">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86c5f-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c5f-280">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="86c5f-280">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

