---
description: 代表虛擬儲存體配置的設定。
ms.assetid: 128fd3e9-8759-4b2f-a881-d34e89c539ac
title: CIM_StorageAllocationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageAllocationSettingData
- CIM_StorageAllocationSettingData.VirtualResourceBlockSize
- CIM_StorageAllocationSettingData.VirtualQuantity
- CIM_StorageAllocationSettingData.VirtualQuantityUnits
- CIM_StorageAllocationSettingData.Access
- CIM_StorageAllocationSettingData.HostResourceBlockSize
- CIM_StorageAllocationSettingData.Reservation
- CIM_StorageAllocationSettingData.Limit
- CIM_StorageAllocationSettingData.HostExtentStartingAddress
- CIM_StorageAllocationSettingData.HostExtentName
- CIM_StorageAllocationSettingData.HostExtentNameFormat
- CIM_StorageAllocationSettingData.OtherHostExtentNameFormat
- CIM_StorageAllocationSettingData.HostExtentNameNamespace
- CIM_StorageAllocationSettingData.OtherHostExtentNameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e66322f20987e2d1f99042430f0f57cdc2e399d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693055"
---
# <a name="cim_storageallocationsettingdata-class"></a><span data-ttu-id="d8248-103">CIM \_ StorageAllocationSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="d8248-103">CIM\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="d8248-104">代表虛擬儲存體配置的設定。</span><span class="sxs-lookup"><span data-stu-id="d8248-104">Represents settings for the allocation of virtual storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8248-105">語法</span><span class="sxs-lookup"><span data-stu-id="d8248-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_StorageAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint64 VirtualResourceBlockSize;
  uint64 VirtualQuantity;
  string VirtualQuantityUnits = "count(fixed size block)";
  uint16 Access;
  uint64 HostResourceBlockSize;
  uint64 Reservation;
  uint64 Limit;
  uint64 HostExtentStartingAddress;
  string HostExtentName;
  uint16 HostExtentNameFormat;
  string OtherHostExtentNameFormat;
  uint16 HostExtentNameNamespace;
  string OtherHostExtentNameNamespace;
};
```

## <a name="members"></a><span data-ttu-id="d8248-106">成員</span><span class="sxs-lookup"><span data-stu-id="d8248-106">Members</span></span>

<span data-ttu-id="d8248-107">**CIM \_ StorageAllocationSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d8248-107">The **CIM\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d8248-108">屬性</span><span class="sxs-lookup"><span data-stu-id="d8248-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8248-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d8248-109">Properties</span></span>

<span data-ttu-id="d8248-110">**CIM \_ StorageAllocationSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d8248-110">The **CIM\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8248-111">**存取**</span><span class="sxs-lookup"><span data-stu-id="d8248-111">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-112">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d8248-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-114">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ StorageExtent**](cim-storageextent.md).**存取**") </span><span class="sxs-lookup"><span data-stu-id="d8248-114">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**Access**")</span></span>
</dt> </dl>

<span data-ttu-id="d8248-115">儲存體配置的讀取/寫入支援。</span><span class="sxs-lookup"><span data-stu-id="d8248-115">The read/write support of the storage allocation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8248-116">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d8248-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="d8248-117">**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="d8248-117">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="d8248-118">可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="d8248-118">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="d8248-119">支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="d8248-119">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d8248-120">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d8248-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8248-121">**HostExtentName**</span><span class="sxs-lookup"><span data-stu-id="d8248-121">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d8248-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-124">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**"，"**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**"，"[**CIM \_ StorageExtent**](cim-storageextent.md).**名稱**") </span><span class="sxs-lookup"><span data-stu-id="d8248-124">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="d8248-125">主機儲存區的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8248-125">A unique identifier of the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="d8248-126">**HostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="d8248-126">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d8248-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-129">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**.**HostExtentName**"，"**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameFormat**"，"[**CIM \_ StorageExtent**](cim-storageextent.md).**NameFormat**") </span><span class="sxs-lookup"><span data-stu-id="d8248-129">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="d8248-130">**HostExtentName** 屬性值的格式。</span><span class="sxs-lookup"><span data-stu-id="d8248-130">The format that of the **HostExtentName** property value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8248-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d8248-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d8248-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d8248-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="d8248-133"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7) </span><span class="sxs-lookup"><span data-stu-id="d8248-133"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d8248-134">序號/廠商/模型 (SNVM) SNVM 是代表廠商名稱、廠商命名空間內的產品名稱，以及模型命名空間內序號的3個字串。</span><span class="sxs-lookup"><span data-stu-id="d8248-134">Serial Number/Vendor/Model (SNVM) SNVM is 3 strings representing the vendor name, product name within the vendor namespace, and the serial number within the model namespace.</span></span> <span data-ttu-id="d8248-135">字串以 ' + ' 分隔。</span><span class="sxs-lookup"><span data-stu-id="d8248-135">Strings are delimited with a '+'.</span></span> <span data-ttu-id="d8248-136">可能包含空格，而且很重要。</span><span class="sxs-lookup"><span data-stu-id="d8248-136">Spaces may be included and are significant.</span></span> <span data-ttu-id="d8248-137">序號是以十六進位大寫表示之序號的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="d8248-137">The serial number is the text representation of the serial number in hexadecimal upper case.</span></span> <span data-ttu-id="d8248-138">這代表來自 SCSI 查詢資料的廠商和型號識別碼;廠商欄位必須是8個字元寬，而 product 欄位必須是16個字元寬。</span><span class="sxs-lookup"><span data-stu-id="d8248-138">This represents the vendor and model ID from SCSI Inquiry data; the vendor field MUST be 8 characters wide and the product field MUST be 16 characters wide.</span></span> <span data-ttu-id="d8248-139">例如，</span><span class="sxs-lookup"><span data-stu-id="d8248-139">For example,</span></span>

<span data-ttu-id="d8248-140">' ACME \_ \_ \_ \_ + SUPER DISK \_ \_ \_ \_ \_ \_ + 124437458 ' (\_ 是空白字元) </span><span class="sxs-lookup"><span data-stu-id="d8248-140">'ACME\_\_\_\_+SUPER DISK\_\_\_\_\_\_+124437458' (\_ is a space character)</span></span>

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="d8248-141"><span id="NAA"></span><span id="naa"></span>**NAA** (9) </span><span class="sxs-lookup"><span data-stu-id="d8248-141"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>


</dt> <dd>

<span data-ttu-id="d8248-142">9 = NAA 為一般格式。</span><span class="sxs-lookup"><span data-stu-id="d8248-142">9 = NAA as a generic format.</span></span> <span data-ttu-id="d8248-143">請參閱</span><span class="sxs-lookup"><span data-stu-id="d8248-143">See</span></span>

<span data-ttu-id="d8248-144"> https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span><span class="sxs-lookup"><span data-stu-id="d8248-144">https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span></span> <span data-ttu-id="d8248-145">格式化為16或32未分隔大寫十六進位字元 (每個二進位位元組) 2。</span><span class="sxs-lookup"><span data-stu-id="d8248-145">Formatted as 16 or 32 unseparated uppercase hex characters (2 per binary byte).</span></span>

<span data-ttu-id="d8248-146">例如 ' 21000020372D3C73 '</span><span class="sxs-lookup"><span data-stu-id="d8248-146">For example '21000020372D3C73'</span></span>

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="d8248-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10) </span><span class="sxs-lookup"><span data-stu-id="d8248-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>


</dt> <dd>

<span data-ttu-id="d8248-148">EUI 作為一般格式 (EUI64) 參閱</span><span class="sxs-lookup"><span data-stu-id="d8248-148">EUI as a generic format (EUI64) See</span></span>

<span data-ttu-id="d8248-149"> https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span><span class="sxs-lookup"><span data-stu-id="d8248-149">https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span></span>

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="d8248-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11) </span><span class="sxs-lookup"><span data-stu-id="d8248-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>


</dt> <dd>

<span data-ttu-id="d8248-151">T10 廠商識別碼格式，如 SCSI 查詢 VPD 頁面83、識別碼類型1所傳回。</span><span class="sxs-lookup"><span data-stu-id="d8248-151">T10 vendor identifier format as returned by SCSI Inquiry VPD page 83, identifier type 1.</span></span> <span data-ttu-id="d8248-152">請參閱 T10 SPC-3 規格。</span><span class="sxs-lookup"><span data-stu-id="d8248-152">See T10 SPC-3 specification.</span></span> <span data-ttu-id="d8248-153">這是 T10 登錄中的8位元組 ASCII 廠商識別碼，後面接著廠商特定的 ASCII 識別碼;允許使用空格。</span><span class="sxs-lookup"><span data-stu-id="d8248-153">This is the 8-byte ASCII vendor ID from the T10 registry followed by a vendor specific ASCII identifier; spaces are permitted.</span></span> <span data-ttu-id="d8248-154">若為非 SCSI 磁片區，' SNVM ' 可能是最適當的選擇。</span><span class="sxs-lookup"><span data-stu-id="d8248-154">For non SCSI volumes, 'SNVM' may be the most appropriate choice.</span></span>

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="d8248-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS 裝置名稱** (12) </span><span class="sxs-lookup"><span data-stu-id="d8248-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>


</dt> <dd>

<span data-ttu-id="d8248-156">LogicalDisks) 的 OS 裝置名稱 (。</span><span class="sxs-lookup"><span data-stu-id="d8248-156">OS Device Name (for LogicalDisks).</span></span> <span data-ttu-id="d8248-157">如需詳細資料，請參閱 LogicalDisk 名稱描述。</span><span class="sxs-lookup"><span data-stu-id="d8248-157">See LogicalDisk Name description for details.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d8248-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d8248-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8248-159">**HostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="d8248-159">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-160">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d8248-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-162">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**.**HostExtentName**"，"**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameNamespace**"，"**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**"，"[**CIM \_ StorageExtent**](cim-storageextent.md).**命名空間**") </span><span class="sxs-lookup"><span data-stu-id="d8248-162">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameNamespace**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Namespace**")</span></span>
</dt> </dl>

<span data-ttu-id="d8248-163">**Name** 屬性的命名格式。</span><span class="sxs-lookup"><span data-stu-id="d8248-163">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8248-164">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d8248-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d8248-165">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d8248-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="d8248-166">**VPD83Type3** (2) </span><span class="sxs-lookup"><span data-stu-id="d8248-166">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="d8248-167">**VPD83Type2** (3) </span><span class="sxs-lookup"><span data-stu-id="d8248-167">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="d8248-168">**VPD83Type1** (4) </span><span class="sxs-lookup"><span data-stu-id="d8248-168">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="d8248-169">**VPD80** (5) </span><span class="sxs-lookup"><span data-stu-id="d8248-169">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="d8248-170">**NodeWWN** (6) </span><span class="sxs-lookup"><span data-stu-id="d8248-170">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="d8248-171">**SNVM** (7) </span><span class="sxs-lookup"><span data-stu-id="d8248-171">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="d8248-172">**OS 裝置命名空間** (8) </span><span class="sxs-lookup"><span data-stu-id="d8248-172">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d8248-173">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d8248-173">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8248-174">**HostExtentStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="d8248-174">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-175">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d8248-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-177">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**"，"[**CIM \_ BasedOn**](cim-basedon.md).**StartingAddress**") </span><span class="sxs-lookup"><span data-stu-id="d8248-177">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**", "[**CIM\_BasedOn**](cim-basedon.md).**StartingAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="d8248-178">主機儲存區的起始位址。</span><span class="sxs-lookup"><span data-stu-id="d8248-178">The starting address on the host storage extent.</span></span> <span data-ttu-id="d8248-179">Null val; ue 表示虛擬儲存區和主機儲存區之間沒有直接對應。</span><span class="sxs-lookup"><span data-stu-id="d8248-179">A NULL val;ue indicates that there is no direct mapping between the virtual storage extent and the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="d8248-180">**HostResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="d8248-180">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-181">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d8248-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-183">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ StorageExtent**](cim-storageextent.md).**區塊**") ， **PUnit** (" byte ") </span><span class="sxs-lookup"><span data-stu-id="d8248-183">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="d8248-184">在主機上配置給儲存體配置之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8248-184">The size, in bytes, of the blocks that are allocated on the host for the storage allocation.</span></span> <span data-ttu-id="d8248-185">如果區塊大小為變數，則應該指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8248-185">If the block size is variable, then the maximum block size in bytes should be specified.</span></span> <span data-ttu-id="d8248-186">如果區塊大小未知或區塊概念未套用，則應該使用值 "1" (未知的) 。</span><span class="sxs-lookup"><span data-stu-id="d8248-186">If the block size is unknown or if a block concept does not apply, then the value "1" (unknown) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d8248-187">**限制**</span><span class="sxs-lookup"><span data-stu-id="d8248-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-188">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d8248-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-190">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Limit" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**。**HostResourceBlockSize**") </span><span class="sxs-lookup"><span data-stu-id="d8248-190">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="d8248-191">針對主機上的儲存體資源配置，將授與的區塊數目上限。</span><span class="sxs-lookup"><span data-stu-id="d8248-191">The maximum amount of blocks that will be granted for the storage resource allocation on the host.</span></span> <span data-ttu-id="d8248-192">區塊大小是由 **HostResourceBlockSize** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="d8248-192">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="d8248-193">**OtherHostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="d8248-193">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d8248-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-196">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**") </span><span class="sxs-lookup"><span data-stu-id="d8248-196">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="d8248-197">如果屬性設定為 "1" (其他) ，則為 **HostExtentName** 屬性的格式。</span><span class="sxs-lookup"><span data-stu-id="d8248-197">The format of the **HostExtentName** property if the property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="d8248-198">**OtherHostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="d8248-198">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d8248-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-201">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**") </span><span class="sxs-lookup"><span data-stu-id="d8248-201">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="d8248-202">字串，如果 **HostExtentNameNamespace** 屬性的值為 "1" (其他) ，則描述 **HostExtentName** 屬性的命名空間。</span><span class="sxs-lookup"><span data-stu-id="d8248-202">A string that describes the namespace of the **HostExtentName** property if the value of the **HostExtentNameNamespace** property is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="d8248-203">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="d8248-203">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-204">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d8248-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-206">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "保留" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**。**HostResourceBlockSize**") </span><span class="sxs-lookup"><span data-stu-id="d8248-206">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Reservation"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="d8248-207">保證可供主機上的儲存體資源配置使用的區塊數量。</span><span class="sxs-lookup"><span data-stu-id="d8248-207">The amount of blocks that are guaranteed to be available for the storage resource allocation on the host.</span></span> <span data-ttu-id="d8248-208">區塊大小是由 **HostResourceBlockSize** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="d8248-208">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="d8248-209">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="d8248-209">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-210">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d8248-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-212">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "VirtualQuantity" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ StorageExtent**](cim-storageextent.md)。**NumberOfBlocks**"，"**CIM \_ StorageAllocationSettingData**.**VirtualQuantityUnits**") </span><span class="sxs-lookup"><span data-stu-id="d8248-212">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**NumberOfBlocks**", "**CIM\_StorageAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="d8248-213">儲存體配置向取用者呈現的區塊數目。</span><span class="sxs-lookup"><span data-stu-id="d8248-213">The number of blocks that the storage allocation presents to the consumer.</span></span>

> [!Note]  
> <span data-ttu-id="d8248-214">**VirtualQuantity** 屬性可以指定 "1" 的區塊大小，即使 **VirtualResourceBlockSize** 是未知的。</span><span class="sxs-lookup"><span data-stu-id="d8248-214">The **VirtualQuantity** property can specify a block size of "1", even if **VirtualResourceBlockSize** is unknown.</span></span>

 

</dd> <dt>

<span data-ttu-id="d8248-215">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="d8248-215">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d8248-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-218">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "VirtualQuantityUnits" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**。**VirtualQuantity**") ， **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="d8248-218">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="d8248-219">**VirtualQuantity** 屬性所使用的單位。</span><span class="sxs-lookup"><span data-stu-id="d8248-219">The units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="d8248-220">此值應該設定為「count (固定大社區塊) 」或「位元組」。</span><span class="sxs-lookup"><span data-stu-id="d8248-220">This value shall should be set to "count(fixed size block)" or "byte".</span></span> <span data-ttu-id="d8248-221">預設值 "count (fixed size block) " 應該用於固定區塊大小，而 "byte" 應該用於未知或變數區塊大小。</span><span class="sxs-lookup"><span data-stu-id="d8248-221">The default value, "count(fixed size block)" should be used for a fixed block size, and "byte" should be used for an unknown or variable block size.</span></span>

</dd> <dt>

<span data-ttu-id="d8248-222">**VirtualResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="d8248-222">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8248-223">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d8248-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8248-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8248-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8248-225">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ StorageExtent**](cim-storageextent.md).**區塊**") ， **PUnit** (" byte ") </span><span class="sxs-lookup"><span data-stu-id="d8248-225">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="d8248-226">形成儲存體配置要求之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8248-226">The size, in bytes, of the blocks that form the storage allocation request.</span></span> <span data-ttu-id="d8248-227">如果區塊大小為變數，則應該指定最大區塊大小。</span><span class="sxs-lookup"><span data-stu-id="d8248-227">If the block size is variable, then the maximum block size should be specified.</span></span> <span data-ttu-id="d8248-228">如果區塊大小未知或區塊概念未套用，則區塊大小應該是 "1" (未知的) 。</span><span class="sxs-lookup"><span data-stu-id="d8248-228">If the block size is unknown or if a block concept does not apply, then the block size should be "1" (unknown).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8248-229">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8248-229">Requirements</span></span>



| <span data-ttu-id="d8248-230">需求</span><span class="sxs-lookup"><span data-stu-id="d8248-230">Requirement</span></span> | <span data-ttu-id="d8248-231">值</span><span class="sxs-lookup"><span data-stu-id="d8248-231">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8248-232">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8248-232">Minimum supported client</span></span><br/> | <span data-ttu-id="d8248-233">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d8248-233">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d8248-234">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8248-234">Minimum supported server</span></span><br/> | <span data-ttu-id="d8248-235">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d8248-235">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d8248-236">命名空間</span><span class="sxs-lookup"><span data-stu-id="d8248-236">Namespace</span></span><br/>                | <span data-ttu-id="d8248-237">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d8248-237">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d8248-238">MOF</span><span class="sxs-lookup"><span data-stu-id="d8248-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8248-239"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d8248-239"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8248-240">DLL</span><span class="sxs-lookup"><span data-stu-id="d8248-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8248-241"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8248-241"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8248-242">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8248-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8248-243">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="d8248-243">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

