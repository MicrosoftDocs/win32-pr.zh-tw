---
description: 描述儲存資料和允許抓取資料的媒體功能和管理。 此超級類別可用來代表軟體和硬體 RAID 元件，或實體媒體的原始邏輯範圍。
ms.assetid: 29d105fb-8c34-4824-8679-883aef02a0c9
title: 'CIM_StorageExtent 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageExtent
- CIM_StorageExtent.DataOrganization
- CIM_StorageExtent.Purpose
- CIM_StorageExtent.Access
- CIM_StorageExtent.ErrorMethodology
- CIM_StorageExtent.BlockSize
- CIM_StorageExtent.NumberOfBlocks
- CIM_StorageExtent.ConsumableBlocks
- CIM_StorageExtent.IsBasedOnUnderlyingRedundancy
- CIM_StorageExtent.SequentialAccess
- CIM_StorageExtent.ExtentStatus
- CIM_StorageExtent.NoSinglePointOfFailure
- CIM_StorageExtent.DataRedundancy
- CIM_StorageExtent.PackageRedundancy
- CIM_StorageExtent.DeltaReservation
- CIM_StorageExtent.Primordial
- CIM_StorageExtent.Name
- CIM_StorageExtent.NameFormat
- CIM_StorageExtent.NameNamespace
- CIM_StorageExtent.OtherNameNamespace
- CIM_StorageExtent.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a3dc1b58dd97582e229497e754d10c3f307eab76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993141"
---
# <a name="cim_storageextent-class-hyper-v-management"></a><span data-ttu-id="04d42-104">CIM_StorageExtent 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="04d42-104">CIM_StorageExtent class (Hyper-V management)</span></span>

<span data-ttu-id="04d42-105">描述儲存資料和允許抓取資料的媒體功能和管理。</span><span class="sxs-lookup"><span data-stu-id="04d42-105">Describes the capabilities and management of media that stores data and allows retrieval of the data.</span></span> <span data-ttu-id="04d42-106">此超級類別可用來代表軟體和硬體 RAID 元件，或實體媒體的原始邏輯範圍。</span><span class="sxs-lookup"><span data-stu-id="04d42-106">This super class is used to represent software and hardware RAID components, or a raw logical extent of physical media.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d42-107">語法</span><span class="sxs-lookup"><span data-stu-id="04d42-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.13.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_StorageExtent : CIM_LogicalDevice
{
  uint16  DataOrganization;
  string  Purpose;
  uint16  Access;
  string  ErrorMethodology;
  uint64  BlockSize;
  uint64  NumberOfBlocks;
  uint64  ConsumableBlocks;
  boolean IsBasedOnUnderlyingRedundancy;
  boolean SequentialAccess;
  uint16  ExtentStatus[];
  boolean NoSinglePointOfFailure;
  uint16  DataRedundancy;
  uint16  PackageRedundancy;
  uint8   DeltaReservation;
  boolean Primordial = FALSE;
  string  Name;
  uint16  NameFormat;
  uint16  NameNamespace;
  string  OtherNameNamespace;
  string  OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="04d42-108">成員</span><span class="sxs-lookup"><span data-stu-id="04d42-108">Members</span></span>

<span data-ttu-id="04d42-109">**CIM \_ StorageExtent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="04d42-109">The **CIM\_StorageExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="04d42-110">屬性</span><span class="sxs-lookup"><span data-stu-id="04d42-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04d42-111">屬性</span><span class="sxs-lookup"><span data-stu-id="04d42-111">Properties</span></span>

<span data-ttu-id="04d42-112">**CIM \_ StorageExtent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="04d42-112">The **CIM\_StorageExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04d42-113">**存取**</span><span class="sxs-lookup"><span data-stu-id="04d42-113">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04d42-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04d42-116">媒體的讀取/寫入支援描述。</span><span class="sxs-lookup"><span data-stu-id="04d42-116">A description of the read/write support of the media.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="04d42-117">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="04d42-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="04d42-118">**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="04d42-118">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="04d42-119">可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="04d42-119">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="04d42-120">支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="04d42-120">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="04d42-121">**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="04d42-121">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="04d42-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="04d42-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-123">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="04d42-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d42-125">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 主機存放裝置 \| 001.4 "，" MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits "，" MIF。DMTF \| 儲存裝置 \| 001.5」 ) </span><span class="sxs-lookup"><span data-stu-id="04d42-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.4", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits", "MIF.DMTF\|Storage Devices\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="04d42-126">形成儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="04d42-126">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="04d42-127">如果使用變數區塊大小，則此屬性應指定最大區塊大小。</span><span class="sxs-lookup"><span data-stu-id="04d42-127">If variable block sizes are used, then this property should specify the maximum block size.</span></span> <span data-ttu-id="04d42-128">如果區塊大小未知或區塊概念無效 (例如，對於 **cim \_ AggregateExtent**、 [**cim \_ 記憶體**](cim-memory.md) 或 [**cim \_ LogicalDisk**](cim-logicaldisk.md)) ，則此屬性應該設為 "1" (未知) 。</span><span class="sxs-lookup"><span data-stu-id="04d42-128">If the block size is unknown or if a block concept is not valid (for example, for **CIM\_AggregateExtent**, [**CIM\_Memory**](cim-memory.md) or [**CIM\_LogicalDisk**](cim-logicaldisk.md)), then this property should be set to "1" (unknow).</span></span>

</dd> <dt>

<span data-ttu-id="04d42-129">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="04d42-129">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-130">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="04d42-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04d42-132">當您使用 [**cim \_ BasedOn**](cim-basedon.md)類別關聯將 **cim \_ StorageExtent** 分層時，可使用的區塊數目上限。</span><span class="sxs-lookup"><span data-stu-id="04d42-132">The maximum number of blocks, that are available for use when layering **CIM\_StorageExtent** using the [**CIM\_BasedOn**](cim-basedon.md) class association.</span></span> <span data-ttu-id="04d42-133">這個屬性只有在 **CIM \_ BasedOn** 物件的 [ **Antecedent** ] 屬性中參考儲存範圍時才有意義。</span><span class="sxs-lookup"><span data-stu-id="04d42-133">This property only has meaning when the storage extent is referenced in the **Antecedent** property in a **CIM\_BasedOn** object.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-134">**DataOrganization**</span><span class="sxs-lookup"><span data-stu-id="04d42-134">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-135">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04d42-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04d42-137">媒體所使用的資料組織類型。</span><span class="sxs-lookup"><span data-stu-id="04d42-137">The type of data organization used by the media.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="04d42-138">**其他** (0) </span><span class="sxs-lookup"><span data-stu-id="04d42-138">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="04d42-139">**未知** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="04d42-139">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Block"></span><span id="fixed_block"></span><span id="FIXED_BLOCK"></span>

<span data-ttu-id="04d42-140">**固定區塊** (2) </span><span class="sxs-lookup"><span data-stu-id="04d42-140">**Fixed Block** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable_Block"></span><span id="variable_block"></span><span id="VARIABLE_BLOCK"></span>

<span data-ttu-id="04d42-141">**變數區塊** (3) </span><span class="sxs-lookup"><span data-stu-id="04d42-141">**Variable Block** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Count_Key_Data"></span><span id="count_key_data"></span><span id="COUNT_KEY_DATA"></span>

<span data-ttu-id="04d42-142">**計算索引鍵資料** (4) </span><span class="sxs-lookup"><span data-stu-id="04d42-142">**Count Key Data** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="04d42-143">**DataRedundancy**</span><span class="sxs-lookup"><span data-stu-id="04d42-143">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04d42-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d42-146">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**"，"**CIM \_ StorageSetting**.**DataRedundancyMax**"，"**CIM \_ StorageSetting**.**DataRedundancyMin**") </span><span class="sxs-lookup"><span data-stu-id="04d42-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**", "**CIM\_StorageSetting**.**DataRedundancyMax**", "**CIM\_StorageSetting**.**DataRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="04d42-147">目前維護之資料的完整複本數目。</span><span class="sxs-lookup"><span data-stu-id="04d42-147">The number of complete copies of data that are currently maintained.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-148">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="04d42-148">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-149">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="04d42-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d42-151">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "百分比" ) 、 [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Int32.maxvalue (100**](/windows/desktop/WmiSdk/standard-qualifiers)) 、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting)。**DeltaReservationGoal**"，"**CIM \_ StorageSetting**.**DeltaReservationMax**"，"**CIM \_ StorageSetting**.**DeltaReservationMin**") </span><span class="sxs-lookup"><span data-stu-id="04d42-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percentage"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**", "**CIM\_StorageSetting**.**DeltaReservationMax**", "**CIM\_StorageSetting**.**DeltaReservationMin**")</span></span>
</dt> </dl>

<span data-ttu-id="04d42-152">Delta 保留的目前值。</span><span class="sxs-lookup"><span data-stu-id="04d42-152">The current value for delta reservation.</span></span> <span data-ttu-id="04d42-153">這是一個百分比，可指定要在複本中保留以進行快取變更的空間量。</span><span class="sxs-lookup"><span data-stu-id="04d42-153">This is a percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-154">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="04d42-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04d42-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04d42-157">儲存範圍所支援的錯誤偵測類型和修正。</span><span class="sxs-lookup"><span data-stu-id="04d42-157">The type of error detection and correction supported by the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-158">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="04d42-158">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-159">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="04d42-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="04d42-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04d42-161">其他狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="04d42-161">Additional status information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="04d42-162">**其他** (0) </span><span class="sxs-lookup"><span data-stu-id="04d42-162">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="04d42-163">**未知** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="04d42-163">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None_Not_Applicable"></span><span id="none_not_applicable"></span><span id="NONE_NOT_APPLICABLE"></span>

<span data-ttu-id="04d42-164">**無/不適用** (2) </span><span class="sxs-lookup"><span data-stu-id="04d42-164">**None/Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broken"></span><span id="broken"></span><span id="BROKEN"></span>

<span data-ttu-id="04d42-165"> (3) **中斷**</span><span class="sxs-lookup"><span data-stu-id="04d42-165">**Broken** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Lost"></span><span id="data_lost"></span><span id="DATA_LOST"></span>

<span data-ttu-id="04d42-166">**資料遺失** (4) </span><span class="sxs-lookup"><span data-stu-id="04d42-166">**Data Lost** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Reconfig"></span><span id="dynamic_reconfig"></span><span id="DYNAMIC_RECONFIG"></span>

<span data-ttu-id="04d42-167">**Dynamic 重新設定** (5) </span><span class="sxs-lookup"><span data-stu-id="04d42-167">**Dynamic Reconfig** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Exposed"></span><span id="exposed"></span><span id="EXPOSED"></span>

<span data-ttu-id="04d42-168">**公開** (6) </span><span class="sxs-lookup"><span data-stu-id="04d42-168">**Exposed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Fractionally_Exposed"></span><span id="fractionally_exposed"></span><span id="FRACTIONALLY_EXPOSED"></span>

<span data-ttu-id="04d42-169">**Fractionally 公開** (7) </span><span class="sxs-lookup"><span data-stu-id="04d42-169">**Fractionally Exposed** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Exposed"></span><span id="partially_exposed"></span><span id="PARTIALLY_EXPOSED"></span>

<span data-ttu-id="04d42-170">**部分公開** (8) </span><span class="sxs-lookup"><span data-stu-id="04d42-170">**Partially Exposed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Disabled"></span><span id="protection_disabled"></span><span id="PROTECTION_DISABLED"></span>

<span data-ttu-id="04d42-171"> (9) **停用保護**</span><span class="sxs-lookup"><span data-stu-id="04d42-171">**Protection Disabled** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Readying"></span><span id="readying"></span><span id="READYING"></span>

<span data-ttu-id="04d42-172">準備 **就緒** (10) </span><span class="sxs-lookup"><span data-stu-id="04d42-172">**Readying** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Rebuild"></span><span id="rebuild"></span><span id="REBUILD"></span>

<span data-ttu-id="04d42-173">**重建** (11) </span><span class="sxs-lookup"><span data-stu-id="04d42-173">**Rebuild** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Recalculate"></span><span id="recalculate"></span><span id="RECALCULATE"></span>

<span data-ttu-id="04d42-174">**重新計算** (12) </span><span class="sxs-lookup"><span data-stu-id="04d42-174">**Recalculate** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Spare_in_Use"></span><span id="spare_in_use"></span><span id="SPARE_IN_USE"></span>

<span data-ttu-id="04d42-175">**使用中的備用** (13) </span><span class="sxs-lookup"><span data-stu-id="04d42-175">**Spare in Use** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Verify_In_Progress"></span><span id="verify_in_progress"></span><span id="VERIFY_IN_PROGRESS"></span>

<span data-ttu-id="04d42-176">**確認進行中** (14) </span><span class="sxs-lookup"><span data-stu-id="04d42-176">**Verify In Progress** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="In-Band_Access_Granted"></span><span id="in-band_access_granted"></span><span id="IN-BAND_ACCESS_GRANTED"></span>

<span data-ttu-id="04d42-177">**授與 (15) 的頻外存取**</span><span class="sxs-lookup"><span data-stu-id="04d42-177">**In-Band Access Granted** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Imported"></span><span id="imported"></span><span id="IMPORTED"></span>

<span data-ttu-id="04d42-178">匯 **入** (16) </span><span class="sxs-lookup"><span data-stu-id="04d42-178">**Imported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Exported"></span><span id="exported"></span><span id="EXPORTED"></span>

<span data-ttu-id="04d42-179">**匯出** (17) </span><span class="sxs-lookup"><span data-stu-id="04d42-179">**Exported** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="04d42-180">**DMTF 保留** (18. 32767) </span><span class="sxs-lookup"><span data-stu-id="04d42-180">**DMTF Reserved** (18..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="04d42-181">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="04d42-181">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="04d42-182">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="04d42-182">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-183">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="04d42-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04d42-185">如果基礎儲存範圍是 [**CIM \_ StorageRedundancyGroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup)的成員，則 **為 true** ，否則為 **false**。</span><span class="sxs-lookup"><span data-stu-id="04d42-185">**true** if the underlying storage extents are members of a [**CIM\_StorageRedundancyGroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-186">**名稱**</span><span class="sxs-lookup"><span data-stu-id="04d42-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04d42-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d42-189">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SPC。INCITS-T10 \| VPD 83、Association 0 \| 識別碼 ") 、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**。**NameFormat**"，"**CIM \_ StorageExtent**.**NameNamespace**") </span><span class="sxs-lookup"><span data-stu-id="04d42-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**", "**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="04d42-190">儲存區的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="04d42-190">A unique identifier for the storage extent.</span></span> <span data-ttu-id="04d42-191">**NameFormat** 屬性會指定要在 **Name** 屬性中使用的命名格式。</span><span class="sxs-lookup"><span data-stu-id="04d42-191">The **NameFormat** property specifies the naming format to use in the **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-192">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="04d42-192">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-193">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04d42-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d42-195">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ StorageExtent**.**Name**"，"**CIM \_ StorageExtent**。**NameNamespace**"，"**CIM \_ StorageExtent**.**OtherNameFormat**") </span><span class="sxs-lookup"><span data-stu-id="04d42-195">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**NameNamespace**", "**CIM\_StorageExtent**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="04d42-196">**Name** 屬性的命名格式。</span><span class="sxs-lookup"><span data-stu-id="04d42-196">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="04d42-197">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="04d42-197">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="04d42-198">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="04d42-198">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA6"></span><span id="vpd83naa6"></span>

<span data-ttu-id="04d42-199">**VPD83NAA6** (2) </span><span class="sxs-lookup"><span data-stu-id="04d42-199">**VPD83NAA6** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA5"></span><span id="vpd83naa5"></span>

<span data-ttu-id="04d42-200">**VPD83NAA5** (3) </span><span class="sxs-lookup"><span data-stu-id="04d42-200">**VPD83NAA5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="04d42-201">**VPD83Type2** (4) </span><span class="sxs-lookup"><span data-stu-id="04d42-201">**VPD83Type2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="04d42-202">**VPD83Type1** (5) </span><span class="sxs-lookup"><span data-stu-id="04d42-202">**VPD83Type1** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type0"></span><span id="vpd83type0"></span><span id="VPD83TYPE0"></span>

<span data-ttu-id="04d42-203">**VPD83Type0** (6) </span><span class="sxs-lookup"><span data-stu-id="04d42-203">**VPD83Type0** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="04d42-204">**SNVM** (7) </span><span class="sxs-lookup"><span data-stu-id="04d42-204">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="04d42-205">**NodeWWN** (8) </span><span class="sxs-lookup"><span data-stu-id="04d42-205">**NodeWWN** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="04d42-206">**NAA** (9) </span><span class="sxs-lookup"><span data-stu-id="04d42-206">**NAA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="04d42-207">**EUI64** (10) </span><span class="sxs-lookup"><span data-stu-id="04d42-207">**EUI64** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="04d42-208">**T10VID** (11) </span><span class="sxs-lookup"><span data-stu-id="04d42-208">**T10VID** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="04d42-209">**OS 裝置名稱** (12) </span><span class="sxs-lookup"><span data-stu-id="04d42-209">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="04d42-210">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="04d42-210">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-211">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04d42-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d42-213">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SPC。INCITS-T10 \| VPD 83、Association 0 \| 識別碼 ") 、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**。**Name**"，"**CIM \_ StorageExtent**。**OtherNameNamespace**"，"**CIM \_ StorageExtent**.**NameFormat**") </span><span class="sxs-lookup"><span data-stu-id="04d42-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**OtherNameNamespace**", "**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="04d42-214">Name 屬性的命名空間。</span><span class="sxs-lookup"><span data-stu-id="04d42-214">The namespace of the name property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="04d42-215">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="04d42-215">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="04d42-216">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="04d42-216">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="04d42-217">**VPD83Type3** (2) </span><span class="sxs-lookup"><span data-stu-id="04d42-217">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="04d42-218">**VPD83Type2** (3) </span><span class="sxs-lookup"><span data-stu-id="04d42-218">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="04d42-219">**VPD83Type1** (4) </span><span class="sxs-lookup"><span data-stu-id="04d42-219">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="04d42-220">**VPD80** (5) </span><span class="sxs-lookup"><span data-stu-id="04d42-220">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="04d42-221">**NodeWWN** (6) </span><span class="sxs-lookup"><span data-stu-id="04d42-221">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="04d42-222">**SNVM** (7) </span><span class="sxs-lookup"><span data-stu-id="04d42-222">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="04d42-223">**OS 裝置命名空間** (8) </span><span class="sxs-lookup"><span data-stu-id="04d42-223">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="04d42-224">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="04d42-224">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-225">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="04d42-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d42-227">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**") </span><span class="sxs-lookup"><span data-stu-id="04d42-227">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")</span></span>
</dt> </dl>

<span data-ttu-id="04d42-228">如果沒有任何單一失敗點，**則為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="04d42-228">**true** if there are not any single points of failure; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-229">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="04d42-229">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-230">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="04d42-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d42-232">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 主機存放裝置 \| 001.5 "，" MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="04d42-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="04d42-233">形成儲存區的邏輯連續區塊總數。</span><span class="sxs-lookup"><span data-stu-id="04d42-233">The total number of logically contiguous blocks that form the storage extent.</span></span> <span data-ttu-id="04d42-234">儲存區的總大小是藉由 **NumberOfBlocks** 來乘以 **區塊** 來計算。</span><span class="sxs-lookup"><span data-stu-id="04d42-234">The total size of the storage extent is calculated by multiplying **BlockSize** by **NumberOfBlocks**.</span></span> <span data-ttu-id="04d42-235">如果 **區塊** 值為 "1"，則此屬性為儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="04d42-235">If the **BlockSize** is "1", this property is the total size of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-236">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="04d42-236">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04d42-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d42-239">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ StorageExtent**.**NameFormat**") </span><span class="sxs-lookup"><span data-stu-id="04d42-239">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="04d42-240">當 **NameFormat** 屬性設定為 "1" (其他) 時， **Name** 屬性的格式。</span><span class="sxs-lookup"><span data-stu-id="04d42-240">The format of the **Name** property when the **NameFormat** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="04d42-241">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="04d42-241">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04d42-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d42-244">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ StorageExtent**.**NameNamespace**") </span><span class="sxs-lookup"><span data-stu-id="04d42-244">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="04d42-245">當 **NameNamespace** 屬性設定為 "1" (其他) 時， **Name** 屬性的命名空間描述。</span><span class="sxs-lookup"><span data-stu-id="04d42-245">A description of the namespace of the **Name** property when the **NameNamespace** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="04d42-246">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="04d42-246">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-247">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04d42-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d42-249">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**"，"**CIM \_ StorageSetting**.**PackageRedundancyMax**"，"**CIM \_ StorageSetting**.**PackageRedundancyMin**") </span><span class="sxs-lookup"><span data-stu-id="04d42-249">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**", "**CIM\_StorageSetting**.**PackageRedundancyMax**", "**CIM\_StorageSetting**.**PackageRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="04d42-250">在不遺失資料的情況下，可能失敗的目前實體封裝數目。</span><span class="sxs-lookup"><span data-stu-id="04d42-250">The current number of physical packages that can fail without data loss.</span></span> <span data-ttu-id="04d42-251">例如，在存放裝置網域中，這可能是磁片主軸的數目。</span><span class="sxs-lookup"><span data-stu-id="04d42-251">For example, in a storage domain, this might be the number of disk spindles.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-252">**原始**</span><span class="sxs-lookup"><span data-stu-id="04d42-252">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-253">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="04d42-253">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04d42-255">如果儲存區是原始的，則為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="04d42-255">**true** if the storage extent is primordial; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-256">**目的**</span><span class="sxs-lookup"><span data-stu-id="04d42-256">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04d42-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d42-259">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageDescr ") </span><span class="sxs-lookup"><span data-stu-id="04d42-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageDescr")</span></span>
</dt> </dl>

<span data-ttu-id="04d42-260">媒體使用方式的描述。</span><span class="sxs-lookup"><span data-stu-id="04d42-260">A description of the media usage.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-261">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="04d42-261">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d42-262">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="04d42-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04d42-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04d42-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04d42-264">如果 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)物件以順序存取儲存體，則 **為 true** ，否則為 **false**。</span><span class="sxs-lookup"><span data-stu-id="04d42-264">**true** if storage is sequentially accessed by a [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) object; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04d42-265">規格需求</span><span class="sxs-lookup"><span data-stu-id="04d42-265">Requirements</span></span>



| <span data-ttu-id="04d42-266">需求</span><span class="sxs-lookup"><span data-stu-id="04d42-266">Requirement</span></span> | <span data-ttu-id="04d42-267">值</span><span class="sxs-lookup"><span data-stu-id="04d42-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04d42-268">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04d42-268">Minimum supported client</span></span><br/> | <span data-ttu-id="04d42-269">Windows 8</span><span class="sxs-lookup"><span data-stu-id="04d42-269">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="04d42-270">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04d42-270">Minimum supported server</span></span><br/> | <span data-ttu-id="04d42-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04d42-271">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="04d42-272">命名空間</span><span class="sxs-lookup"><span data-stu-id="04d42-272">Namespace</span></span><br/>                | <span data-ttu-id="04d42-273">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="04d42-273">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="04d42-274">MOF</span><span class="sxs-lookup"><span data-stu-id="04d42-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04d42-275"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="04d42-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04d42-276">DLL</span><span class="sxs-lookup"><span data-stu-id="04d42-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04d42-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04d42-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="04d42-278">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04d42-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d42-279">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="04d42-279">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

