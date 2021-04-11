---
description: 表示 \_ 非配置相關之 Msvm ResourcePool 實例的設定。
ms.assetid: c5954a92-8942-4b45-aae2-6936328dab1a
title: Msvm_AbstractResourcePoolSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AbstractResourcePoolSettingData
- Msvm_AbstractResourcePoolSettingData.InstanceID
- Msvm_AbstractResourcePoolSettingData.Caption
- Msvm_AbstractResourcePoolSettingData.Description
- Msvm_AbstractResourcePoolSettingData.ElementName
- Msvm_AbstractResourcePoolSettingData.PoolID
- Msvm_AbstractResourcePoolSettingData.ResourceType
- Msvm_AbstractResourcePoolSettingData.OtherResourceType
- Msvm_AbstractResourcePoolSettingData.ResourceSubType
- Msvm_AbstractResourcePoolSettingData.LoadBalancingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingOrder
- Msvm_AbstractResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9109bd428797c8c4f1073577e015bf4b9eddcc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944568"
---
# <a name="msvm_abstractresourcepoolsettingdata-class"></a><span data-ttu-id="21303-103">Msvm \_ AbstractResourcePoolSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="21303-103">Msvm\_AbstractResourcePoolSettingData class</span></span>

<span data-ttu-id="21303-104">表示非配置相關之 [**Msvm \_ ResourcePool**](msvm-resourcepool.md) 實例的設定。</span><span class="sxs-lookup"><span data-stu-id="21303-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="21303-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="21303-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="21303-106">語法</span><span class="sxs-lookup"><span data-stu-id="21303-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_AbstractResourcePoolSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string PoolID;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 LoadBalancingBehavior;
  uint16 MappingBehavior;
  string MappingOrder[];
  string Notes;
};
```

## <a name="members"></a><span data-ttu-id="21303-107">成員</span><span class="sxs-lookup"><span data-stu-id="21303-107">Members</span></span>

<span data-ttu-id="21303-108">**Msvm \_ AbstractResourcePoolSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="21303-108">The **Msvm\_AbstractResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="21303-109">屬性</span><span class="sxs-lookup"><span data-stu-id="21303-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21303-110">屬性</span><span class="sxs-lookup"><span data-stu-id="21303-110">Properties</span></span>

<span data-ttu-id="21303-111">**Msvm \_ AbstractResourcePoolSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="21303-111">The **Msvm\_AbstractResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21303-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="21303-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21303-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="21303-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21303-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21303-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21303-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="21303-115">A short description of the object.</span></span> <span data-ttu-id="21303-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="21303-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="21303-117">**說明**</span><span class="sxs-lookup"><span data-stu-id="21303-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21303-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="21303-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21303-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21303-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21303-120">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="21303-120">A description of the object.</span></span> <span data-ttu-id="21303-121">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="21303-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="21303-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="21303-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21303-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="21303-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21303-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21303-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21303-125">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="21303-125">A display name for the object.</span></span> <span data-ttu-id="21303-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="21303-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="21303-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="21303-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21303-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="21303-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21303-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21303-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21303-130">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="21303-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="21303-131">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="21303-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="21303-132">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="21303-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="21303-133">**LoadBalancingBehavior**</span><span class="sxs-lookup"><span data-stu-id="21303-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21303-134">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="21303-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21303-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21303-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21303-136">指定資源集區用來在其匯總資源之間平衡資源使用量的配置策略。</span><span class="sxs-lookup"><span data-stu-id="21303-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21303-137">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="21303-137">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="21303-138">**不支援** (2) </span><span class="sxs-lookup"><span data-stu-id="21303-138">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="21303-139">**無** (3) </span><span class="sxs-lookup"><span data-stu-id="21303-139">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>

<span data-ttu-id="21303-140">**分散式** (4) </span><span class="sxs-lookup"><span data-stu-id="21303-140">**Distributed** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Consolidated"></span><span id="consolidated"></span><span id="CONSOLIDATED"></span>

<span data-ttu-id="21303-141">**合併** (5) </span><span class="sxs-lookup"><span data-stu-id="21303-141">**Consolidated** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21303-142">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="21303-142">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21303-143">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="21303-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21303-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21303-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21303-145">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**") </span><span class="sxs-lookup"><span data-stu-id="21303-145">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="21303-146">指定當無法配置所需的資源時，資源集區是否可以嘗試使用其他主機資源來滿足配置要求。</span><span class="sxs-lookup"><span data-stu-id="21303-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21303-147">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="21303-147">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="21303-148">**不支援** (2) </span><span class="sxs-lookup"><span data-stu-id="21303-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="21303-149">**專用** (3) </span><span class="sxs-lookup"><span data-stu-id="21303-149">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="21303-150">**軟親和性** (4) </span><span class="sxs-lookup"><span data-stu-id="21303-150">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="21303-151">**硬性親和性** (5) </span><span class="sxs-lookup"><span data-stu-id="21303-151">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="21303-152">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="21303-152">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="21303-153">**廠商保留** (32767. 65535) </span><span class="sxs-lookup"><span data-stu-id="21303-153">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21303-154">**MappingOrder**</span><span class="sxs-lookup"><span data-stu-id="21303-154">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21303-155">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="21303-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="21303-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21303-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21303-157">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md)。**MappingBehavior**") </span><span class="sxs-lookup"><span data-stu-id="21303-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="21303-158">指定當嘗試滿足配置要求、無法使用要求的主機資源或未指定任何主機資源時，將會選取可透過此集區使用之主機資源的順序。</span><span class="sxs-lookup"><span data-stu-id="21303-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span>

</dd> <dt>

<span data-ttu-id="21303-159">**注意事項**</span><span class="sxs-lookup"><span data-stu-id="21303-159">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21303-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="21303-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21303-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21303-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21303-162">終端使用者提供的與此資源集區相關的附注。</span><span class="sxs-lookup"><span data-stu-id="21303-162">End-user supplied notes that are related to this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="21303-163">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="21303-163">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21303-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="21303-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21303-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21303-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21303-166">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ ResourcePool**](cim-resourcepool.md).**OtherResourceType**") </span><span class="sxs-lookup"><span data-stu-id="21303-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="21303-167">描述資源類型的字串，當無法使用定義完善的值，並將 **ResourceType** 設定為 0 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="21303-167">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="21303-168">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="21303-168">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21303-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="21303-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21303-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21303-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21303-171">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ ResourcePool**](cim-resourcepool.md).**PoolID**") </span><span class="sxs-lookup"><span data-stu-id="21303-171">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolID**")</span></span>
</dt> </dl>

<span data-ttu-id="21303-172">集區的識別碼。</span><span class="sxs-lookup"><span data-stu-id="21303-172">An identifier for the pool.</span></span> <span data-ttu-id="21303-173">這個屬性是用來提供將設定資料儲存和還原到基礎持續性儲存體之間的相互關聯。</span><span class="sxs-lookup"><span data-stu-id="21303-173">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="21303-174">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="21303-174">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21303-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="21303-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21303-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21303-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21303-177">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceSubType**") </span><span class="sxs-lookup"><span data-stu-id="21303-177">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="21303-178">字串，描述這個集區的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="21303-178">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="21303-179">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="21303-179">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="21303-180">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="21303-180">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21303-181">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="21303-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21303-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21303-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21303-183">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceType**") </span><span class="sxs-lookup"><span data-stu-id="21303-183">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="21303-184">此資源集區可以配置的資源類型。</span><span class="sxs-lookup"><span data-stu-id="21303-184">The type of resource this resource pool can allocate.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21303-185">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="21303-185">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="21303-186">**電腦系統** (2) </span><span class="sxs-lookup"><span data-stu-id="21303-186">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="21303-187">**處理器** (3) </span><span class="sxs-lookup"><span data-stu-id="21303-187">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="21303-188">**記憶體** (4) </span><span class="sxs-lookup"><span data-stu-id="21303-188">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="21303-189">**IDE 控制器** (5) </span><span class="sxs-lookup"><span data-stu-id="21303-189">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="21303-190">**平行 SCSI HBA** (6) </span><span class="sxs-lookup"><span data-stu-id="21303-190">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="21303-191">**FC HBA** (7) </span><span class="sxs-lookup"><span data-stu-id="21303-191">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="21303-192">**ISCSI HBA** (8) </span><span class="sxs-lookup"><span data-stu-id="21303-192">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="21303-193">**IB HCA** (9) </span><span class="sxs-lookup"><span data-stu-id="21303-193">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="21303-194">**乙太網路介面卡** (10) </span><span class="sxs-lookup"><span data-stu-id="21303-194">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="21303-195">**其他網路介面卡** (11) </span><span class="sxs-lookup"><span data-stu-id="21303-195">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="21303-196">**I/o 插槽** (12) </span><span class="sxs-lookup"><span data-stu-id="21303-196">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="21303-197"> (13) 的 **I/o 裝置**</span><span class="sxs-lookup"><span data-stu-id="21303-197">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="21303-198">**磁片磁碟機** (14) </span><span class="sxs-lookup"><span data-stu-id="21303-198">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="21303-199">**CD 光碟機** (15) </span><span class="sxs-lookup"><span data-stu-id="21303-199">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="21303-200">**DVD 光碟機** (16) </span><span class="sxs-lookup"><span data-stu-id="21303-200">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="21303-201">**磁片磁碟機** (17) </span><span class="sxs-lookup"><span data-stu-id="21303-201">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="21303-202">**磁帶機** (18) </span><span class="sxs-lookup"><span data-stu-id="21303-202">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="21303-203">**儲存體範圍** (19) </span><span class="sxs-lookup"><span data-stu-id="21303-203">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="21303-204">**其他存放裝置** (20) </span><span class="sxs-lookup"><span data-stu-id="21303-204">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="21303-205">**序列埠** (21) </span><span class="sxs-lookup"><span data-stu-id="21303-205">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="21303-206">**平行埠** (22) </span><span class="sxs-lookup"><span data-stu-id="21303-206">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="21303-207">**USB 控制器** (23) </span><span class="sxs-lookup"><span data-stu-id="21303-207">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="21303-208">**圖形控制器** (24) </span><span class="sxs-lookup"><span data-stu-id="21303-208">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="21303-209">**IEEE 1394 控制器** (25) </span><span class="sxs-lookup"><span data-stu-id="21303-209">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="21303-210">**可分割 Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="21303-210">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="21303-211">**基底可分割單位** (27) </span><span class="sxs-lookup"><span data-stu-id="21303-211">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="21303-212">**Power** (28) </span><span class="sxs-lookup"><span data-stu-id="21303-212">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="21303-213">**冷卻容量** (29) </span><span class="sxs-lookup"><span data-stu-id="21303-213">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="21303-214">**乙太網路交換器埠** (30) </span><span class="sxs-lookup"><span data-stu-id="21303-214">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="21303-215">**邏輯磁片** (31) </span><span class="sxs-lookup"><span data-stu-id="21303-215">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="21303-216">**存放磁片區** (32) </span><span class="sxs-lookup"><span data-stu-id="21303-216">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="21303-217">**Ethernet 連接** (33) </span><span class="sxs-lookup"><span data-stu-id="21303-217">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="21303-218">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="21303-218">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="21303-219">**廠商保留** (0x8000。0xFFFF) </span><span class="sxs-lookup"><span data-stu-id="21303-219">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="21303-220"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="21303-220"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="21303-221">規格需求</span><span class="sxs-lookup"><span data-stu-id="21303-221">Requirements</span></span>



| <span data-ttu-id="21303-222">需求</span><span class="sxs-lookup"><span data-stu-id="21303-222">Requirement</span></span> | <span data-ttu-id="21303-223">值</span><span class="sxs-lookup"><span data-stu-id="21303-223">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21303-224">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21303-224">Minimum supported client</span></span><br/> | <span data-ttu-id="21303-225">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21303-225">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="21303-226">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21303-226">Minimum supported server</span></span><br/> | <span data-ttu-id="21303-227">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21303-227">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="21303-228">命名空間</span><span class="sxs-lookup"><span data-stu-id="21303-228">Namespace</span></span><br/>                | <span data-ttu-id="21303-229">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="21303-229">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="21303-230">MOF</span><span class="sxs-lookup"><span data-stu-id="21303-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21303-231"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="21303-231"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="21303-232">DLL</span><span class="sxs-lookup"><span data-stu-id="21303-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21303-233"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="21303-233"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

