---
description: 用於 Msvm VirtualSystemManagementService 類別中的 GetSummaryInformation 方法 \_ ，以快速取得與虛擬系統或快照集相關的一般資訊。
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Msvm_SummaryInformationBase 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65c20239673f279babba2581c4300f373f1392bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974155"
---
# <a name="msvm_summaryinformationbase-class"></a><span data-ttu-id="d6df4-103">Msvm \_ SummaryInformationBase 類別</span><span class="sxs-lookup"><span data-stu-id="d6df4-103">Msvm\_SummaryInformationBase class</span></span>

<span data-ttu-id="d6df4-104">用於 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別中的 [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)方法，以快速取得與虛擬系統或快照集相關的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="d6df4-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) method in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual system or snapshot.</span></span>

<span data-ttu-id="d6df4-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d6df4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6df4-106">語法</span><span class="sxs-lookup"><span data-stu-id="d6df4-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="d6df4-107">成員</span><span class="sxs-lookup"><span data-stu-id="d6df4-107">Members</span></span>

<span data-ttu-id="d6df4-108">**Msvm \_ SummaryInformationBase** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d6df4-108">The **Msvm\_SummaryInformationBase** class has these types of members:</span></span>

-   [<span data-ttu-id="d6df4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d6df4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6df4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d6df4-110">Properties</span></span>

<span data-ttu-id="d6df4-111">**Msvm \_ SummaryInformationBase** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d6df4-111">The **Msvm\_SummaryInformationBase** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6df4-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="d6df4-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-113">資料類型： **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d6df4-113">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-115">建立虛擬系統或快照集的時間。</span><span class="sxs-lookup"><span data-stu-id="d6df4-115">The time at which the virtual system or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-116">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d6df4-116">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6df4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ ManagedElement. ElementName" ) </span><span class="sxs-lookup"><span data-stu-id="d6df4-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-120">虛擬系統或快照的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="d6df4-120">The friendly name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-121">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d6df4-121">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-122">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d6df4-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-124">虛擬系統或快照的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d6df4-124">The current state of the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-125">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="d6df4-125">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d6df4-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-128">指出主機是否允許增強模式連線，以及是否允許虛擬機器使用它們（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d6df4-128">Indicates whether or not enhanced mode connections are allowed by the host and if allowed, whether or not they are available to the virtual machine.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="d6df4-129">**允許和可用** (2) </span><span class="sxs-lookup"><span data-stu-id="d6df4-129">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="d6df4-130">**不允許** (3) </span><span class="sxs-lookup"><span data-stu-id="d6df4-130">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="d6df4-131">**允許但無法使用** (6) </span><span class="sxs-lookup"><span data-stu-id="d6df4-131">**Allowed but not available** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d6df4-132">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d6df4-132">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-133">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d6df4-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-135">虛擬系統目前的健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="d6df4-135">The current health state for the virtual system.</span></span> <span data-ttu-id="d6df4-136">對於代表虛擬系統快照集的 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="d6df4-136">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-137">**HostComputerSystemName**</span><span class="sxs-lookup"><span data-stu-id="d6df4-137">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6df4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-140">裝載此虛擬機器的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="d6df4-140">The name of the computer hosting this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d6df4-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6df4-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-144">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ ManagedElement. InstanceID" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d6df4-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-145">InstanceID 是選擇性屬性，可在具現化命名空間的範圍內，用來以不透明和唯一的方式識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="d6df4-145">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="d6df4-146">此類別的各種子類別可覆寫這個屬性，使其成為必要或索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d6df4-146">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="d6df4-147">這類子類別也可以修改慣用的演算法，以確保以下定義的唯一性。</span><span class="sxs-lookup"><span data-stu-id="d6df4-147">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="d6df4-148">為確保命名空間中的唯一性，InstanceID 的值應使用下列「慣用」演算法來建立：</span><span class="sxs-lookup"><span data-stu-id="d6df4-148">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="d6df4-149"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="d6df4-149"><OrgID>:<LocalID></span></span>

<span data-ttu-id="d6df4-150">Where <OrgID> 和 <LocalID> 會以冒號分隔 (： ) ，其中 <OrgID> 必須包含受著作權、商標或其他唯一的名稱，而該名稱是由建立或定義 InstanceID 的商務實體所擁有，或是由可辨識的全域授權單位指派給商務實體的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6df4-150">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="d6df4-151"> (這項需求類似于 <Schema Name> \_ <Class Name> 架構類別名稱的結構。此外，) 此外，為了確保唯一性， <OrgID> 不能包含冒號 (： ) 。</span><span class="sxs-lookup"><span data-stu-id="d6df4-151">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="d6df4-152">使用此演算法時，InstanceID 中出現的第一個冒號必須出現在 <OrgID> 和之間 <LocalID> 。</span><span class="sxs-lookup"><span data-stu-id="d6df4-152">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="d6df4-153"><LocalID> 由商務實體選擇，不應重複使用，以找出不同的基礎 (真實世界) 元素。</span><span class="sxs-lookup"><span data-stu-id="d6df4-153"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="d6df4-154">如果不是 null，而且未使用上述的「慣用」演算法，則定義實體必須確保產生的 InstanceID 不會在這個實例的命名空間或其他提供者所產生的任何 InstanceIDs 上重複使用。</span><span class="sxs-lookup"><span data-stu-id="d6df4-154">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="d6df4-155">如果未針對 DMTF 定義的實例將設定為 null，就必須使用「慣用」演算法搭配 <OrgID> 將設定為 CIM。</span><span class="sxs-lookup"><span data-stu-id="d6df4-155">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-156">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d6df4-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6df4-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-159">虛擬系統或快照的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="d6df4-159">The unique name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-160">**注意事項**</span><span class="sxs-lookup"><span data-stu-id="d6df4-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6df4-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-163">與虛擬系統或快照集相關的附注。</span><span class="sxs-lookup"><span data-stu-id="d6df4-163">The notes associated with the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-164">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="d6df4-164">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-165">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d6df4-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-167">配置給虛擬系統或快照集的虛擬處理器總數。</span><span class="sxs-lookup"><span data-stu-id="d6df4-167">The total number of virtual processors allocated to the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-168">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d6df4-168">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-169">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d6df4-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-171">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="d6df4-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-172">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d6df4-172">The current status of the element.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-173">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d6df4-173">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6df4-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-176">描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="d6df4-176">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="d6df4-177">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 null。</span><span class="sxs-lookup"><span data-stu-id="d6df4-177">This property must be set to null when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-178">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d6df4-178">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-179">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d6df4-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-181">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="d6df4-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-182">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="d6df4-182">Strings that describe the various **OperationalStatus** array values.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-183">**99.99**</span><span class="sxs-lookup"><span data-stu-id="d6df4-183">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-184">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d6df4-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-186">自虛擬系統上次開機之後的時間量。</span><span class="sxs-lookup"><span data-stu-id="d6df4-186">The amount of time since the virtual system was last booted.</span></span> <span data-ttu-id="d6df4-187">對於代表虛擬系統快照集的 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="d6df4-187">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-188">**版本**</span><span class="sxs-lookup"><span data-stu-id="d6df4-188">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6df4-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-191">虛擬系統的版本，格式為「主要. 次要」;例如 "2.0"。</span><span class="sxs-lookup"><span data-stu-id="d6df4-191">The version of the virtual system in a format of "major.minor"; for example, "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-192">**VirtualSwitchNames**</span><span class="sxs-lookup"><span data-stu-id="d6df4-192">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-193">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d6df4-193">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-195">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="d6df4-195">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-196">列出 VM 所連接之虛擬交換器的易記名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="d6df4-196">Strings that list the friendly names of the virtual switches the VM is connected to.</span></span>

</dd> <dt>

<span data-ttu-id="d6df4-197">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="d6df4-197">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6df4-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6df4-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6df4-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6df4-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6df4-200">虛擬系統的子類型。</span><span class="sxs-lookup"><span data-stu-id="d6df4-200">The subtype of the virtual system.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="d6df4-201">**Microsoft： hyper-v：子類型： 1** ( "Microsoft： Hyper-v：子類型： 1" ) </span><span class="sxs-lookup"><span data-stu-id="d6df4-201">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="d6df4-202">**Microsoft： hyper-v：子類型： 2** ( "Microsoft： Hyper-v：子類型： 2" ) </span><span class="sxs-lookup"><span data-stu-id="d6df4-202">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


<span data-ttu-id="d6df4-203"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d6df4-203"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d6df4-204">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6df4-204">Requirements</span></span>



| <span data-ttu-id="d6df4-205">需求</span><span class="sxs-lookup"><span data-stu-id="d6df4-205">Requirement</span></span> | <span data-ttu-id="d6df4-206">值</span><span class="sxs-lookup"><span data-stu-id="d6df4-206">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6df4-207">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6df4-207">Minimum supported client</span></span><br/> | <span data-ttu-id="d6df4-208">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6df4-208">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d6df4-209">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6df4-209">Minimum supported server</span></span><br/> | <span data-ttu-id="d6df4-210">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d6df4-210">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d6df4-211">命名空間</span><span class="sxs-lookup"><span data-stu-id="d6df4-211">Namespace</span></span><br/>                | <span data-ttu-id="d6df4-212">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d6df4-212">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d6df4-213">MOF</span><span class="sxs-lookup"><span data-stu-id="d6df4-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6df4-214"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d6df4-214"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6df4-215">DLL</span><span class="sxs-lookup"><span data-stu-id="d6df4-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6df4-216"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d6df4-216"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d6df4-217">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6df4-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6df4-218">**CIM \_ 視圖**</span><span class="sxs-lookup"><span data-stu-id="d6df4-218">**CIM\_View**</span></span>](cim-view.md)
</dt> </dl>

 

