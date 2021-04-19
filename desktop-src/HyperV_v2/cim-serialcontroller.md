---
description: 描述序列控制器的功能和管理。
ms.assetid: ce3e0424-4ab8-435d-a155-1164535b3b0d
title: 'CIM_SerialController 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a2e69bab38bb8b68c15ed93b2bee721c35a7600
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972070"
---
# <a name="cim_serialcontroller-class-hyper-v-management"></a><span data-ttu-id="9df31-103">CIM_SerialController 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="9df31-103">CIM_SerialController class (Hyper-V management)</span></span>

<span data-ttu-id="9df31-104">描述序列控制器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="9df31-104">Describes the capabilities and management of a serial controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="9df31-105">語法</span><span class="sxs-lookup"><span data-stu-id="9df31-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_SerialController : CIM_Controller
{
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint32 MaxBaudRate;
  uint16 Security;
};
```

## <a name="members"></a><span data-ttu-id="9df31-106">成員</span><span class="sxs-lookup"><span data-stu-id="9df31-106">Members</span></span>

<span data-ttu-id="9df31-107">**CIM \_ SerialController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9df31-107">The **CIM\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="9df31-108">屬性</span><span class="sxs-lookup"><span data-stu-id="9df31-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9df31-109">屬性</span><span class="sxs-lookup"><span data-stu-id="9df31-109">Properties</span></span>

<span data-ttu-id="9df31-110">**CIM \_ SerialController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9df31-110">The **CIM\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9df31-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="9df31-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df31-112">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9df31-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9df31-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9df31-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9df31-114">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 序列埠 \| 004.7 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="9df31-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="9df31-115">序列控制器的晶片層級相容性。</span><span class="sxs-lookup"><span data-stu-id="9df31-115">The chip level compatibility for the serial controller.</span></span> <span data-ttu-id="9df31-116">此屬性描述可能在晶片硬體中固有之序列控制器的緩衝和其他功能。</span><span class="sxs-lookup"><span data-stu-id="9df31-116">This property describes the buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9df31-117">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="9df31-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9df31-118">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="9df31-118">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="9df31-119">**XT/相容** (3) </span><span class="sxs-lookup"><span data-stu-id="9df31-119">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="9df31-120">**16450 相容** (4) </span><span class="sxs-lookup"><span data-stu-id="9df31-120">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="9df31-121">**16550 相容** (5) </span><span class="sxs-lookup"><span data-stu-id="9df31-121">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="9df31-122">**16550A 相容** (6) </span><span class="sxs-lookup"><span data-stu-id="9df31-122">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="9df31-123">**8251 相容** (160) </span><span class="sxs-lookup"><span data-stu-id="9df31-123">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="9df31-124">**8251FIFO 相容** (161) </span><span class="sxs-lookup"><span data-stu-id="9df31-124">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9df31-125">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9df31-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df31-126">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9df31-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9df31-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9df31-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9df31-128">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ SerialController**。**功能**") </span><span class="sxs-lookup"><span data-stu-id="9df31-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="9df31-129">陣列，其中包含 **功能** 陣列中序列控制器功能的更詳細說明。</span><span class="sxs-lookup"><span data-stu-id="9df31-129">An array that contains more detailed explanations for serial controller features in the **Capabilities** array.</span></span> <span data-ttu-id="9df31-130">**CapabilityDescriptions** 陣列中的專案與 **功能** 陣列中的專案相互關聯。</span><span class="sxs-lookup"><span data-stu-id="9df31-130">The items in the **CapabilityDescriptions** array correlate to those in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="9df31-131">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="9df31-131">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df31-132">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9df31-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9df31-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9df31-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9df31-134">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 序列埠 \| 004.6 ") ， **PUnit** (" bit/second ") </span><span class="sxs-lookup"><span data-stu-id="9df31-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.6"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="9df31-135">序列控制器支援的最大傳輸速率（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="9df31-135">The maximum baud rate in, bits per second, that is supported by the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="9df31-136">**安全性**</span><span class="sxs-lookup"><span data-stu-id="9df31-136">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df31-137">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9df31-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9df31-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9df31-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9df31-139">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 序列埠 \| 004.9 ") </span><span class="sxs-lookup"><span data-stu-id="9df31-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="9df31-140">控制器的操作安全性。</span><span class="sxs-lookup"><span data-stu-id="9df31-140">The operational security for the controller.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9df31-141">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="9df31-141">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9df31-142">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="9df31-142">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="9df31-143">**無** (3) </span><span class="sxs-lookup"><span data-stu-id="9df31-143">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Locked_Out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="9df31-144">**外部介面被鎖定** (4) </span><span class="sxs-lookup"><span data-stu-id="9df31-144">**External Interface Locked Out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="9df31-145">**已啟用外部介面** (5) </span><span class="sxs-lookup"><span data-stu-id="9df31-145">**External Interface Enabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="9df31-146">**開機略過** (6) </span><span class="sxs-lookup"><span data-stu-id="9df31-146">**Boot Bypass** (6)</span></span>


<span data-ttu-id="9df31-147"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9df31-147"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="9df31-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="9df31-148">Requirements</span></span>



| <span data-ttu-id="9df31-149">需求</span><span class="sxs-lookup"><span data-stu-id="9df31-149">Requirement</span></span> | <span data-ttu-id="9df31-150">值</span><span class="sxs-lookup"><span data-stu-id="9df31-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9df31-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9df31-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9df31-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9df31-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9df31-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9df31-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9df31-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9df31-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9df31-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="9df31-155">Namespace</span></span><br/>                | <span data-ttu-id="9df31-156">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="9df31-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9df31-157">MOF</span><span class="sxs-lookup"><span data-stu-id="9df31-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9df31-158"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9df31-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9df31-159">DLL</span><span class="sxs-lookup"><span data-stu-id="9df31-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9df31-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9df31-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9df31-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9df31-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9df31-162">**CIM \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="9df31-162">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

