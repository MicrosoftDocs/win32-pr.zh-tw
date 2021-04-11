---
description: CIM \_ SerialInterface 類別代表 cim \_ ControlledBy 關聯性，指出哪些裝置可透過序列控制器存取，以及存取的特性。
ms.assetid: bebc304a-c2b7-41c7-b24a-8f450ee3c4bb
ms.tgt_platform: multiple
title: CIM_SerialInterface 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialInterface
- CIM_SerialInterface.NegotiatedDataWidth
- CIM_SerialInterface.NegotiatedSpeed
- CIM_SerialInterface.AccessState
- CIM_SerialInterface.NumberOfHardResets
- CIM_SerialInterface.NumberOfSoftResets
- CIM_SerialInterface.Dependent
- CIM_SerialInterface.Antecedent
- CIM_SerialInterface.FlowControlInfo
- CIM_SerialInterface.NumberOfStopBits
- CIM_SerialInterface.ParityInfo
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1df787ff64798f412035a72e6db6d7b01b4b9b0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847244"
---
# <a name="cim_serialinterface-class"></a><span data-ttu-id="267fd-103">CIM \_ SerialInterface 類別</span><span class="sxs-lookup"><span data-stu-id="267fd-103">CIM\_SerialInterface class</span></span>

<span data-ttu-id="267fd-104">**Cim \_ SerialInterface** 類別代表 [**cim \_ ControlledBy**](cim-controlledby.md)關聯性，指出哪些裝置可透過序列控制器存取，以及存取的特性。</span><span class="sxs-lookup"><span data-stu-id="267fd-104">The **CIM\_SerialInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="267fd-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="267fd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="267fd-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="267fd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="267fd-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="267fd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="267fd-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="267fd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="267fd-109">語法</span><span class="sxs-lookup"><span data-stu-id="267fd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8B309BDA-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SerialInterface : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  CIM_LogicalDevice    REF Dependent;
  CIM_SerialController REF Antecedent;
  uint16                   FlowControlInfo;
  uint16                   NumberOfStopBits;
  uint16                   ParityInfo;
};
```

## <a name="members"></a><span data-ttu-id="267fd-110">成員</span><span class="sxs-lookup"><span data-stu-id="267fd-110">Members</span></span>

<span data-ttu-id="267fd-111">**CIM \_ SerialInterface** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="267fd-111">The **CIM\_SerialInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="267fd-112">屬性</span><span class="sxs-lookup"><span data-stu-id="267fd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="267fd-113">屬性</span><span class="sxs-lookup"><span data-stu-id="267fd-113">Properties</span></span>

<span data-ttu-id="267fd-114">**CIM \_ SerialInterface** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="267fd-114">The **CIM\_SerialInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="267fd-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="267fd-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="267fd-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="267fd-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="267fd-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="267fd-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="267fd-118">指出控制器是否正在主動命令或存取裝置。</span><span class="sxs-lookup"><span data-stu-id="267fd-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="267fd-119">當邏輯裝置可透過多個控制器來發出或存取時，這項資訊是必要的。</span><span class="sxs-lookup"><span data-stu-id="267fd-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="267fd-120">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="267fd-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="267fd-121">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="267fd-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="267fd-122">**Active** (1) </span><span class="sxs-lookup"><span data-stu-id="267fd-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="267fd-123">**非** 使用中 (2) </span><span class="sxs-lookup"><span data-stu-id="267fd-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="267fd-124">**先行**</span><span class="sxs-lookup"><span data-stu-id="267fd-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="267fd-125">資料類型： **CIM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="267fd-125">Data type: **CIM\_SerialController**</span></span>
</dt> <dt>

<span data-ttu-id="267fd-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="267fd-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="267fd-127">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="267fd-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="267fd-128">描述序列控制器的 [**CIM \_ SerialController**](cim-serialcontroller.md) 。</span><span class="sxs-lookup"><span data-stu-id="267fd-128">A [**CIM\_SerialController**](cim-serialcontroller.md) that describes the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="267fd-129">**依賴**</span><span class="sxs-lookup"><span data-stu-id="267fd-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="267fd-130">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="267fd-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="267fd-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="267fd-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="267fd-132">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="267fd-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="267fd-133">描述邏輯裝置的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="267fd-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="267fd-134">**FlowControlInfo**</span><span class="sxs-lookup"><span data-stu-id="267fd-134">**FlowControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="267fd-135">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="267fd-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="267fd-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="267fd-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="267fd-137">表示傳輸資料的流程式控制制。</span><span class="sxs-lookup"><span data-stu-id="267fd-137">Indicates the flow control for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="267fd-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="267fd-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="267fd-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="267fd-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="267fd-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (2) </span><span class="sxs-lookup"><span data-stu-id="267fd-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>

<span data-ttu-id="267fd-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XonXoff** (3) </span><span class="sxs-lookup"><span data-stu-id="267fd-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XonXoff** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="RTS_CTS"></span><span id="rts_cts"></span>

<span data-ttu-id="267fd-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4) </span><span class="sxs-lookup"><span data-stu-id="267fd-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>

<span data-ttu-id="267fd-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**XonXoff 和 RTS/CTS** (5) </span><span class="sxs-lookup"><span data-stu-id="267fd-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**Both XonXoff and RTS/CTS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="267fd-144">XonXoff 和 RTS/CTS</span><span class="sxs-lookup"><span data-stu-id="267fd-144">XonXoff and RTS/CTS</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="267fd-145">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="267fd-145">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="267fd-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="267fd-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="267fd-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="267fd-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="267fd-148">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="267fd-148">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="267fd-149">當有數個匯流排或連接資料寬度時，此屬性會定義裝置之間使用的資料寬度。</span><span class="sxs-lookup"><span data-stu-id="267fd-149">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="267fd-150">資料寬度的指定單位為位。</span><span class="sxs-lookup"><span data-stu-id="267fd-150">Data width is specified in bits.</span></span> <span data-ttu-id="267fd-151">如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="267fd-151">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="267fd-152">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="267fd-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="267fd-153">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="267fd-153">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="267fd-154">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="267fd-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="267fd-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="267fd-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="267fd-156">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="267fd-156">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="267fd-157">當可能有數個匯流排或連線速度時，此屬性會定義要在裝置之間使用的速率。</span><span class="sxs-lookup"><span data-stu-id="267fd-157">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="267fd-158">以每秒位數指定速度。</span><span class="sxs-lookup"><span data-stu-id="267fd-158">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="267fd-159">如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="267fd-159">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="267fd-160">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="267fd-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="267fd-161">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="267fd-161">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="267fd-162">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="267fd-162">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="267fd-163">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="267fd-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="267fd-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="267fd-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="267fd-165">控制器發出的硬重設數目。</span><span class="sxs-lookup"><span data-stu-id="267fd-165">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="267fd-166">硬重設會將裝置傳回到其初始化或啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="267fd-166">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="267fd-167">所有內部裝置狀態資訊和資料都會遺失。</span><span class="sxs-lookup"><span data-stu-id="267fd-167">All internal device state information and data are lost.</span></span>

<span data-ttu-id="267fd-168">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="267fd-168">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="267fd-169">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="267fd-169">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="267fd-170">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="267fd-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="267fd-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="267fd-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="267fd-172">控制器發出的軟重設數目。</span><span class="sxs-lookup"><span data-stu-id="267fd-172">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="267fd-173">軟重設並不會完全清除目前的裝置狀態和資料。</span><span class="sxs-lookup"><span data-stu-id="267fd-173">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="267fd-174">確切的語法取決於裝置，以及用來與其通訊的通訊協定和機制。</span><span class="sxs-lookup"><span data-stu-id="267fd-174">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="267fd-175">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="267fd-175">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="267fd-176">**NumberOfStopBits**</span><span class="sxs-lookup"><span data-stu-id="267fd-176">**NumberOfStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="267fd-177">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="267fd-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="267fd-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="267fd-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="267fd-179">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="267fd-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="267fd-180">要傳輸的停止位數目。</span><span class="sxs-lookup"><span data-stu-id="267fd-180">Number of stop bits to transmit.</span></span>

</dd> <dt>

<span data-ttu-id="267fd-181">**ParityInfo**</span><span class="sxs-lookup"><span data-stu-id="267fd-181">**ParityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="267fd-182">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="267fd-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="267fd-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="267fd-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="267fd-184">有關傳輸資料的同位設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="267fd-184">Information about the parity setting for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="267fd-185">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="267fd-185">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="267fd-186">**無** (1) </span><span class="sxs-lookup"><span data-stu-id="267fd-186">**None** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="267fd-187">**甚至** (2) </span><span class="sxs-lookup"><span data-stu-id="267fd-187">**Even** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="267fd-188">**奇數** (3) </span><span class="sxs-lookup"><span data-stu-id="267fd-188">**Odd** (3)</span></span>


<span data-ttu-id="267fd-189"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="267fd-189"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="267fd-190">備註</span><span class="sxs-lookup"><span data-stu-id="267fd-190">Remarks</span></span>

<span data-ttu-id="267fd-191">**Cim \_ SerialInterface** 類別衍生自 [**cim \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="267fd-191">The **CIM\_SerialInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="267fd-192">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="267fd-192">WMI does not implement this class.</span></span>

<span data-ttu-id="267fd-193">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="267fd-193">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="267fd-194">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="267fd-194">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="267fd-195">規格需求</span><span class="sxs-lookup"><span data-stu-id="267fd-195">Requirements</span></span>



| <span data-ttu-id="267fd-196">需求</span><span class="sxs-lookup"><span data-stu-id="267fd-196">Requirement</span></span> | <span data-ttu-id="267fd-197">值</span><span class="sxs-lookup"><span data-stu-id="267fd-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="267fd-198">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="267fd-198">Minimum supported client</span></span><br/> | <span data-ttu-id="267fd-199">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="267fd-199">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="267fd-200">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="267fd-200">Minimum supported server</span></span><br/> | <span data-ttu-id="267fd-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="267fd-201">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="267fd-202">命名空間</span><span class="sxs-lookup"><span data-stu-id="267fd-202">Namespace</span></span><br/>                | <span data-ttu-id="267fd-203">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="267fd-203">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="267fd-204">MOF</span><span class="sxs-lookup"><span data-stu-id="267fd-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="267fd-205"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="267fd-205"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="267fd-206">DLL</span><span class="sxs-lookup"><span data-stu-id="267fd-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="267fd-207"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="267fd-207"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="267fd-208">另請參閱</span><span class="sxs-lookup"><span data-stu-id="267fd-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="267fd-209">**CIM \_ ControlledBy**</span><span class="sxs-lookup"><span data-stu-id="267fd-209">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

