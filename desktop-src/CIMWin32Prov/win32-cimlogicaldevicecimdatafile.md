---
description: Win32 \_ CIMLogicalDeviceCIMDataFile 關聯 WMI 類別會關聯邏輯裝置和資料檔案，指出裝置所使用的驅動程式檔案。 此類別是用來探索裝置所使用的設備磁碟機。
ms.assetid: 892272de-920d-4fa0-adbc-f584ed6e8748
ms.tgt_platform: multiple
title: Win32_CIMLogicalDeviceCIMDataFile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CIMLogicalDeviceCIMDataFile
- Win32_CIMLogicalDeviceCIMDataFile.Dependent
- Win32_CIMLogicalDeviceCIMDataFile.Antecedent
- Win32_CIMLogicalDeviceCIMDataFile.Purpose
- Win32_CIMLogicalDeviceCIMDataFile.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15db6209360cbd150a722dc98b6255afd696cbe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510661"
---
# <a name="win32_cimlogicaldevicecimdatafile-class"></a><span data-ttu-id="42710-104">Win32 \_ CIMLogicalDeviceCIMDataFile 類別</span><span class="sxs-lookup"><span data-stu-id="42710-104">Win32\_CIMLogicalDeviceCIMDataFile class</span></span>

<span data-ttu-id="42710-105">**Win32 \_ CIMLogicalDeviceCIMDataFile** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會關聯邏輯裝置和資料檔案，指出裝置所使用的驅動程式檔案。</span><span class="sxs-lookup"><span data-stu-id="42710-105">The **Win32\_CIMLogicalDeviceCIMDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical devices and data files, indicating the driver files used by the device.</span></span> <span data-ttu-id="42710-106">此類別是用來探索裝置所使用的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="42710-106">This class is used to discover which device drivers a device uses.</span></span>

<span data-ttu-id="42710-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="42710-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="42710-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="42710-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="42710-109">語法</span><span class="sxs-lookup"><span data-stu-id="42710-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C510-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CIMLogicalDeviceCIMDataFile : CIM_Dependency
{
  CIM_DataFile      REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint16                Purpose;
  string                PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="42710-110">成員</span><span class="sxs-lookup"><span data-stu-id="42710-110">Members</span></span>

<span data-ttu-id="42710-111">**Win32 \_ CIMLogicalDeviceCIMDataFile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="42710-111">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="42710-112">屬性</span><span class="sxs-lookup"><span data-stu-id="42710-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42710-113">屬性</span><span class="sxs-lookup"><span data-stu-id="42710-113">Properties</span></span>

<span data-ttu-id="42710-114">**Win32 \_ CIMLogicalDeviceCIMDataFile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="42710-114">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42710-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="42710-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42710-116">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="42710-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="42710-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42710-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42710-118">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "cim \| CIM \_ LogicalDevice" ) </span><span class="sxs-lookup"><span data-stu-id="42710-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="42710-119">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，表示資料檔正在使用的邏輯裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="42710-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is being used by the data file.</span></span>

</dd> <dt>

<span data-ttu-id="42710-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="42710-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42710-121">資料類型： **CIM 資料 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="42710-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="42710-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42710-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42710-123">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「cim \| cim \_ 資料檔案」 ) </span><span class="sxs-lookup"><span data-stu-id="42710-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="42710-124">[**CIM 資料 \_ 檔**](cim-datafile.md)，代表指派給邏輯裝置的資料檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="42710-124">A [**CIM\_DataFile**](cim-datafile.md) that represents the properties of the data file assigned to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="42710-125">**目的**</span><span class="sxs-lookup"><span data-stu-id="42710-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42710-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="42710-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42710-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42710-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42710-128">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM" ) </span><span class="sxs-lookup"><span data-stu-id="42710-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="42710-129">資料檔案與其相關聯邏輯裝置的播放角色。</span><span class="sxs-lookup"><span data-stu-id="42710-129">Role that the data file plays with regard to its associated logical device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="42710-130">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="42710-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="42710-131">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="42710-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="42710-132">**驅動程式** (2) </span><span class="sxs-lookup"><span data-stu-id="42710-132">**Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="42710-133">**Configuration Software** (3) </span><span class="sxs-lookup"><span data-stu-id="42710-133">**Configuration Software** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="42710-134">**應用程式軟體** (4) </span><span class="sxs-lookup"><span data-stu-id="42710-134">**Application Software** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="42710-135">**檢測** (5) </span><span class="sxs-lookup"><span data-stu-id="42710-135">**Instrumentation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="42710-136">**固件** (6) </span><span class="sxs-lookup"><span data-stu-id="42710-136">**Firmware** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="42710-137">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="42710-137">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42710-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42710-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42710-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42710-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42710-140">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM" ) </span><span class="sxs-lookup"><span data-stu-id="42710-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="42710-141">擴充此類別的 **目的** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="42710-141">Extends the value of the **Purpose** property of this class.</span></span>

<span data-ttu-id="42710-142">範例：「磁片磁碟機磁碟機」</span><span class="sxs-lookup"><span data-stu-id="42710-142">Example: "Floppy Disk Driver"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42710-143">備註</span><span class="sxs-lookup"><span data-stu-id="42710-143">Remarks</span></span>

<span data-ttu-id="42710-144">**Win32 \_ CIMLogicalDeviceCIMDataFile** 類別衍生自 CIM 相依 [**性 \_**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="42710-144">The **Win32\_CIMLogicalDeviceCIMDataFile** class is derived from [**CIM\_Dependency**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42710-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="42710-145">Requirements</span></span>



| <span data-ttu-id="42710-146">需求</span><span class="sxs-lookup"><span data-stu-id="42710-146">Requirement</span></span> | <span data-ttu-id="42710-147">值</span><span class="sxs-lookup"><span data-stu-id="42710-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42710-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42710-148">Minimum supported client</span></span><br/> | <span data-ttu-id="42710-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42710-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42710-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42710-150">Minimum supported server</span></span><br/> | <span data-ttu-id="42710-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42710-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42710-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="42710-152">Namespace</span></span><br/>                | <span data-ttu-id="42710-153">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="42710-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="42710-154">MOF</span><span class="sxs-lookup"><span data-stu-id="42710-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42710-155"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="42710-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="42710-156">DLL</span><span class="sxs-lookup"><span data-stu-id="42710-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42710-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42710-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42710-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42710-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42710-159">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="42710-159">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="42710-160">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="42710-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

