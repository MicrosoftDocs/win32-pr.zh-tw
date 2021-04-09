---
description: CIM \_ UnitaryComputerSystem 類別代表桌上型電腦、行動裝置、網路電腦、伺服器或其他類型的單一節點電腦系統。
ms.assetid: c696050d-c921-4056-adc7-e4a2e9f4e119
ms.tgt_platform: multiple
title: CIM_UnitaryComputerSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem
- CIM_UnitaryComputerSystem.Caption
- CIM_UnitaryComputerSystem.CreationClassName
- CIM_UnitaryComputerSystem.Description
- CIM_UnitaryComputerSystem.InitialLoadInfo
- CIM_UnitaryComputerSystem.InstallDate
- CIM_UnitaryComputerSystem.LastLoadInfo
- CIM_UnitaryComputerSystem.Name
- CIM_UnitaryComputerSystem.NameFormat
- CIM_UnitaryComputerSystem.PowerManagementCapabilities
- CIM_UnitaryComputerSystem.PowerManagementSupported
- CIM_UnitaryComputerSystem.PowerState
- CIM_UnitaryComputerSystem.PrimaryOwnerContact
- CIM_UnitaryComputerSystem.PrimaryOwnerName
- CIM_UnitaryComputerSystem.ResetCapability
- CIM_UnitaryComputerSystem.Roles
- CIM_UnitaryComputerSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e14812fda7971ffe045e8e36752c983cf5350402
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936150"
---
# <a name="cim_unitarycomputersystem-class"></a><span data-ttu-id="b7141-103">CIM \_ UnitaryComputerSystem 類別</span><span class="sxs-lookup"><span data-stu-id="b7141-103">CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="b7141-104">**CIM \_ UnitaryComputerSystem** 類別代表桌上型電腦、行動裝置、網路電腦、伺服器或其他類型的單一節點電腦系統。</span><span class="sxs-lookup"><span data-stu-id="b7141-104">The **CIM\_UnitaryComputerSystem** class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7141-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="b7141-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b7141-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="b7141-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b7141-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b7141-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b7141-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b7141-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7141-109">語法</span><span class="sxs-lookup"><span data-stu-id="b7141-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C526-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UnitaryComputerSystem : CIM_ComputerSystem
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  string   InitialLoadInfo[];
  datetime InstallDate;
  string   LastLoadInfo;
  string   Name;
  string   NameFormat;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  string   Roles[];
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="b7141-110">成員</span><span class="sxs-lookup"><span data-stu-id="b7141-110">Members</span></span>

<span data-ttu-id="b7141-111">**CIM \_ UnitaryComputerSystem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b7141-111">The **CIM\_UnitaryComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="b7141-112">方法</span><span class="sxs-lookup"><span data-stu-id="b7141-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b7141-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b7141-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b7141-114">方法</span><span class="sxs-lookup"><span data-stu-id="b7141-114">Methods</span></span>

<span data-ttu-id="b7141-115">**CIM \_ UnitaryComputerSystem** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b7141-115">The **CIM\_UnitaryComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="b7141-116">方法</span><span class="sxs-lookup"><span data-stu-id="b7141-116">Method</span></span>                                                                           | <span data-ttu-id="b7141-117">描述</span><span class="sxs-lookup"><span data-stu-id="b7141-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7141-118">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b7141-118">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md) | <span data-ttu-id="b7141-119">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="b7141-119">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b7141-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="b7141-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b7141-121">屬性</span><span class="sxs-lookup"><span data-stu-id="b7141-121">Properties</span></span>

<span data-ttu-id="b7141-122">**CIM \_ UnitaryComputerSystem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b7141-122">The **CIM\_UnitaryComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7141-123">**標題**</span><span class="sxs-lookup"><span data-stu-id="b7141-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b7141-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7141-126">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b7141-127">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="b7141-127">Short textual description of the object.</span></span>

<span data-ttu-id="b7141-128">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b7141-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7141-129">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b7141-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b7141-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7141-132">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7141-132">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7141-133">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7141-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b7141-134">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="b7141-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b7141-135">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="b7141-135">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7141-136">**說明**</span><span class="sxs-lookup"><span data-stu-id="b7141-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b7141-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7141-139">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b7141-140">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="b7141-140">Textual description of the object.</span></span>

<span data-ttu-id="b7141-141">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b7141-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7141-142">**InitialLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="b7141-142">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-143">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b7141-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b7141-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7141-145">找出初始載入裝置 (的資料) 或啟動服務要求作業系統啟動所需的資料。</span><span class="sxs-lookup"><span data-stu-id="b7141-145">Data needed to find either the initial load device (its key) or the boot service to request the operating system to start.</span></span> <span data-ttu-id="b7141-146">此外，載入參數 (也可以指定) 的路徑名稱和參數。</span><span class="sxs-lookup"><span data-stu-id="b7141-146">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="b7141-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b7141-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-148">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b7141-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7141-150">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="b7141-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b7141-151">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b7141-151">Date and time the object was installed.</span></span> <span data-ttu-id="b7141-152">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="b7141-152">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b7141-153">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b7141-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7141-154">**LastLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="b7141-154">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b7141-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7141-157">識別初始載入裝置 (其金鑰) 或要求最後作業系統載入的開機服務的資料。</span><span class="sxs-lookup"><span data-stu-id="b7141-157">Data that identifies either the initial load device (its key) or the boot service that requested the last operating system load.</span></span> <span data-ttu-id="b7141-158">此外，載入參數 (也可以指定) 的路徑名稱和參數。</span><span class="sxs-lookup"><span data-stu-id="b7141-158">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="b7141-159">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b7141-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b7141-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7141-162">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b7141-162">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b7141-163">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="b7141-163">Label by which the object is known.</span></span> <span data-ttu-id="b7141-164">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="b7141-164">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b7141-165">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b7141-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7141-166">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="b7141-166">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b7141-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7141-169">Cim 系統元件和其衍生物件是 CIM 的最上層物件，可提供許多元件的範圍，而且需要唯一的 [**cim \_ 系統**](cim-system.md)金鑰。 [**\_**](cim-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="b7141-169">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of CIM that provide the scope for numerous components and require unique [**CIM\_System**](cim-system.md) keys.</span></span> <span data-ttu-id="b7141-170">啟發學習法的定義是要在嘗試一律產生相同的系統名稱（與探索通訊協定無關）時，建立 CIM 的系統名稱。 **\_**</span><span class="sxs-lookup"><span data-stu-id="b7141-170">A heuristic is defined to create the **CIM\_ComputerSystem** name in an attempt to always generate the same system name, independent of discovery protocol.</span></span> <span data-ttu-id="b7141-171">這可防止清查和管理問題，也就是相同的資產或實體發現多次，但是無法解析成單一物件。</span><span class="sxs-lookup"><span data-stu-id="b7141-171">This prevents inventory and management problems where the same asset or entity is discovered multiple times, but cannot be resolved to a single object.</span></span> <span data-ttu-id="b7141-172">這個屬性會識別如何使用子類別啟發學習法來產生系統名稱。</span><span class="sxs-lookup"><span data-stu-id="b7141-172">This property identifies how the system name was generated by using the subclass heuristic.</span></span> <span data-ttu-id="b7141-173">啟發學習法會在 CIM V2 的一般模型規格中概述，並假設已記載的規則會經過決定並指派名稱。</span><span class="sxs-lookup"><span data-stu-id="b7141-173">The heuristic is outlined in the CIM V2 Common Model specification and assumes that the documented rules are traversed to determine and assign a name.</span></span> <span data-ttu-id="b7141-174">**NameFormat** 值清單會定義優先順序，以將多個規則對應指派給相同值的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="b7141-174">The **NameFormat** values list defines the precedence order for assigning the system name with several rules mapping to the same value.</span></span> <span data-ttu-id="b7141-175">請注意，使用啟發學習法計算的 **CIM \_** 程式名稱是系統的索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="b7141-175">Note that the **CIM\_ComputerSystem** name that is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="b7141-176">您可以使用別名來指派其他名稱，並將其用於更適合商務的 **CIM \_** 程式類型。</span><span class="sxs-lookup"><span data-stu-id="b7141-176">Other names can be assigned and used for the **CIM\_ComputerSystem** that better suit the business, using aliases.</span></span>

<span data-ttu-id="b7141-177">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="b7141-177">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="b7141-178">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="b7141-178">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="b7141-179">**Ip** ( 「ip」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-179">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="b7141-180">**撥號** ( 「撥號」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-180">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="b7141-181">**Hid** ( "hid" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-181">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="b7141-182">**NWA** ( "NWA" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-182">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="b7141-183">**HWA** ( "HWA" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-183">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="b7141-184">**X25** ( "x25" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-184">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="b7141-185">**Isdn** ( "isdn" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-185">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="b7141-186">**Ipx** ( 「ipx」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-186">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="b7141-187">**DCC** ( "DCC" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-187">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="b7141-188">**Icd** ( 「icd」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-188">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="b7141-189">**E.** ( "e. 164" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-189">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="b7141-190">**Sna** ( 「sna」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-190">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="b7141-191">**Oid/osi** ( "OID/osi" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-191">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b7141-192">**其他** ( "其他" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-192">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b7141-193">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b7141-193">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-194">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b7141-194">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b7141-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7141-196">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統電源控制項 \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="b7141-196">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="b7141-197">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="b7141-197">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b7141-198">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="b7141-198">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b7141-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b7141-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b7141-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="b7141-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b7141-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="b7141-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b7141-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="b7141-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-203">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="b7141-203">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b7141-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="b7141-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-205">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="b7141-205">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b7141-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="b7141-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-207">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b7141-207">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b7141-208">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="b7141-208">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b7141-209">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="b7141-209">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b7141-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="b7141-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-211">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="b7141-211">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b7141-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="b7141-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-213">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="b7141-213">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b7141-214">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b7141-214">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-215">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b7141-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7141-217">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="b7141-217">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b7141-218">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="b7141-218">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b7141-219">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="b7141-219">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b7141-220">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="b7141-220">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="b7141-221">**>powerstate**</span><span class="sxs-lookup"><span data-stu-id="b7141-221">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-222">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b7141-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7141-224">電腦系統的目前電源狀態及其相關聯的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b7141-224">Current power state of the computer system and its associated operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b7141-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b7141-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-226">不明。</span><span class="sxs-lookup"><span data-stu-id="b7141-226">Unknown.</span></span>

</dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="b7141-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1) </span><span class="sxs-lookup"><span data-stu-id="b7141-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-228">完整功能。</span><span class="sxs-lookup"><span data-stu-id="b7141-228">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b7141-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (2) </span><span class="sxs-lookup"><span data-stu-id="b7141-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-230">系統處於省電狀態，但仍正常運作，但效能可能會降低。</span><span class="sxs-lookup"><span data-stu-id="b7141-230">System is in a power-save state and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b7141-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (3) </span><span class="sxs-lookup"><span data-stu-id="b7141-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-232">系統無法正常運作，但可以快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="b7141-232">System is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b7141-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (4) </span><span class="sxs-lookup"><span data-stu-id="b7141-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-234">系統已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="b7141-234">System is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b7141-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**電源週期** (5) </span><span class="sxs-lookup"><span data-stu-id="b7141-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-236">電源週期。</span><span class="sxs-lookup"><span data-stu-id="b7141-236">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b7141-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (6) 的電源</span><span class="sxs-lookup"><span data-stu-id="b7141-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-238">關閉電源。</span><span class="sxs-lookup"><span data-stu-id="b7141-238">Power off.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b7141-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (7) </span><span class="sxs-lookup"><span data-stu-id="b7141-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-240">系統處於警告狀態，也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="b7141-240">System is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="b7141-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>省 **電-休眠** (8) </span><span class="sxs-lookup"><span data-stu-id="b7141-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-242">省電休眠。</span><span class="sxs-lookup"><span data-stu-id="b7141-242">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="b7141-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>省 **電-軟關閉** (9) </span><span class="sxs-lookup"><span data-stu-id="b7141-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="b7141-244">省電。</span><span class="sxs-lookup"><span data-stu-id="b7141-244">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b7141-245">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="b7141-245">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b7141-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7141-248">提供有關如何聯繫主要系統擁有者的資訊 (例如電話號碼、電子郵件地址等等) 。</span><span class="sxs-lookup"><span data-stu-id="b7141-248">String that provides information on how to reach the primary system owner (for example, phone number, email address, and so on).</span></span>

<span data-ttu-id="b7141-249">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="b7141-249">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7141-250">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="b7141-250">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b7141-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7141-253">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="b7141-253">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b7141-254">主要系統擁有者的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7141-254">Name of the primary system owner.</span></span>

<span data-ttu-id="b7141-255">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="b7141-255">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7141-256">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="b7141-256">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-257">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b7141-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7141-259">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統硬體安全性 \| 001.4」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="b7141-260">如果啟用，則可以使用硬體 (來重設單一電腦系統，例如，具有 [電源] 和 [重設] 按鈕) 。</span><span class="sxs-lookup"><span data-stu-id="b7141-260">If enabled, the unitary computer system can be reset with hardware (for example, with the power and reset buttons).</span></span> <span data-ttu-id="b7141-261">如果停用，則不允許硬體重設。</span><span class="sxs-lookup"><span data-stu-id="b7141-261">If disabled, hardware reset is not allowed.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b7141-262">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b7141-262">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b7141-263">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="b7141-263">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b7141-264">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="b7141-264">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b7141-265">**已啟用** (4) </span><span class="sxs-lookup"><span data-stu-id="b7141-265">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="b7141-266">**未執行** (5) </span><span class="sxs-lookup"><span data-stu-id="b7141-266">**Not Implemented** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b7141-267">**角色**</span><span class="sxs-lookup"><span data-stu-id="b7141-267">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-268">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b7141-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b7141-269">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b7141-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b7141-270">系統在資訊技術環境中扮演的角色。</span><span class="sxs-lookup"><span data-stu-id="b7141-270">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="b7141-271">系統的子類別可以覆寫這個屬性，以定義明確的角色值。</span><span class="sxs-lookup"><span data-stu-id="b7141-271">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="b7141-272">或者，工作群組也可以描述指定角色的啟發學習法、慣例和指導方針。</span><span class="sxs-lookup"><span data-stu-id="b7141-272">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="b7141-273">例如，如果是網路系統的實例，這個屬性可能會包含 "Switch" 或 "Bridge" 字串。</span><span class="sxs-lookup"><span data-stu-id="b7141-273">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="b7141-274">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="b7141-274">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7141-275">**狀態**</span><span class="sxs-lookup"><span data-stu-id="b7141-275">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7141-276">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b7141-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7141-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7141-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7141-278">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-278">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b7141-279">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b7141-279">Current status of the object.</span></span> <span data-ttu-id="b7141-280">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b7141-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b7141-281">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="b7141-281">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b7141-282">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="b7141-282">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b7141-283">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-283">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b7141-284">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-284">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b7141-285">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-285">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b7141-286">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-286">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b7141-287">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-287">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b7141-288">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-288">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b7141-289">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-289">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b7141-290">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-290">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b7141-291">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="b7141-291">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b7141-292">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-292">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b7141-293">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="b7141-293">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="b7141-294"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b7141-294"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b7141-295">備註</span><span class="sxs-lookup"><span data-stu-id="b7141-295">Remarks</span></span>

<span data-ttu-id="b7141-296">**Cim \_ UnitaryComputerSystem** 類別衍生自 cim 的 [**\_ 程式**](cim-computersystem.md)類型。</span><span class="sxs-lookup"><span data-stu-id="b7141-296">The **CIM\_UnitaryComputerSystem** class is derived from [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="b7141-297">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="b7141-297">WMI does not implement this class.</span></span> <span data-ttu-id="b7141-298">針對衍生自 **CIM \_ UNITARYCOMPUTERSYSTEM** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="b7141-298">For WMI classes derived from **CIM\_UnitaryComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b7141-299">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="b7141-299">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b7141-300">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b7141-300">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7141-301">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7141-301">Requirements</span></span>



| <span data-ttu-id="b7141-302">需求</span><span class="sxs-lookup"><span data-stu-id="b7141-302">Requirement</span></span> | <span data-ttu-id="b7141-303">值</span><span class="sxs-lookup"><span data-stu-id="b7141-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7141-304">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7141-304">Minimum supported client</span></span><br/> | <span data-ttu-id="b7141-305">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7141-305">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7141-306">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7141-306">Minimum supported server</span></span><br/> | <span data-ttu-id="b7141-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7141-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7141-308">命名空間</span><span class="sxs-lookup"><span data-stu-id="b7141-308">Namespace</span></span><br/>                | <span data-ttu-id="b7141-309">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b7141-309">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b7141-310">MOF</span><span class="sxs-lookup"><span data-stu-id="b7141-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7141-311"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7141-311"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7141-312">DLL</span><span class="sxs-lookup"><span data-stu-id="b7141-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7141-313"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7141-313"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7141-314">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7141-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7141-315">**CIM \_ 未進行**</span><span class="sxs-lookup"><span data-stu-id="b7141-315">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

