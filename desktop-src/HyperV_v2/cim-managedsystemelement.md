---
description: CIM \_ ManagedSystemElement 是 system 元素階層的基類。 系統可能會以這個類別或其子類別來表示系統的任何元件。
ms.assetid: 838cc77f-8a8d-429a-8e17-5ede3cc9b6ed
title: 'CIM_ManagedSystemElement 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.OperationalStatus
- CIM_ManagedSystemElement.StatusDescriptions
- CIM_ManagedSystemElement.Status
- CIM_ManagedSystemElement.HealthState
- CIM_ManagedSystemElement.CommunicationStatus
- CIM_ManagedSystemElement.DetailedStatus
- CIM_ManagedSystemElement.OperatingStatus
- CIM_ManagedSystemElement.PrimaryStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f16b84e24929d5cfdb6e5dd8855d69a8bce2dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193515"
---
# <a name="cim_managedsystemelement-class-hyper-v-management"></a><span data-ttu-id="06520-104">CIM_ManagedSystemElement 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="06520-104">CIM_ManagedSystemElement class (Hyper-V management)</span></span>

<span data-ttu-id="06520-105">**CIM \_ManagedSystemElement** 是系統元素階層的基類。</span><span class="sxs-lookup"><span data-stu-id="06520-105">**CIM\_ManagedSystemElement** is the base class for the system element hierarchy.</span></span> <span data-ttu-id="06520-106">系統可能會以這個類別或其子類別來表示系統的任何元件。</span><span class="sxs-lookup"><span data-stu-id="06520-106">Any component of a system can potentially be represented by this class or its subclasses.</span></span>

## <a name="syntax"></a><span data-ttu-id="06520-107">語法</span><span class="sxs-lookup"><span data-stu-id="06520-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedSystemElement : CIM_ManagedElement
{
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
};
```

## <a name="members"></a><span data-ttu-id="06520-108">成員</span><span class="sxs-lookup"><span data-stu-id="06520-108">Members</span></span>

<span data-ttu-id="06520-109">**CIM \_ ManagedSystemElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="06520-109">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="06520-110">屬性</span><span class="sxs-lookup"><span data-stu-id="06520-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06520-111">屬性</span><span class="sxs-lookup"><span data-stu-id="06520-111">Properties</span></span>

<span data-ttu-id="06520-112">**CIM \_ ManagedSystemElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="06520-112">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06520-113">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="06520-113">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06520-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06520-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06520-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06520-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06520-116">指出檢測與此元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="06520-116">Indicates the ability of the instrumentation to communicate with this element.</span></span> <span data-ttu-id="06520-117">**Null** 值表示檢測不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="06520-117">A **NULL** value indicates that instrumentation does not support this property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06520-118">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06520-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="06520-119"> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="06520-119">**Not Available** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>

<span data-ttu-id="06520-120">**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="06520-120">**Communication OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="06520-121">**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="06520-121">**Lost Communication** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="06520-122">**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="06520-122">**No Contact** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="06520-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="06520-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="06520-124">**廠商保留** (0x8000。) </span><span class="sxs-lookup"><span data-stu-id="06520-124">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06520-125">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="06520-125">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06520-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06520-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06520-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06520-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06520-128">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**"，"**CIM \_ ManagedSystemElement**.**HealthState**") </span><span class="sxs-lookup"><span data-stu-id="06520-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="06520-129">指出補充 **PrimaryStatus** 屬性的其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="06520-129">Indicates additional status details that complement the **PrimaryStatus** property.</span></span> <span data-ttu-id="06520-130">**Null** 值表示檢測不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="06520-130">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="06520-131"> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="06520-131">**Not Available** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>

<span data-ttu-id="06520-132">**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="06520-132">**No Additional Information** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="06520-133">**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="06520-133">**Stressed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="06520-134">**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="06520-134">**Predictive Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="06520-135">**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="06520-135">**Non-Recoverable Error** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="06520-136">**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="06520-136">**Supporting Entity in Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="06520-137">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="06520-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="06520-138">**廠商保留** (0x8000。) </span><span class="sxs-lookup"><span data-stu-id="06520-138">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06520-139">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="06520-139">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06520-140">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06520-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06520-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06520-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06520-142">表示專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="06520-142">Indicates the current health of the element.</span></span> <span data-ttu-id="06520-143">這個屬性會表示這個專案的健康情況，但不一定是其子元件的健全狀況。</span><span class="sxs-lookup"><span data-stu-id="06520-143">This attribute expresses the health of this element, but not necessarily the health of its subcomponents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06520-144">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06520-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="06520-145">**確定** (5) </span><span class="sxs-lookup"><span data-stu-id="06520-145">**OK** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="06520-146">**降級/警告** (10) </span><span class="sxs-lookup"><span data-stu-id="06520-146">**Degraded/Warning** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_failure"></span><span id="minor_failure"></span><span id="MINOR_FAILURE"></span>

<span data-ttu-id="06520-147">**次要失敗** (15) </span><span class="sxs-lookup"><span data-stu-id="06520-147">**Minor failure** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span>

<span data-ttu-id="06520-148">**重大失敗** (20) </span><span class="sxs-lookup"><span data-stu-id="06520-148">**Major failure** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span>

<span data-ttu-id="06520-149">**嚴重失敗** (25) </span><span class="sxs-lookup"><span data-stu-id="06520-149">**Critical failure** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable_error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="06520-150">**無法復原的錯誤** (30) </span><span class="sxs-lookup"><span data-stu-id="06520-150">**Non-recoverable error** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="06520-151">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="06520-151">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06520-152">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="06520-152">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06520-153">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="06520-153">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06520-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06520-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06520-155">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="06520-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="06520-156">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="06520-156">Indicates when the object was installed.</span></span> <span data-ttu-id="06520-157">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="06520-157">The lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="06520-158">**名稱**</span><span class="sxs-lookup"><span data-stu-id="06520-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06520-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06520-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06520-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06520-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06520-161">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="06520-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="06520-162">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="06520-162">The label by which the object is known.</span></span> <span data-ttu-id="06520-163">子類別化時， **Name** 屬性可以覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="06520-163">When subclassed, the **Name** property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="06520-164">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="06520-164">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06520-165">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06520-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06520-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06520-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06520-167">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**") </span><span class="sxs-lookup"><span data-stu-id="06520-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="06520-168">表示專案目前的操作條件。</span><span class="sxs-lookup"><span data-stu-id="06520-168">Indicates the current operational condition of the element.</span></span> <span data-ttu-id="06520-169">這個屬性可以用來提供關於 **EnabledState** 屬性值的更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="06520-169">This property can be used to provide more detail about the value of the **EnabledState** property.</span></span> <span data-ttu-id="06520-170">**Null** 值表示檢測不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="06520-170">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<span data-ttu-id="06520-171">「未知」表示</span><span class="sxs-lookup"><span data-stu-id="06520-171">"Unknown" indicates</span></span>

<span data-ttu-id="06520-172">「無」表示</span><span class="sxs-lookup"><span data-stu-id="06520-172">"None" indicates that</span></span>

<span data-ttu-id="06520-173">于</span><span class="sxs-lookup"><span data-stu-id="06520-173">"Servicing"</span></span>

<span data-ttu-id="06520-174">入門</span><span class="sxs-lookup"><span data-stu-id="06520-174">"Starting"</span></span>

<span data-ttu-id="06520-175">從而</span><span class="sxs-lookup"><span data-stu-id="06520-175">"Stopping"</span></span>

<span data-ttu-id="06520-176">「已停止」和「已中止」很類似，雖然前者</span><span class="sxs-lookup"><span data-stu-id="06520-176">"Stopped" and "Aborted" are similar, although the former , while the latter i</span></span>

<span data-ttu-id="06520-177">「休眠」表示</span><span class="sxs-lookup"><span data-stu-id="06520-177">"Dormant" indicates that</span></span>

<span data-ttu-id="06520-178">「已完成」表示 t</span><span class="sxs-lookup"><span data-stu-id="06520-178">"Completed" indicates that t</span></span>

<span data-ttu-id="06520-179">遷移</span><span class="sxs-lookup"><span data-stu-id="06520-179">"Migrating"</span></span>

<span data-ttu-id="06520-180">"Immigrating"</span><span class="sxs-lookup"><span data-stu-id="06520-180">"Immigrating"</span></span>

<span data-ttu-id="06520-181">"Emigrating"</span><span class="sxs-lookup"><span data-stu-id="06520-181">"Emigrating"</span></span>

<span data-ttu-id="06520-182">「正在關機」</span><span class="sxs-lookup"><span data-stu-id="06520-182">"Shutting Down"</span></span>

<span data-ttu-id="06520-183">「測試中」</span><span class="sxs-lookup"><span data-stu-id="06520-183">"In Test"</span></span>

<span data-ttu-id="06520-184">轉變</span><span class="sxs-lookup"><span data-stu-id="06520-184">"Transitioning"</span></span>

<span data-ttu-id="06520-185">「服務中」</span><span class="sxs-lookup"><span data-stu-id="06520-185">"In Service"</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06520-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06520-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="06520-187">實作為一般能夠傳回這個屬性，但目前無法這麼做。</span><span class="sxs-lookup"><span data-stu-id="06520-187">The implementation is in general capable of returning this property, but is unable to do so at this time.</span></span>

</dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="06520-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="06520-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="06520-189">執行 (提供者) 能夠傳回這個屬性的值，但不是針對此特定硬體/軟體的部分，或是刻意未使用屬性的情況，因為它不會加入任何有意義的資訊 (例如，將其他資訊新增至另一個屬性) 時所使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="06520-189">The implementation (provider) is capable of returning a value for this property, but not ever for this particular piece of hardware/software or the property is intentionally not used because it adds no meaningful information (as in the case of a property that is intended to add additional info to another property).</span></span>

</dd> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>

<span data-ttu-id="06520-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="06520-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>


</dt> <dd>

<span data-ttu-id="06520-191">描述要設定、維護、清除或以其他方式管理的元素。</span><span class="sxs-lookup"><span data-stu-id="06520-191">Describes an element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="06520-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="06520-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="06520-193">描述正在初始化的元素。</span><span class="sxs-lookup"><span data-stu-id="06520-193">Describes an element being initialized.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="06520-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="06520-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>


</dt> <dd>

<span data-ttu-id="06520-195">描述要帶到有條理之停止的元素。</span><span class="sxs-lookup"><span data-stu-id="06520-195">Describes an element being brought to an orderly stop.</span></span>

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="06520-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="06520-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>


</dt> <dd>

<span data-ttu-id="06520-197">發生乾淨且有條理的停止。</span><span class="sxs-lookup"><span data-stu-id="06520-197">A clean and orderly stop has occurred.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="06520-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="06520-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>


</dt> <dd>

<span data-ttu-id="06520-199">發生突然停止，其中元素的狀態和設定可能需要更新。</span><span class="sxs-lookup"><span data-stu-id="06520-199">An abrupt stop has occurred, where the state and configuration of the element might need to be updated.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="06520-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="06520-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>


</dt> <dd>

<span data-ttu-id="06520-201">元素為非使用中或已停止。</span><span class="sxs-lookup"><span data-stu-id="06520-201">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="06520-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="06520-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>


</dt> <dd>

<span data-ttu-id="06520-203">元素已完成其作業。</span><span class="sxs-lookup"><span data-stu-id="06520-203">The element has completed its operation.</span></span> <span data-ttu-id="06520-204">此值應該與 PrimaryStatus 中的 [確定]、[錯誤] 或 [已降級]，讓用戶端能夠判斷完成的作業是否已完成，但有「確定」 (通過) 、已完成，但 (失敗) 或已完成，但作業已完成，但未完成，或未報告錯誤 (。</span><span class="sxs-lookup"><span data-stu-id="06520-204">This value should be combined with either OK, Error, or Degraded in the PrimaryStatus so that a client can tell if the complete operation Completed with OK (passed), Completed with Error (failed), or Completed with Degraded (the operation finished, but it did not complete OK or did not report an error).</span></span>

</dd> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>

<span data-ttu-id="06520-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="06520-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>


</dt> <dd>

<span data-ttu-id="06520-206">專案正在主控制項之間移動。</span><span class="sxs-lookup"><span data-stu-id="06520-206">The element is being moved between host elements.</span></span>

</dd> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>

<span data-ttu-id="06520-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="06520-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>


</dt> <dd>

<span data-ttu-id="06520-208">正在將專案從主控制項移開。</span><span class="sxs-lookup"><span data-stu-id="06520-208">The element is being moved away from host element.</span></span>

</dd> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>

<span data-ttu-id="06520-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="06520-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>


</dt> <dd>

<span data-ttu-id="06520-210">正在將元素移至新的主項目目。</span><span class="sxs-lookup"><span data-stu-id="06520-210">The element is being moved to new host element.</span></span>

</dd> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>

<span data-ttu-id="06520-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="06520-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="06520-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="06520-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>


</dt> <dd>

<span data-ttu-id="06520-213">描述進入突然停止的元素。</span><span class="sxs-lookup"><span data-stu-id="06520-213">Describes an element being brought to an abrupt stop.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="06520-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="06520-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>


</dt> <dd>

<span data-ttu-id="06520-215">元素正在執行測試函數。</span><span class="sxs-lookup"><span data-stu-id="06520-215">The element is performing test functions.</span></span>

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>

<span data-ttu-id="06520-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="06520-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>


</dt> <dd>

<span data-ttu-id="06520-217">描述狀態之間的專案，也就是它在先前的狀態或下一個狀態下並未完全可用。</span><span class="sxs-lookup"><span data-stu-id="06520-217">Describes an element that is between states, that is, it is not fully available in either its previous state or its next state.</span></span> <span data-ttu-id="06520-218">如果其他表示轉換為特定狀態的值不適用，則應使用此值。</span><span class="sxs-lookup"><span data-stu-id="06520-218">This value should be used if other values indicating a transition to a specific state are not applicable.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="06520-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="06520-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>


</dt> <dd>

<span data-ttu-id="06520-220">描述服務中和操作中的元素。</span><span class="sxs-lookup"><span data-stu-id="06520-220">Describes an element that is in service and operational.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="06520-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="06520-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="06520-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (0x8000。) </span><span class="sxs-lookup"><span data-stu-id="06520-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06520-223">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="06520-223">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06520-224">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06520-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06520-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06520-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06520-226">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ManagedSystemElement**。**StatusDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="06520-226">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**StatusDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="06520-227">包含元素目前狀態的指標。</span><span class="sxs-lookup"><span data-stu-id="06520-227">Contains indicators of the current status of the element.</span></span> <span data-ttu-id="06520-228">**OperationalStatus** 屬性的第一個值應該包含元素的主要狀態。</span><span class="sxs-lookup"><span data-stu-id="06520-228">The first value of the **OperationalStatus** property should contain the primary status for the element.</span></span>

> [!Note]  
> <span data-ttu-id="06520-229">**OperationalStatus** 屬性會取代已被取代的 **Status** 屬性。</span><span class="sxs-lookup"><span data-stu-id="06520-229">The **OperationalStatus** property replaces the deprecated **Status** property.</span></span> <span data-ttu-id="06520-230">由於在管理應用程式中廣泛使用現有的 **Status** 屬性，因此強烈建議提供者或檢測提供 **狀態** 和 **OperationalStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="06520-230">Due to the widespread use of the existing **Status** property in management applications, we strongly recommend that providers or instrumentation provide both the **Status** and **OperationalStatus** properties.</span></span> <span data-ttu-id="06520-231">當已檢測的 **狀態**，因為它是單一值屬性，所以也應該提供元素的主要狀態。</span><span class="sxs-lookup"><span data-stu-id="06520-231">When instrumented, **Status**, because it is a single-valued property, should also provide the primary status of the element.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06520-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06520-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06520-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06520-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="06520-234"><span id="OK"></span><span id="ok"></span>**確定** (2) </span><span class="sxs-lookup"><span data-stu-id="06520-234"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="06520-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (3) **降級**</span><span class="sxs-lookup"><span data-stu-id="06520-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="06520-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span> (4) 的 **壓力**</span><span class="sxs-lookup"><span data-stu-id="06520-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (4)</span></span>


</dt> <dd>

<span data-ttu-id="06520-237">元素運作正常，但需要注意。</span><span class="sxs-lookup"><span data-stu-id="06520-237">The element is functioning, but needs attention.</span></span> <span data-ttu-id="06520-238">「壓力」狀態的範例有多載、針對過熱等等。</span><span class="sxs-lookup"><span data-stu-id="06520-238">Examples of "Stressed" states are overload, overheated, and so on.</span></span>

</dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="06520-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (5) </span><span class="sxs-lookup"><span data-stu-id="06520-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (5)</span></span>


</dt> <dd>

<span data-ttu-id="06520-240">元素正在運作名義上，但在不久的未來預測失敗。</span><span class="sxs-lookup"><span data-stu-id="06520-240">An element is functioning nominally but predicting a failure in the near future.</span></span>

</dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="06520-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="06520-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="06520-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="06520-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="06520-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (8) </span><span class="sxs-lookup"><span data-stu-id="06520-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="06520-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (9) </span><span class="sxs-lookup"><span data-stu-id="06520-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="06520-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (10) </span><span class="sxs-lookup"><span data-stu-id="06520-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (10)</span></span>


</dt> <dd>

<span data-ttu-id="06520-246">發生有條理的停止。</span><span class="sxs-lookup"><span data-stu-id="06520-246">An orderly stop has occurred.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="06520-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (11) </span><span class="sxs-lookup"><span data-stu-id="06520-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="06520-248">要設定、維護、清除或以其他方式管理的元素。</span><span class="sxs-lookup"><span data-stu-id="06520-248">An element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="06520-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (12) </span><span class="sxs-lookup"><span data-stu-id="06520-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="06520-250">監視系統有此專案的知識，但是從未能夠與其建立通訊。</span><span class="sxs-lookup"><span data-stu-id="06520-250">The monitoring system has knowledge of this element, but has never been able to establish communications with it.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="06520-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (13) </span><span class="sxs-lookup"><span data-stu-id="06520-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="06520-252">已知 ManagedSystem 元素存在，而且已在過去成功聯繫，但目前無法連線。</span><span class="sxs-lookup"><span data-stu-id="06520-252">The ManagedSystem Element is known to exist and has been contacted successfully in the past, but is currently unreachable.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="06520-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (14) </span><span class="sxs-lookup"><span data-stu-id="06520-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (14)</span></span>


</dt> <dd>

<span data-ttu-id="06520-254">突然停止，其中專案的狀態和設定可能需要更新的位置發生。</span><span class="sxs-lookup"><span data-stu-id="06520-254">An abrupt stop, where where the state and configuration of the element might need to be updated, has occurred.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="06520-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (15) </span><span class="sxs-lookup"><span data-stu-id="06520-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (15)</span></span>


</dt> <dd>

<span data-ttu-id="06520-256">元素為非使用中或已停止。</span><span class="sxs-lookup"><span data-stu-id="06520-256">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="06520-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>錯誤 (16) **中支援的實體**</span><span class="sxs-lookup"><span data-stu-id="06520-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

<span data-ttu-id="06520-258">這個元素可能是「確定」，但另一個相依的元素（相依）發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06520-258">This element might be "OK" but that another element, on which it is dependent, is in error.</span></span> <span data-ttu-id="06520-259">例如，因為較低層的網路問題而無法運作的網路服務或端點。</span><span class="sxs-lookup"><span data-stu-id="06520-259">An example is a network service or endpoint that cannot function due to lower-layer networking problems.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="06520-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (17) </span><span class="sxs-lookup"><span data-stu-id="06520-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (17)</span></span>


</dt> <dd>

<span data-ttu-id="06520-261">元素已完成其作業。</span><span class="sxs-lookup"><span data-stu-id="06520-261">The element has completed its operation.</span></span>

</dd> <dt>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>

<span data-ttu-id="06520-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**電源模式** (18) </span><span class="sxs-lookup"><span data-stu-id="06520-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Power Mode** (18)</span></span>


</dt> <dd>

<span data-ttu-id="06520-263">專案具有相關聯 PowerManagementService 關聯中包含的額外電源模型資訊。</span><span class="sxs-lookup"><span data-stu-id="06520-263">The element has additional power model information contained in the Associated PowerManagementService association.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="06520-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="06520-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="06520-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (0x8000。) </span><span class="sxs-lookup"><span data-stu-id="06520-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06520-266">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="06520-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06520-267">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06520-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06520-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06520-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06520-269">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ManagedSystemElement**.**DetailedStatus**"，"**CIM \_ ManagedSystemElement**.**HealthState**") </span><span class="sxs-lookup"><span data-stu-id="06520-269">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**DetailedStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="06520-270">表示高階狀態值。</span><span class="sxs-lookup"><span data-stu-id="06520-270">Indicates a high-level status value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06520-271">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06520-271">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="06520-272">**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="06520-272">**OK** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="06520-273"> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="06520-273">**Degraded** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="06520-274">**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="06520-274">**Error** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="06520-275">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="06520-275">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="06520-276">**廠商保留** (0x8000。) </span><span class="sxs-lookup"><span data-stu-id="06520-276">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06520-277">**狀態**</span><span class="sxs-lookup"><span data-stu-id="06520-277">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06520-278">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06520-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06520-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06520-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06520-280">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「**CIM \_ ManagedSystemElement**。**OperationalStatus**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="06520-280">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="06520-281">指出物件的主要狀態。</span><span class="sxs-lookup"><span data-stu-id="06520-281">Indicates the primary status of the object.</span></span>

> [!Note]  
> <span data-ttu-id="06520-282">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="06520-282">This property is deprecated.</span></span> <span data-ttu-id="06520-283">它會由 **OperationalStatus** 屬性取代。</span><span class="sxs-lookup"><span data-stu-id="06520-283">It is replaced by the **OperationalStatus** property.</span></span> <span data-ttu-id="06520-284">如果您選擇使用 **Status** 屬性來提供回溯相容性，它應該是 [ **OperationalStatus** ] 屬性的 [次要]。</span><span class="sxs-lookup"><span data-stu-id="06520-284">If you choose to use the **Status** property for backward compatibility, it should be secondary to the **OperationalStatus** property.</span></span>

 

<dt>



 <span data-ttu-id="06520-285"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="06520-285">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06520-286"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="06520-286">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06520-287"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="06520-287">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06520-288"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="06520-288">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06520-289"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="06520-289">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06520-290"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="06520-290">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06520-291"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="06520-291">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06520-292"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="06520-292">("Service")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06520-293"> ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="06520-293">("Stressed")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06520-294"> ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="06520-294">("NonRecover")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06520-295"> ( "No Contact" ) </span><span class="sxs-lookup"><span data-stu-id="06520-295">("No Contact")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06520-296"> ( 「遺失通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="06520-296">("Lost Comm")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06520-297"> ( 「已停止」 ) </span><span class="sxs-lookup"><span data-stu-id="06520-297">("Stopped")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06520-298">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="06520-298">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06520-299">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06520-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06520-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06520-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06520-301">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ManagedSystemElement**。**OperationalStatus**") </span><span class="sxs-lookup"><span data-stu-id="06520-301">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="06520-302">指出 **OperationalStatus** 陣列中對應值的描述。</span><span class="sxs-lookup"><span data-stu-id="06520-302">Indicates descriptions of the corresponding values in the **OperationalStatus** array.</span></span> <span data-ttu-id="06520-303">例如，如果 [ **OperationalStatus** ] 屬性中的專案包含 [ **正在停止**] 值，則在這個屬性中相同陣列索引處的專案可能會包含物件停止原因的說明。</span><span class="sxs-lookup"><span data-stu-id="06520-303">For example, if an element in the **OperationalStatus** property contains the value **Stopping**, then the element at the same array index in this property might contain an explanation as to why an object is being stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06520-304">規格需求</span><span class="sxs-lookup"><span data-stu-id="06520-304">Requirements</span></span>



| <span data-ttu-id="06520-305">需求</span><span class="sxs-lookup"><span data-stu-id="06520-305">Requirement</span></span> | <span data-ttu-id="06520-306">值</span><span class="sxs-lookup"><span data-stu-id="06520-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06520-307">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06520-307">Minimum supported client</span></span><br/> | <span data-ttu-id="06520-308">Windows 8</span><span class="sxs-lookup"><span data-stu-id="06520-308">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="06520-309">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06520-309">Minimum supported server</span></span><br/> | <span data-ttu-id="06520-310">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06520-310">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="06520-311">命名空間</span><span class="sxs-lookup"><span data-stu-id="06520-311">Namespace</span></span><br/>                | <span data-ttu-id="06520-312">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="06520-312">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="06520-313">MOF</span><span class="sxs-lookup"><span data-stu-id="06520-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06520-314"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="06520-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06520-315">DLL</span><span class="sxs-lookup"><span data-stu-id="06520-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06520-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06520-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06520-317">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06520-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06520-318">**CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="06520-318">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

