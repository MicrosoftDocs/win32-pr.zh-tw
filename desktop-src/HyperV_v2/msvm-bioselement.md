---
description: 代表載入 RAM 以設定及啟動系統的低層級軟體。
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Msvm_BIOSElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8d36ea50791bf6f1413815583fe1168f564d50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848289"
---
# <a name="msvm_bioselement-class"></a><span data-ttu-id="273c7-103">Msvm \_ BIOSElement 類別</span><span class="sxs-lookup"><span data-stu-id="273c7-103">Msvm\_BIOSElement class</span></span>

<span data-ttu-id="273c7-104">代表載入 RAM 以設定及啟動系統的低層級軟體。</span><span class="sxs-lookup"><span data-stu-id="273c7-104">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span> <span data-ttu-id="273c7-105">BIOS 不是邏輯裝置，因此不應該將虛擬 BIOS 視為虛擬機器裝置。</span><span class="sxs-lookup"><span data-stu-id="273c7-105">The BIOS is not a logical device, hence the virtual BIOS should not be thought of as a virtual machine device.</span></span> <span data-ttu-id="273c7-106">因為它不是裝置，所以沒有對應的資源集區。</span><span class="sxs-lookup"><span data-stu-id="273c7-106">As it is not a device, it does not have a corresponding resource pool.</span></span> <span data-ttu-id="273c7-107">BIOS 物件透過 [**Msvm \_ SystemBIOS**](msvm-systembios.md) 關聯與虛擬機器相關聯。</span><span class="sxs-lookup"><span data-stu-id="273c7-107">The BIOS object is associated with the virtual machine through the [**Msvm\_SystemBIOS**](msvm-systembios.md) association.</span></span>

<span data-ttu-id="273c7-108">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="273c7-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="273c7-109">語法</span><span class="sxs-lookup"><span data-stu-id="273c7-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a><span data-ttu-id="273c7-110">成員</span><span class="sxs-lookup"><span data-stu-id="273c7-110">Members</span></span>

<span data-ttu-id="273c7-111">**Msvm \_ BIOSElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="273c7-111">The **Msvm\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="273c7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="273c7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="273c7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="273c7-113">Properties</span></span>

<span data-ttu-id="273c7-114">**Msvm \_ BIOSElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="273c7-114">The **Msvm\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="273c7-115">**BaseBoardSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="273c7-115">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-118">虛擬機器上基本板的序號。</span><span class="sxs-lookup"><span data-stu-id="273c7-118">The serial number for the base board on the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-119">**BIOSGUID**</span><span class="sxs-lookup"><span data-stu-id="273c7-119">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-122">BIOS 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="273c7-122">The unique identifier for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-123">**BIOSNumLock**</span><span class="sxs-lookup"><span data-stu-id="273c7-123">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-124">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="273c7-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-126">BIOS 中 Num Lock 的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="273c7-126">The enabled state of the Num Lock in the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-127">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="273c7-127">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-130">BIOS 的序號。</span><span class="sxs-lookup"><span data-stu-id="273c7-130">The serial number for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-131">**BootOrder**</span><span class="sxs-lookup"><span data-stu-id="273c7-131">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-132">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="273c7-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="273c7-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-134">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (4) </span><span class="sxs-lookup"><span data-stu-id="273c7-134">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="273c7-135">裝置將在啟動時搜尋開機磁區的順序。</span><span class="sxs-lookup"><span data-stu-id="273c7-135">The order in which devices will be searched for a boot sector at startup.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-136">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="273c7-136">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-139">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="273c7-139">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="273c7-140">此軟體專案編譯的內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="273c7-140">The internal identifier for this compilation of software element.</span></span> <span data-ttu-id="273c7-141">這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，而且一律設定為14。</span><span class="sxs-lookup"><span data-stu-id="273c7-141">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 14.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-142">**標題**</span><span class="sxs-lookup"><span data-stu-id="273c7-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-145">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="273c7-145">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="273c7-146">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="273c7-146">A short description of the object.</span></span> <span data-ttu-id="273c7-147">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-148">**ChassisAssetTag**</span><span class="sxs-lookup"><span data-stu-id="273c7-148">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-151">建立虛擬機器時，會自動填入 BIOS。</span><span class="sxs-lookup"><span data-stu-id="273c7-151">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-152">**ChassisSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="273c7-152">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-155">建立虛擬機器時，會自動填入 BIOS。</span><span class="sxs-lookup"><span data-stu-id="273c7-155">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-156">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="273c7-156">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-159">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="273c7-159">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="273c7-160">Software 元素所使用的程式碼集。</span><span class="sxs-lookup"><span data-stu-id="273c7-160">The code set used by the software element.</span></span> <span data-ttu-id="273c7-161">這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="273c7-161">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="273c7-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-163">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="273c7-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-165">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="273c7-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="273c7-166">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="273c7-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="273c7-167">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-168">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="273c7-168">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-171">BIOS 目前選取的語言。</span><span class="sxs-lookup"><span data-stu-id="273c7-171">The currently selected language for the BIOS.</span></span> <span data-ttu-id="273c7-172">這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為 "en-us \| US \| iso8859-1"。</span><span class="sxs-lookup"><span data-stu-id="273c7-172">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="273c7-173">**說明**</span><span class="sxs-lookup"><span data-stu-id="273c7-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-176">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="273c7-176">A description of the object.</span></span> <span data-ttu-id="273c7-177">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="273c7-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-179">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="273c7-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-181">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="273c7-181">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="273c7-182">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="273c7-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="273c7-183">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="273c7-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-187">元素的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="273c7-187">A display name for the element.</span></span> <span data-ttu-id="273c7-188">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="273c7-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-190">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="273c7-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-192">指定元素目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="273c7-192">Specifies the current health of the element.</span></span> <span data-ttu-id="273c7-193">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="273c7-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="273c7-194">發生重大錯誤時，請檢查事件記錄檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="273c7-194">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="273c7-195">**EnabledState** 屬性也可以包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="273c7-195">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="273c7-196">例如，當磁碟空間不足時， **HealthState** 會設定為25、虛擬機器暫停，而 **EnabledState** 設定為 32768 (暫停) 。</span><span class="sxs-lookup"><span data-stu-id="273c7-196">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="273c7-197">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="273c7-198">值</span><span class="sxs-lookup"><span data-stu-id="273c7-198">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="273c7-199">意義</span><span class="sxs-lookup"><span data-stu-id="273c7-199">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="273c7-200"><dt>**確定**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-200"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="273c7-201">虛擬機器完全正常運作，且在正常指令引數內運作，而且沒有錯誤。</span><span class="sxs-lookup"><span data-stu-id="273c7-201">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="273c7-202"><dt>**重大失敗**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-202"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="273c7-203">虛擬機器發生重大故障。</span><span class="sxs-lookup"><span data-stu-id="273c7-203">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="273c7-204">當包含虛擬機器 Vhd 的一或多個磁片的磁碟空間不足，且虛擬機器已暫停時，就會使用此值。</span><span class="sxs-lookup"><span data-stu-id="273c7-204">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="273c7-205"><dt>**重大失敗**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-205"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="273c7-206">元素沒有作用，而且可能無法復原。</span><span class="sxs-lookup"><span data-stu-id="273c7-206">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="273c7-207">這可能表示虛擬機器 (Vmwp.exe) 的工作者進程沒有回應控制或資訊要求，或是包含虛擬機器 Vhd 的一或多個磁片磁碟空間不足。</span><span class="sxs-lookup"><span data-stu-id="273c7-207">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="273c7-208">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="273c7-208">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-209">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-211">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="273c7-211">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="273c7-212">此軟體元素的製造商識別碼。</span><span class="sxs-lookup"><span data-stu-id="273c7-212">The manufacturer's identifier for this software element.</span></span> <span data-ttu-id="273c7-213">通常這會是 (SKU) 或元件編號的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="273c7-213">Often this will be a stock keeping unit (SKU) or a part number.</span></span> <span data-ttu-id="273c7-214">這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="273c7-214">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="273c7-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-216">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="273c7-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-218">建立虛擬機器時，會自動填入 BIOS。</span><span class="sxs-lookup"><span data-stu-id="273c7-218">Automatically populated by the BIOS when the virtual machine is created.</span></span> <span data-ttu-id="273c7-219">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-220">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="273c7-220">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-223">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="273c7-223">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="273c7-224">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="273c7-224">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="273c7-225">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-226">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="273c7-226">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-229">限定詞： **MaxLen** (32) </span><span class="sxs-lookup"><span data-stu-id="273c7-229">Qualifiers: **MaxLen** (32)</span></span>
</dt> </dl>

<span data-ttu-id="273c7-230">此軟體元素的語言版本。</span><span class="sxs-lookup"><span data-stu-id="273c7-230">The language edition of this software element.</span></span> <span data-ttu-id="273c7-231">這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="273c7-231">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-232">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="273c7-232">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-233">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="273c7-233">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="273c7-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-235">適用于 BIOS 的可安裝語言清單。</span><span class="sxs-lookup"><span data-stu-id="273c7-235">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="273c7-236">這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為 "en-us \| US \| iso8859-1"。</span><span class="sxs-lookup"><span data-stu-id="273c7-236">THIS property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="273c7-237">**LoadedEndingAddress**</span><span class="sxs-lookup"><span data-stu-id="273c7-237">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-238">資料類型： **unit64**</span><span class="sxs-lookup"><span data-stu-id="273c7-238">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-240">此 BIOS 所佔用記憶體的結束位址。</span><span class="sxs-lookup"><span data-stu-id="273c7-240">The ending address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="273c7-241">這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為0xFFFFF。</span><span class="sxs-lookup"><span data-stu-id="273c7-241">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-242">**LoadedStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="273c7-242">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-243">資料類型： **unit64**</span><span class="sxs-lookup"><span data-stu-id="273c7-243">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-245">此 BIOS 所佔用記憶體的起始位址。</span><span class="sxs-lookup"><span data-stu-id="273c7-245">The starting address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="273c7-246">這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為0xE0000。</span><span class="sxs-lookup"><span data-stu-id="273c7-246">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xE0000.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-247">**LoadUtilityInformation**</span><span class="sxs-lookup"><span data-stu-id="273c7-247">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-248">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-250">描述更新 BIOS 元素所需的 BIOS flash/load 公用程式字串。</span><span class="sxs-lookup"><span data-stu-id="273c7-250">A string that describes the BIOS flash/load utility that is required to update the BIOS element.</span></span> <span data-ttu-id="273c7-251">版本和其他資訊可能會顯示在此屬性中。</span><span class="sxs-lookup"><span data-stu-id="273c7-251">Version and other information may be indicated in this property.</span></span> <span data-ttu-id="273c7-252">這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="273c7-252">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-253">**製造商**</span><span class="sxs-lookup"><span data-stu-id="273c7-253">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-254">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-256">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="273c7-256">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="273c7-257">此 BIOS 的製造商。</span><span class="sxs-lookup"><span data-stu-id="273c7-257">The manufacturer of this BIOS.</span></span> <span data-ttu-id="273c7-258">這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為 "Microsoft Corporation"。</span><span class="sxs-lookup"><span data-stu-id="273c7-258">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="273c7-259">**名稱**</span><span class="sxs-lookup"><span data-stu-id="273c7-259">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-260">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-262">限定詞： **MaxLen** (1024) </span><span class="sxs-lookup"><span data-stu-id="273c7-262">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="273c7-263">用來識別此軟體元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="273c7-263">The name used to identify this software element.</span></span> <span data-ttu-id="273c7-264">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="273c7-264">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="273c7-265">這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，一律設為 "BIOS"。</span><span class="sxs-lookup"><span data-stu-id="273c7-265">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "BIOS".</span></span>

</dd> <dt>

<span data-ttu-id="273c7-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="273c7-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-267">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="273c7-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-269">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="273c7-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="273c7-270">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="273c7-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="273c7-271">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-272">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="273c7-272">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-273">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="273c7-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="273c7-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-275">陣列，其中包含物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="273c7-275">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="273c7-276">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="273c7-277">位於索引零 (0) 的值是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="273c7-277">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="273c7-278">值</span><span class="sxs-lookup"><span data-stu-id="273c7-278">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="273c7-279">意義</span><span class="sxs-lookup"><span data-stu-id="273c7-279">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="273c7-280"><dt>**確定**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-280"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="273c7-281">虛擬機器正常運作，且正常運作。</span><span class="sxs-lookup"><span data-stu-id="273c7-281">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="273c7-282"><dt>**降級**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-282"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="273c7-283">虛擬機器只能部分運作。</span><span class="sxs-lookup"><span data-stu-id="273c7-283">The virtual machine is only partially functional.</span></span> <span data-ttu-id="273c7-284">這表示無法存取包含設定的儲存體。</span><span class="sxs-lookup"><span data-stu-id="273c7-284">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="273c7-285">處於此狀態的虛擬機器只可關閉或刪除。</span><span class="sxs-lookup"><span data-stu-id="273c7-285">A virtual machine in this state may only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="273c7-286"><dt>**預測性失敗**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-286"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="273c7-287">虛擬機器可正常運作，但未來可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="273c7-287">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="273c7-288">這表示包含虛擬機器虛擬硬碟的存放裝置可用空間不足。</span><span class="sxs-lookup"><span data-stu-id="273c7-288">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="273c7-289">如果沒有可用的磁碟空間，將會暫停虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="273c7-289">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="273c7-290"><dt>**已停止**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-290"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="273c7-291">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="273c7-291">This value is not supported.</span></span> <span data-ttu-id="273c7-292">如果虛擬機器已停止，則 [ **EnabledState** ] 屬性的值會是3， ([已停用]) 。</span><span class="sxs-lookup"><span data-stu-id="273c7-292">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="273c7-293"><dt>**在服務**</dt> <dt>11</dt>中</span><span class="sxs-lookup"><span data-stu-id="273c7-293"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="273c7-294">虛擬機器正在處理要求。</span><span class="sxs-lookup"><span data-stu-id="273c7-294">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="273c7-295"><dt>**休眠**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-295"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="273c7-296">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="273c7-296">This value is not supported.</span></span> <span data-ttu-id="273c7-297">如果虛擬機器已暫停或暫停，則 [ **EnabledState** ] 屬性的值會是 32769 ([已暫停]) 或 32768 (暫停) 。</span><span class="sxs-lookup"><span data-stu-id="273c7-297">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="273c7-298">位於索引 1 (1) 的值是選擇性的，並包含次要狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="273c7-298">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="273c7-299">用戶端應該使用索引零 (0) 的主要狀態，以判斷是否可以將新的要求發行至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="273c7-299">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="273c7-300">如果 **operationalstatus** \[ 0 \] 是 2 (確定) ，則由 **OperationalStatus** 1 指出的作業 \[ \] 可能會中斷。</span><span class="sxs-lookup"><span data-stu-id="273c7-300">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="273c7-301">在 **OperationalStatus** \[ 1 的值 \] 是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="273c7-301">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="273c7-302">值</span><span class="sxs-lookup"><span data-stu-id="273c7-302">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="273c7-303">意義</span><span class="sxs-lookup"><span data-stu-id="273c7-303">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="273c7-304"><dt>**正在建立快照**</dt>集 <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-304"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="273c7-305">正在為虛擬機器建立快照集。</span><span class="sxs-lookup"><span data-stu-id="273c7-305">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="273c7-306">正在套用 <dt>**快照**</dt>集 <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-306"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="273c7-307">正在將快照集套用到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="273c7-307">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="273c7-308"><dt>**正在刪除快照**</dt>集 <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-308"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="273c7-309">正在從虛擬機器刪除快照集。</span><span class="sxs-lookup"><span data-stu-id="273c7-309">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="273c7-310"><dt>**正在等候開始**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-310"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="273c7-311">虛擬機器將會在自動啟動延遲經過之後啟動。</span><span class="sxs-lookup"><span data-stu-id="273c7-311">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="273c7-312"><dt>**合併磁片**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-312"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="273c7-313">先前已刪除之快照集的虛擬硬碟正在合併。</span><span class="sxs-lookup"><span data-stu-id="273c7-313">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="273c7-314"><dt>**正在匯出虛擬機器**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-314"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="273c7-315">正在匯出虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="273c7-315">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="273c7-316">正在 <dt>**遷移虛擬機器**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-316"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="273c7-317">虛擬機器正在從一部實體電腦即時移轉至另一部電腦。</span><span class="sxs-lookup"><span data-stu-id="273c7-317">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="273c7-318">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="273c7-318">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-321">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="273c7-321">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="273c7-322">當 **TargetOperatingSystem** 屬性的值為 1 (其他) （需要 **OtherTargetOS** 屬性必須有非 **Null** 值）時，軟體元素的製造商和作業系統。</span><span class="sxs-lookup"><span data-stu-id="273c7-322">The manufacturer and operating system for a software element when the **TargetOperatingSystem** property has a value of 1 (Other), which requires the **OtherTargetOS** property to have a non-**Null** value.</span></span> <span data-ttu-id="273c7-323">對於 **TargetOperatingSystem** 的所有其他值， **OtherTargetOS** 屬性必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="273c7-323">For all other values of **TargetOperatingSystem**, the **OtherTargetOS** property must be **Null**.</span></span> <span data-ttu-id="273c7-324">這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="273c7-324">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-325">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="273c7-325">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-326">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="273c7-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-328">若為 True，則這是電腦系統的主要 BIOS。</span><span class="sxs-lookup"><span data-stu-id="273c7-328">If True, this is the primary BIOS of the computer system.</span></span> <span data-ttu-id="273c7-329">這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="273c7-329">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-330">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="273c7-330">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-331">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="273c7-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-333">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="273c7-333">Provides high level status information.</span></span> <span data-ttu-id="273c7-334">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="273c7-334">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="273c7-335">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="273c7-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="273c7-336">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-337">**RegistryURIs**</span><span class="sxs-lookup"><span data-stu-id="273c7-337">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-338">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="273c7-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="273c7-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-340">字串的陣列，表示執行符合的 BIOS 屬性登錄或登錄的發行位置。</span><span class="sxs-lookup"><span data-stu-id="273c7-340">An array of strings representing the publication location of the BIOS attribute registry or registries the implementation complies to.</span></span> <span data-ttu-id="273c7-341">這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-341">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-342">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="273c7-342">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-343">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="273c7-343">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-345">BIOS 的發行日期。</span><span class="sxs-lookup"><span data-stu-id="273c7-345">The date that the BIOS was released.</span></span> <span data-ttu-id="273c7-346">這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-346">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-347">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="273c7-347">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-348">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-350">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="273c7-350">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="273c7-351">指派的 BIOS 序號。</span><span class="sxs-lookup"><span data-stu-id="273c7-351">The assigned serial number of the BIOS.</span></span> <span data-ttu-id="273c7-352">這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-352">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-353">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="273c7-353">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-354">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-356">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="273c7-356">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="273c7-357">Software 元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="273c7-357">An identifier for the software element.</span></span> <span data-ttu-id="273c7-358">這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，且一律設定為 "Microsoft：*GUID* \\ *裝置特定資料*"。</span><span class="sxs-lookup"><span data-stu-id="273c7-358">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="273c7-359">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="273c7-359">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-360">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="273c7-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-362">軟體元素生命週期的狀態。</span><span class="sxs-lookup"><span data-stu-id="273c7-362">The state of a software element's life cycle.</span></span> <span data-ttu-id="273c7-363">這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，而且一律設定為 2 (可執行檔) 。</span><span class="sxs-lookup"><span data-stu-id="273c7-363">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 2 (Executable).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-364">**狀態**</span><span class="sxs-lookup"><span data-stu-id="273c7-364">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-365">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-367">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="273c7-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="273c7-368">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="273c7-368">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-369">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="273c7-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="273c7-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-371">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="273c7-371">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="273c7-372">陣列，其中包含描述對應之 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="273c7-372">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="273c7-373">例如，如果服務) 中的 11 (是指派給 **OperationalStatus** \[ 0 的值 \] ，則 **StatusDescriptions** \[ 0 \] 可能會包含虛擬機器處理要求的原因說明。</span><span class="sxs-lookup"><span data-stu-id="273c7-373">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="273c7-374">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="273c7-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-375">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="273c7-375">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-376">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="273c7-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273c7-378">元素的作業系統環境。</span><span class="sxs-lookup"><span data-stu-id="273c7-378">The element's operating system environment.</span></span> <span data-ttu-id="273c7-379">這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，且一律設定為 0 (未知) 。</span><span class="sxs-lookup"><span data-stu-id="273c7-379">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 0 (Unknown).</span></span>

</dd> <dt>

<span data-ttu-id="273c7-380">**版本**</span><span class="sxs-lookup"><span data-stu-id="273c7-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273c7-381">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="273c7-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="273c7-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="273c7-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273c7-383">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="273c7-383">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="273c7-384">BIOS 的版本。</span><span class="sxs-lookup"><span data-stu-id="273c7-384">The version of the BIOS.</span></span> <span data-ttu-id="273c7-385">這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為 "8.02.00"。</span><span class="sxs-lookup"><span data-stu-id="273c7-385">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "8.02.00".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="273c7-386">備註</span><span class="sxs-lookup"><span data-stu-id="273c7-386">Remarks</span></span>

<span data-ttu-id="273c7-387">存取 **Msvm \_ BIOSElement** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="273c7-387">Access to the **Msvm\_BIOSElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="273c7-388">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="273c7-388">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="273c7-389">規格需求</span><span class="sxs-lookup"><span data-stu-id="273c7-389">Requirements</span></span>



| <span data-ttu-id="273c7-390">需求</span><span class="sxs-lookup"><span data-stu-id="273c7-390">Requirement</span></span> | <span data-ttu-id="273c7-391">值</span><span class="sxs-lookup"><span data-stu-id="273c7-391">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="273c7-392">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="273c7-392">Minimum supported client</span></span><br/> | <span data-ttu-id="273c7-393">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="273c7-393">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="273c7-394">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="273c7-394">Minimum supported server</span></span><br/> | <span data-ttu-id="273c7-395">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="273c7-395">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="273c7-396">命名空間</span><span class="sxs-lookup"><span data-stu-id="273c7-396">Namespace</span></span><br/>                | <span data-ttu-id="273c7-397">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="273c7-397">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="273c7-398">MOF</span><span class="sxs-lookup"><span data-stu-id="273c7-398">MOF</span></span><br/>                      | <dl> <span data-ttu-id="273c7-399"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-399"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="273c7-400">DLL</span><span class="sxs-lookup"><span data-stu-id="273c7-400">DLL</span></span><br/>                      | <dl> <span data-ttu-id="273c7-401"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="273c7-401"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="273c7-402">另請參閱</span><span class="sxs-lookup"><span data-stu-id="273c7-402">See also</span></span>

<dl> <dt>

[<span data-ttu-id="273c7-403">**CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="273c7-403">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="273c7-404">BIOS 類別</span><span class="sxs-lookup"><span data-stu-id="273c7-404">BIOS Classes</span></span>](bios-classes.md)
</dt> <dt>

[<span data-ttu-id="273c7-405">**CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="273c7-405">**CIM\_BIOSElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 

