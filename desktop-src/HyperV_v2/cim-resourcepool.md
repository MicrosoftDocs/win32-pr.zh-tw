---
description: 代表資源集區，這是主機系統提供來配置和指派資源的邏輯實體。
ms.assetid: c8e0b701-1814-4409-a073-017f8fea841a
title: CIM_ResourcePool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePool
- CIM_ResourcePool.InstanceID
- CIM_ResourcePool.PoolID
- CIM_ResourcePool.Primordial
- CIM_ResourcePool.Capacity
- CIM_ResourcePool.Reserved
- CIM_ResourcePool.ResourceType
- CIM_ResourcePool.OtherResourceType
- CIM_ResourcePool.ResourceSubType
- CIM_ResourcePool.AllocationUnits
- CIM_ResourcePool.ConsumedResourceUnits
- CIM_ResourcePool.CurrentlyConsumedResource
- CIM_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11a073f817da27dbbd45be26a008486a776470cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113577"
---
# <a name="cim_resourcepool-class"></a><span data-ttu-id="1ed59-103">CIM \_ ResourcePool 類別</span><span class="sxs-lookup"><span data-stu-id="1ed59-103">CIM\_ResourcePool class</span></span>

<span data-ttu-id="1ed59-104">代表資源集區，這是主機系統提供來配置和指派資源的邏輯實體。</span><span class="sxs-lookup"><span data-stu-id="1ed59-104">Represents a resource pool, which is a logical entity provided by the host system to allocate and assign resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed59-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ed59-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourcePool : CIM_LogicalElement
{
  string  InstanceID;
  string  PoolID;
  boolean Primordial = FALSE;
  uint64  Capacity;
  uint64  Reserved;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  AllocationUnits;
  string  ConsumedResourceUnits = "count";
  uint64  CurrentlyConsumedResource;
  uint64  MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="1ed59-106">成員</span><span class="sxs-lookup"><span data-stu-id="1ed59-106">Members</span></span>

<span data-ttu-id="1ed59-107">**CIM \_ ResourcePool** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1ed59-107">The **CIM\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="1ed59-108">屬性</span><span class="sxs-lookup"><span data-stu-id="1ed59-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ed59-109">屬性</span><span class="sxs-lookup"><span data-stu-id="1ed59-109">Properties</span></span>

<span data-ttu-id="1ed59-110">**CIM \_ ResourcePool** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1ed59-110">The **CIM\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ed59-111">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="1ed59-111">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-112">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ed59-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ed59-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-114">限定詞： **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="1ed59-114">Qualifiers: **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-115">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="1ed59-115">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="1ed59-116">例如，當 **ResourceType** 設定為 "Processor" 時， **AllocationUnits** 可以設定為 "赫茲 \* 10 ^ 6" 或 "percent"。</span><span class="sxs-lookup"><span data-stu-id="1ed59-116">For example, when **ResourceType** is set to "Processor", **AllocationUnits** may be set to "hertz\*10^6" or "percent".</span></span> <span data-ttu-id="1ed59-117">這個屬性的值應該是 *DSP0004 2.4* 或更新版本的附錄 C. 1 的程式設計單位辨識符號合法值。</span><span class="sxs-lookup"><span data-stu-id="1ed59-117">The value of this property should be a legal value of the Programmatic Units qualifier from Appendix C.1 of *DSP0004 V2.4* or later.</span></span>

</dd> <dt>

<span data-ttu-id="1ed59-118">**容量**</span><span class="sxs-lookup"><span data-stu-id="1ed59-118">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-119">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1ed59-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ed59-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-121">資源集區可支援的最大保留量。</span><span class="sxs-lookup"><span data-stu-id="1ed59-121">The maximum amount of reservations that the resource pool can support.</span></span> <span data-ttu-id="1ed59-122">**AllocationUnits** 屬性會指定單位類型。</span><span class="sxs-lookup"><span data-stu-id="1ed59-122">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="1ed59-123">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="1ed59-123">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ed59-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ed59-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-126">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourcePool**.**MaxConsumableResource**"，"**CIM \_ ResourcePool**.**CurrentlyConsumedResource**") ， **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="1ed59-126">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**MaxConsumableResource**", "**CIM\_ResourcePool**.**CurrentlyConsumedResource**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-127">**MaxConsumable** 的單位和已 **使用** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ed59-127">The units for the **MaxConsumable** and the **Consumed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="1ed59-128">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="1ed59-128">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-129">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1ed59-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ed59-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-131">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourcePool**.**ConsumedResourceUnits**") </span><span class="sxs-lookup"><span data-stu-id="1ed59-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-132">資源集區目前呈現給資源取用者的資源數量。</span><span class="sxs-lookup"><span data-stu-id="1ed59-132">The amount of resource that the resource pool currently presents to resource consumers.</span></span> <span data-ttu-id="1ed59-133">這個屬性與 **保留** 的屬性不同，因為它會描述資源的取用者觀點，而 **保留** 的屬性會描述資源的產生者觀點。</span><span class="sxs-lookup"><span data-stu-id="1ed59-133">This property is different from the **Reserved** property because it describes the consumers view of the resource while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="1ed59-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1ed59-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ed59-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ed59-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-137">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "InstanceID" ) </span><span class="sxs-lookup"><span data-stu-id="1ed59-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-138">在包含的命名空間範圍內唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="1ed59-138">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="1ed59-139">為了確保命名空間中的唯一性， **InstanceID** 屬性的值應該以下列模式來建立： *OrgID*：*LocalID*</span><span class="sxs-lookup"><span data-stu-id="1ed59-139">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="1ed59-140">*OrgID* 必須包含受著作權、商標或其他唯一的名稱，該名稱是由定義 **InstanceID** 屬性的商業實體所擁有，或是由可辨識的全域授權單位指派的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ed59-140">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="1ed59-141">*OrgID* 不能包含冒號。</span><span class="sxs-lookup"><span data-stu-id="1ed59-141">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="1ed59-142">**InstanceID** 中的第一個冒號必須介於 *OrgID* 和 *LocalID* 之間。</span><span class="sxs-lookup"><span data-stu-id="1ed59-142">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="1ed59-143">*LocalID* 是由商務實體所選擇，不應重新使用以識別不同的基礎現實世界元素。</span><span class="sxs-lookup"><span data-stu-id="1ed59-143">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="1ed59-144">如果未使用上述模式，則定義實體必須確保產生的 **instanceid** 值不會重複用於這個提供者所產生之任何 **instanceid** 屬性或這個命名空間的其他提供者。</span><span class="sxs-lookup"><span data-stu-id="1ed59-144">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="1ed59-145">針對已定義的 DMTF 實例，必須搭配 *OrgID* 設定為 "CIM" 的模式使用。</span><span class="sxs-lookup"><span data-stu-id="1ed59-145">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> <dt>

<span data-ttu-id="1ed59-146">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="1ed59-146">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-147">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1ed59-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ed59-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-149">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourcePool**.**ConsumedResourceUnits**") </span><span class="sxs-lookup"><span data-stu-id="1ed59-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-150">資源集區可呈現給資源取用者的可耗用資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="1ed59-150">The maximum of amount of consumable resources that the resource pool can present to resource consumers.</span></span> <span data-ttu-id="1ed59-151">這個屬性與 [ **容量** ] 屬性不同，因為它會描述資源的取用者觀點，而 [ **容量** ] 屬性則會描述資源的生產者視圖。</span><span class="sxs-lookup"><span data-stu-id="1ed59-151">This property is different from the **Capacity** property because it describes the consumers view of the resource while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="1ed59-152">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="1ed59-152">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ed59-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ed59-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-155">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourcePool**.**ResourceType**") </span><span class="sxs-lookup"><span data-stu-id="1ed59-155">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-156">**ResourceType** 屬性設定為 "0" (其他) 的資源類型。</span><span class="sxs-lookup"><span data-stu-id="1ed59-156">The resource type when the **ResourceType** property is set to "0" (other).</span></span>

</dd> <dt>

<span data-ttu-id="1ed59-157">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="1ed59-157">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ed59-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ed59-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-160">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**") </span><span class="sxs-lookup"><span data-stu-id="1ed59-160">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-161">集區不透明的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ed59-161">An opaque identifier for the pool.</span></span> <span data-ttu-id="1ed59-162">這個屬性是用來在儲存和還原設定資料到基礎持續性儲存體時提供相互關聯。</span><span class="sxs-lookup"><span data-stu-id="1ed59-162">This property is used to provide correlation when saving and restoring configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="1ed59-163">**原始**</span><span class="sxs-lookup"><span data-stu-id="1ed59-163">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-164">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ed59-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ed59-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-166">如果資源集區是原始的，**則為 true** 。</span><span class="sxs-lookup"><span data-stu-id="1ed59-166">**true** if the resource pool is primordial.</span></span> <span data-ttu-id="1ed59-167">如果資源集區是實體資源集區，則 **為 false** 。</span><span class="sxs-lookup"><span data-stu-id="1ed59-167">**false** if the resource pool is a concrete resource pool.</span></span> <span data-ttu-id="1ed59-168">原始資源集區是資源的取用者未建立或刪除的資源集區。</span><span class="sxs-lookup"><span data-stu-id="1ed59-168">A primordial resource pool is a resource pool that is not created or deleted by consumers of the resource.</span></span> <span data-ttu-id="1ed59-169">資源配置服務可以更新實體資源集區。</span><span class="sxs-lookup"><span data-stu-id="1ed59-169">A concrete resource pool can be updated by resource allocation services.</span></span>

</dd> <dt>

<span data-ttu-id="1ed59-170">**已保留**</span><span class="sxs-lookup"><span data-stu-id="1ed59-170">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-171">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1ed59-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ed59-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-173">從這個集區到所有使用中配置的目前保留數目。</span><span class="sxs-lookup"><span data-stu-id="1ed59-173">The current number of reservations spread across all active allocations from this pool.</span></span> <span data-ttu-id="1ed59-174">在階層式設定中，這代表所有目前下階保留專案的總和。</span><span class="sxs-lookup"><span data-stu-id="1ed59-174">In a hierarchical configuration, this represents the sum of all current descendant reservations.</span></span> <span data-ttu-id="1ed59-175">**AllocationUnits** 屬性會指定單位類型。</span><span class="sxs-lookup"><span data-stu-id="1ed59-175">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="1ed59-176">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="1ed59-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ed59-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ed59-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-179">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourcePool**.**ResourceType**") </span><span class="sxs-lookup"><span data-stu-id="1ed59-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-180">資源集區的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="1ed59-180">The implementation specific sub-type for the resource pool.</span></span> <span data-ttu-id="1ed59-181">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="1ed59-181">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="1ed59-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="1ed59-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-183">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ed59-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ed59-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-185">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourcePool**.**OtherResourceType**"，"**CIM \_ ResourcePool**.**ResourceSubType**") </span><span class="sxs-lookup"><span data-stu-id="1ed59-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**OtherResourceType**", "**CIM\_ResourcePool**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-186">資源集區所配置的資源類型。</span><span class="sxs-lookup"><span data-stu-id="1ed59-186">The type of resource allocated by the resource pool.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1ed59-187">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1ed59-187">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="1ed59-188">**電腦系統** (2) </span><span class="sxs-lookup"><span data-stu-id="1ed59-188">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="1ed59-189">**處理器** (3) </span><span class="sxs-lookup"><span data-stu-id="1ed59-189">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="1ed59-190">**記憶體** (4) </span><span class="sxs-lookup"><span data-stu-id="1ed59-190">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="1ed59-191">**IDE 控制器** (5) </span><span class="sxs-lookup"><span data-stu-id="1ed59-191">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="1ed59-192">**平行 SCSI HBA** (6) </span><span class="sxs-lookup"><span data-stu-id="1ed59-192">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="1ed59-193">**FC HBA** (7) </span><span class="sxs-lookup"><span data-stu-id="1ed59-193">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="1ed59-194">**ISCSI HBA** (8) </span><span class="sxs-lookup"><span data-stu-id="1ed59-194">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="1ed59-195">**IB HCA** (9) </span><span class="sxs-lookup"><span data-stu-id="1ed59-195">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="1ed59-196">**乙太網路介面卡** (10) </span><span class="sxs-lookup"><span data-stu-id="1ed59-196">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="1ed59-197">**其他網路介面卡** (11) </span><span class="sxs-lookup"><span data-stu-id="1ed59-197">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="1ed59-198">**I/o 插槽** (12) </span><span class="sxs-lookup"><span data-stu-id="1ed59-198">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="1ed59-199"> (13) 的 **I/o 裝置**</span><span class="sxs-lookup"><span data-stu-id="1ed59-199">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="1ed59-200">**磁片磁碟機** (14) </span><span class="sxs-lookup"><span data-stu-id="1ed59-200">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="1ed59-201">**CD 光碟機** (15) </span><span class="sxs-lookup"><span data-stu-id="1ed59-201">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="1ed59-202">**DVD 光碟機** (16) </span><span class="sxs-lookup"><span data-stu-id="1ed59-202">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="1ed59-203">**磁片磁碟機** (17) </span><span class="sxs-lookup"><span data-stu-id="1ed59-203">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="1ed59-204">**磁帶機** (18) </span><span class="sxs-lookup"><span data-stu-id="1ed59-204">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="1ed59-205">**儲存體範圍** (19) </span><span class="sxs-lookup"><span data-stu-id="1ed59-205">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="1ed59-206">**其他存放裝置** (20) </span><span class="sxs-lookup"><span data-stu-id="1ed59-206">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="1ed59-207">**序列埠** (21) </span><span class="sxs-lookup"><span data-stu-id="1ed59-207">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="1ed59-208">**平行埠** (22) </span><span class="sxs-lookup"><span data-stu-id="1ed59-208">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="1ed59-209">**USB 控制器** (23) </span><span class="sxs-lookup"><span data-stu-id="1ed59-209">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="1ed59-210">**圖形控制器** (24) </span><span class="sxs-lookup"><span data-stu-id="1ed59-210">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="1ed59-211">**IEEE 1394 控制器** (25) </span><span class="sxs-lookup"><span data-stu-id="1ed59-211">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="1ed59-212">**可分割 Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="1ed59-212">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="1ed59-213">**基底可分割單位** (27) </span><span class="sxs-lookup"><span data-stu-id="1ed59-213">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="1ed59-214">**Power** (28) </span><span class="sxs-lookup"><span data-stu-id="1ed59-214">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="1ed59-215">**冷卻容量** (29) </span><span class="sxs-lookup"><span data-stu-id="1ed59-215">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="1ed59-216">**乙太網路交換器埠** (30) </span><span class="sxs-lookup"><span data-stu-id="1ed59-216">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="1ed59-217">**邏輯磁片** (31) </span><span class="sxs-lookup"><span data-stu-id="1ed59-217">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="1ed59-218">**存放磁片區** (32) </span><span class="sxs-lookup"><span data-stu-id="1ed59-218">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="1ed59-219">**Ethernet 連接** (33) </span><span class="sxs-lookup"><span data-stu-id="1ed59-219">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1ed59-220">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="1ed59-220">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1ed59-221">**廠商保留** (0x8000。0xFFFF) </span><span class="sxs-lookup"><span data-stu-id="1ed59-221">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="1ed59-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1ed59-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1ed59-223">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ed59-223">Requirements</span></span>



| <span data-ttu-id="1ed59-224">需求</span><span class="sxs-lookup"><span data-stu-id="1ed59-224">Requirement</span></span> | <span data-ttu-id="1ed59-225">值</span><span class="sxs-lookup"><span data-stu-id="1ed59-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed59-226">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ed59-226">Minimum supported client</span></span><br/> | <span data-ttu-id="1ed59-227">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1ed59-227">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1ed59-228">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ed59-228">Minimum supported server</span></span><br/> | <span data-ttu-id="1ed59-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ed59-229">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1ed59-230">命名空間</span><span class="sxs-lookup"><span data-stu-id="1ed59-230">Namespace</span></span><br/>                | <span data-ttu-id="1ed59-231">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="1ed59-231">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1ed59-232">MOF</span><span class="sxs-lookup"><span data-stu-id="1ed59-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ed59-233"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1ed59-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ed59-234">DLL</span><span class="sxs-lookup"><span data-stu-id="1ed59-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ed59-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ed59-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ed59-236">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ed59-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed59-237">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="1ed59-237">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

