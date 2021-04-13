---
description: CIM DeviceSoftware 關聯性 \_ 會識別與裝置相關聯的軟體，例如驅動程式、設定或應用程式軟體或固件。
ms.assetid: 831d0014-2a01-49f4-9642-fae5682f0388
ms.tgt_platform: multiple
title: CIM_DeviceSoftware 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSoftware
- CIM_DeviceSoftware.Dependent
- CIM_DeviceSoftware.Antecedent
- CIM_DeviceSoftware.Purpose
- CIM_DeviceSoftware.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 467fa670e8bb3f7d6ee967e6dd422102a2026a57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510633"
---
# <a name="cim_devicesoftware-class"></a><span data-ttu-id="b2e8d-103">CIM \_ DeviceSoftware 類別</span><span class="sxs-lookup"><span data-stu-id="b2e8d-103">CIM\_DeviceSoftware class</span></span>

<span data-ttu-id="b2e8d-104">**CIM \_ DeviceSoftware** 關聯性會識別與裝置相關聯的軟體，例如驅動程式、設定或應用程式軟體或固件。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-104">The **CIM\_DeviceSoftware** relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2e8d-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b2e8d-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b2e8d-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b2e8d-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e8d-109">語法</span><span class="sxs-lookup"><span data-stu-id="b2e8d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36363AAA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceSoftware : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_SoftwareElement REF Antecedent;
  uint16                  Purpose;
  string                  PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="b2e8d-110">成員</span><span class="sxs-lookup"><span data-stu-id="b2e8d-110">Members</span></span>

<span data-ttu-id="b2e8d-111">**CIM \_ DeviceSoftware** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b2e8d-111">The **CIM\_DeviceSoftware** class has these types of members:</span></span>

-   [<span data-ttu-id="b2e8d-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b2e8d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2e8d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b2e8d-113">Properties</span></span>

<span data-ttu-id="b2e8d-114">**CIM \_ DeviceSoftware** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-114">The **CIM\_DeviceSoftware** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2e8d-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-116">資料類型： **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b2e8d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="b2e8d-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-119">描述 software 元素的 [**CIM \_ SoftwareElement**](cim-softwareelement.md) 。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-119">A [**CIM\_SoftwareElement**](cim-softwareelement.md) that describes the software element.</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-121">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b2e8d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="b2e8d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-124">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，描述需要或使用軟體的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that requires or uses the software.</span></span>

</dd> <dt>

<span data-ttu-id="b2e8d-125">**目的**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b2e8d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-128">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ DeviceSoftware**.**PurposeDescription**") </span><span class="sxs-lookup"><span data-stu-id="b2e8d-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-129">軟體針對其相關聯裝置所採取的角色。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-129">Role that the software takes regarding its associated device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b2e8d-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b2e8d-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-131">不明。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-131">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b2e8d-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b2e8d-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-133">其他。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-133">Other.</span></span>

</dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="b2e8d-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**驅動程式** (2) </span><span class="sxs-lookup"><span data-stu-id="b2e8d-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Driver** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-135">司機。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-135">Driver.</span></span>

</dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="b2e8d-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Configuration Software** (3) </span><span class="sxs-lookup"><span data-stu-id="b2e8d-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Configuration Software** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-137">設定軟體。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-137">Configuration software.</span></span>

</dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="b2e8d-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**應用程式軟體** (4) </span><span class="sxs-lookup"><span data-stu-id="b2e8d-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Application Software** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-139">應用程式軟體。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-139">Application software.</span></span>

</dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="b2e8d-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**檢測** (5) </span><span class="sxs-lookup"><span data-stu-id="b2e8d-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Instrumentation** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-141">檢測。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-141">Instrumentation.</span></span>

</dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="b2e8d-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**固件** (6) </span><span class="sxs-lookup"><span data-stu-id="b2e8d-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Firmware** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-143">固件。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-143">Firmware.</span></span>

</dd> <dt>

<span id="BIOS"></span><span id="bios"></span>

<span data-ttu-id="b2e8d-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7) </span><span class="sxs-lookup"><span data-stu-id="b2e8d-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-145">Bios。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-145">BIOS.</span></span>

</dd> <dt>

<span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>

<span data-ttu-id="b2e8d-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**開機 ROM** (8) </span><span class="sxs-lookup"><span data-stu-id="b2e8d-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**Boot ROM** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b2e8d-147">開機 ROM。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-147">Boot ROM.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b2e8d-148">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-148">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e8d-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b2e8d-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e8d-151">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ DeviceSoftware**.**目的**」 ) </span><span class="sxs-lookup"><span data-stu-id="b2e8d-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**Purpose**")</span></span>
</dt> </dl>

<span data-ttu-id="b2e8d-152">提供 **目的** 屬性詳細資訊的自由格式字串，例如「應用程式軟體」。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-152">Free-form string that provides more information for the **Purpose** property, for example, "Application Software".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2e8d-153">備註</span><span class="sxs-lookup"><span data-stu-id="b2e8d-153">Remarks</span></span>

<span data-ttu-id="b2e8d-154">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-154">WMI does not implement this class.</span></span>

<span data-ttu-id="b2e8d-155">**Cim \_ DeviceSoftware** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-155">The **CIM\_DeviceSoftware** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="b2e8d-156">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b2e8d-157">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b2e8d-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e8d-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2e8d-158">Requirements</span></span>



| <span data-ttu-id="b2e8d-159">需求</span><span class="sxs-lookup"><span data-stu-id="b2e8d-159">Requirement</span></span> | <span data-ttu-id="b2e8d-160">值</span><span class="sxs-lookup"><span data-stu-id="b2e8d-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e8d-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2e8d-161">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e8d-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2e8d-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b2e8d-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2e8d-163">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e8d-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2e8d-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b2e8d-165">命名空間</span><span class="sxs-lookup"><span data-stu-id="b2e8d-165">Namespace</span></span><br/>                | <span data-ttu-id="b2e8d-166">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b2e8d-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b2e8d-167">MOF</span><span class="sxs-lookup"><span data-stu-id="b2e8d-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2e8d-168"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2e8d-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2e8d-169">DLL</span><span class="sxs-lookup"><span data-stu-id="b2e8d-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2e8d-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2e8d-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e8d-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2e8d-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e8d-172">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="b2e8d-172">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

