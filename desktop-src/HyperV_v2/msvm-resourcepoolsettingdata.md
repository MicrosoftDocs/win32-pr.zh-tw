---
description: 表示 \_ 非配置相關之 Msvm ResourcePool 實例的設定。
ms.assetid: 32e0066c-7e14-454c-8aa9-06e093ef8072
title: Msvm_ResourcePoolSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolSettingData
- Msvm_ResourcePoolSettingData.InstanceID
- Msvm_ResourcePoolSettingData.Caption
- Msvm_ResourcePoolSettingData.Description
- Msvm_ResourcePoolSettingData.ElementName
- Msvm_ResourcePoolSettingData.PoolID
- Msvm_ResourcePoolSettingData.ResourceType
- Msvm_ResourcePoolSettingData.OtherResourceType
- Msvm_ResourcePoolSettingData.ResourceSubType
- Msvm_ResourcePoolSettingData.LoadBalancingBehavior
- Msvm_ResourcePoolSettingData.MappingBehavior
- Msvm_ResourcePoolSettingData.MappingOrder
- Msvm_ResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37ec7dc6600dbc536ac50a2042e7d53ff8043242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983671"
---
# <a name="msvm_resourcepoolsettingdata-class"></a><span data-ttu-id="5c922-103">Msvm \_ ResourcePoolSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="5c922-103">Msvm\_ResourcePoolSettingData class</span></span>

<span data-ttu-id="5c922-104">表示非配置相關之 [**Msvm \_ ResourcePool**](msvm-resourcepool.md) 實例的設定。</span><span class="sxs-lookup"><span data-stu-id="5c922-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="5c922-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5c922-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c922-106">語法</span><span class="sxs-lookup"><span data-stu-id="5c922-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePoolSettingData : Msvm_AbstractResourcePoolSettingData
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

## <a name="members"></a><span data-ttu-id="5c922-107">成員</span><span class="sxs-lookup"><span data-stu-id="5c922-107">Members</span></span>

<span data-ttu-id="5c922-108">**Msvm \_ ResourcePoolSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5c922-108">The **Msvm\_ResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5c922-109">屬性</span><span class="sxs-lookup"><span data-stu-id="5c922-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c922-110">屬性</span><span class="sxs-lookup"><span data-stu-id="5c922-110">Properties</span></span>

<span data-ttu-id="5c922-111">**Msvm \_ ResourcePoolSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5c922-111">The **Msvm\_ResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c922-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="5c922-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c922-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c922-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c922-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c922-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c922-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="5c922-115">A short description of the object.</span></span> <span data-ttu-id="5c922-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5c922-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c922-117">**說明**</span><span class="sxs-lookup"><span data-stu-id="5c922-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c922-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c922-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c922-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c922-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c922-120">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="5c922-120">A description of the object.</span></span> <span data-ttu-id="5c922-121">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5c922-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c922-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5c922-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c922-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c922-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c922-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c922-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c922-125">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5c922-125">A display name for the object.</span></span> <span data-ttu-id="5c922-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5c922-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c922-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5c922-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c922-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c922-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c922-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c922-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c922-130">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="5c922-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5c922-131">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="5c922-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5c922-132">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="5c922-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c922-133">**LoadBalancingBehavior**</span><span class="sxs-lookup"><span data-stu-id="5c922-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c922-134">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c922-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c922-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c922-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c922-136">指定資源集區用來在其匯總資源之間平衡資源使用量的配置策略。</span><span class="sxs-lookup"><span data-stu-id="5c922-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span> <span data-ttu-id="5c922-137">這個屬性繼承自 [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md)。</span><span class="sxs-lookup"><span data-stu-id="5c922-137">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="5c922-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5c922-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (2) </span><span class="sxs-lookup"><span data-stu-id="5c922-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (3) </span><span class="sxs-lookup"><span data-stu-id="5c922-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**分散式** (4) </span><span class="sxs-lookup"><span data-stu-id="5c922-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Distributed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**合併** (5 ) </span><span class="sxs-lookup"><span data-stu-id="5c922-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Consolidated** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5c922-143">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="5c922-143">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c922-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c922-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c922-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c922-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c922-146">指定當無法配置所需的資源時，資源集區是否可以嘗試使用其他主機資源來滿足配置要求。</span><span class="sxs-lookup"><span data-stu-id="5c922-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span> <span data-ttu-id="5c922-147">這個屬性繼承自 [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md)。</span><span class="sxs-lookup"><span data-stu-id="5c922-147">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="5c922-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5c922-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (2) </span><span class="sxs-lookup"><span data-stu-id="5c922-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (3) </span><span class="sxs-lookup"><span data-stu-id="5c922-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**軟親和性** (4) </span><span class="sxs-lookup"><span data-stu-id="5c922-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**硬性親和性** (5) </span><span class="sxs-lookup"><span data-stu-id="5c922-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="5c922-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (32767. 65535 ) </span><span class="sxs-lookup"><span data-stu-id="5c922-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32767..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5c922-155">**MappingOrder**</span><span class="sxs-lookup"><span data-stu-id="5c922-155">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c922-156">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="5c922-156">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5c922-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c922-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c922-158">指定當嘗試滿足配置要求、無法使用要求的主機資源或未指定任何主機資源時，將會選取可透過此集區使用之主機資源的順序。</span><span class="sxs-lookup"><span data-stu-id="5c922-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span> <span data-ttu-id="5c922-159">這個屬性繼承自 [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md)。</span><span class="sxs-lookup"><span data-stu-id="5c922-159">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c922-160">**注意事項**</span><span class="sxs-lookup"><span data-stu-id="5c922-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c922-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c922-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c922-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c922-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c922-163">終端使用者提供的與此資源集區相關的附注。</span><span class="sxs-lookup"><span data-stu-id="5c922-163">End-user supplied notes that are related to this resource pool.</span></span> <span data-ttu-id="5c922-164">這個屬性繼承自 [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md)。</span><span class="sxs-lookup"><span data-stu-id="5c922-164">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c922-165">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="5c922-165">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c922-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c922-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c922-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c922-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c922-168">描述資源類型的字串，當無法使用定義完善的值，並將 **ResourceType** 設定為 0 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="5c922-168">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span> <span data-ttu-id="5c922-169">這個屬性繼承自 [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md)。</span><span class="sxs-lookup"><span data-stu-id="5c922-169">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c922-170">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="5c922-170">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c922-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c922-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c922-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c922-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c922-173">集區的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c922-173">An identifier for the pool.</span></span> <span data-ttu-id="5c922-174">這個屬性是用來提供將設定資料儲存和還原到基礎持續性儲存體之間的相互關聯。</span><span class="sxs-lookup"><span data-stu-id="5c922-174">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span> <span data-ttu-id="5c922-175">這個屬性繼承自 [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md)。</span><span class="sxs-lookup"><span data-stu-id="5c922-175">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c922-176">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="5c922-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c922-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c922-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c922-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c922-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c922-179">描述此集區之特定執行子類型的字串。</span><span class="sxs-lookup"><span data-stu-id="5c922-179">A string that describes an implementation-specific subtype for this pool.</span></span> <span data-ttu-id="5c922-180">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="5c922-180">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="5c922-181">這個屬性繼承自 [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md)。</span><span class="sxs-lookup"><span data-stu-id="5c922-181">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c922-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="5c922-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c922-183">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c922-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c922-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c922-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c922-185">此資源集區可以配置的資源類型。</span><span class="sxs-lookup"><span data-stu-id="5c922-185">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="5c922-186">這個屬性繼承自 [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md)。</span><span class="sxs-lookup"><span data-stu-id="5c922-186">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="5c922-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5c922-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**電腦系統** (2) </span><span class="sxs-lookup"><span data-stu-id="5c922-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**處理器** (3) </span><span class="sxs-lookup"><span data-stu-id="5c922-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**記憶體** (4) </span><span class="sxs-lookup"><span data-stu-id="5c922-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE 控制器** (5) </span><span class="sxs-lookup"><span data-stu-id="5c922-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**平行 SCSI HBA** (6) </span><span class="sxs-lookup"><span data-stu-id="5c922-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7) </span><span class="sxs-lookup"><span data-stu-id="5c922-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**ISCSI HBA** (8) </span><span class="sxs-lookup"><span data-stu-id="5c922-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9) </span><span class="sxs-lookup"><span data-stu-id="5c922-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**乙太網路介面卡** (10) </span><span class="sxs-lookup"><span data-stu-id="5c922-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**其他網路介面卡** (11) </span><span class="sxs-lookup"><span data-stu-id="5c922-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/o 插槽** (12) </span><span class="sxs-lookup"><span data-stu-id="5c922-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span> (13) 的 **I/o 裝置**</span><span class="sxs-lookup"><span data-stu-id="5c922-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**磁片磁碟機** (14) </span><span class="sxs-lookup"><span data-stu-id="5c922-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD 光碟機** (15) </span><span class="sxs-lookup"><span data-stu-id="5c922-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD 光碟機** (16) </span><span class="sxs-lookup"><span data-stu-id="5c922-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**磁片磁碟機** (17) </span><span class="sxs-lookup"><span data-stu-id="5c922-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**磁帶機** (18) </span><span class="sxs-lookup"><span data-stu-id="5c922-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**儲存體範圍** (19) </span><span class="sxs-lookup"><span data-stu-id="5c922-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**其他存放裝置** (20) </span><span class="sxs-lookup"><span data-stu-id="5c922-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**序列埠** (21) </span><span class="sxs-lookup"><span data-stu-id="5c922-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**平行埠** (22) </span><span class="sxs-lookup"><span data-stu-id="5c922-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB 控制器** (23) </span><span class="sxs-lookup"><span data-stu-id="5c922-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**圖形控制器** (24) </span><span class="sxs-lookup"><span data-stu-id="5c922-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 控制器** (25) </span><span class="sxs-lookup"><span data-stu-id="5c922-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**可分割 Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="5c922-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**基底可分割單位** (27) </span><span class="sxs-lookup"><span data-stu-id="5c922-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28) </span><span class="sxs-lookup"><span data-stu-id="5c922-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**冷卻容量** (29) </span><span class="sxs-lookup"><span data-stu-id="5c922-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**乙太網路交換器埠** (30) </span><span class="sxs-lookup"><span data-stu-id="5c922-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**邏輯磁片** (31) </span><span class="sxs-lookup"><span data-stu-id="5c922-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**存放磁片區** (32) </span><span class="sxs-lookup"><span data-stu-id="5c922-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet 連接** (33) </span><span class="sxs-lookup"><span data-stu-id="5c922-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="5c922-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5c922-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。0xFFFF ) </span><span class="sxs-lookup"><span data-stu-id="5c922-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c922-222">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c922-222">Requirements</span></span>



| <span data-ttu-id="5c922-223">需求</span><span class="sxs-lookup"><span data-stu-id="5c922-223">Requirement</span></span> | <span data-ttu-id="5c922-224">值</span><span class="sxs-lookup"><span data-stu-id="5c922-224">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c922-225">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c922-225">Minimum supported client</span></span><br/> | <span data-ttu-id="5c922-226">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c922-226">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5c922-227">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c922-227">Minimum supported server</span></span><br/> | <span data-ttu-id="5c922-228">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c922-228">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5c922-229">命名空間</span><span class="sxs-lookup"><span data-stu-id="5c922-229">Namespace</span></span><br/>                | <span data-ttu-id="5c922-230">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="5c922-230">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5c922-231">MOF</span><span class="sxs-lookup"><span data-stu-id="5c922-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c922-232"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5c922-232"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c922-233">DLL</span><span class="sxs-lookup"><span data-stu-id="5c922-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c922-234"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5c922-234"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

