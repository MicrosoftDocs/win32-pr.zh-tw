---
description: 管理 \_ cim ResourcePool 物件之 cim ResourcePoolConfigurationService 實例的功能 \_ 。
ms.assetid: bd2eb4da-8ecd-4adb-b657-837c8da4dcdc
title: CIM_ResourcePoolConfigurationCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationCapabilities
- CIM_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- CIM_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 967b307049fa9c5f81b8deb6da96bcaa3be9acc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974066"
---
# <a name="cim_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="6c6ef-103">CIM \_ ResourcePoolConfigurationCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="6c6ef-103">CIM\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="6c6ef-104">管理 [**cim \_ ResourcePool**](cim-resourcepool.md)物件之 [**cim \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md)實例的功能。</span><span class="sxs-lookup"><span data-stu-id="6c6ef-104">Manages the capabilities of the [**CIM\_ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md) instance for a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6ef-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c6ef-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="6c6ef-106">成員</span><span class="sxs-lookup"><span data-stu-id="6c6ef-106">Members</span></span>

<span data-ttu-id="6c6ef-107">**CIM \_ ResourcePoolConfigurationCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6c6ef-107">The **CIM\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="6c6ef-108">屬性</span><span class="sxs-lookup"><span data-stu-id="6c6ef-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c6ef-109">屬性</span><span class="sxs-lookup"><span data-stu-id="6c6ef-109">Properties</span></span>

<span data-ttu-id="6c6ef-110">**CIM \_ ResourcePoolConfigurationCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6c6ef-110">The **CIM\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c6ef-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c6ef-112">資料類型： **uint32** 陣列</span><span class="sxs-lookup"><span data-stu-id="6c6ef-112">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="6c6ef-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c6ef-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c6ef-114">支援非同步作業的設定服務方法。</span><span class="sxs-lookup"><span data-stu-id="6c6ef-114">The methods of the configuration service that are supported for asynchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="6c6ef-115"> (2) **支援 CreateResourcePool**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-115">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="6c6ef-116"> (3) **支援 CreateChild ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-116">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="6c6ef-117"> (4) **支援 DeleteResourcePool**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-117">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="6c6ef-118"> (5) **支援 AddResourcesToResourcePool**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-118">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="6c6ef-119"> (6) **支援 RemoveResourcesFromResourcePool**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-119">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangeParentResourcePool_is_supported"></span><span id="changeparentresourcepool_is_supported"></span><span id="CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="6c6ef-120"> (7) **支援 ChangeParentResourcePool**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-120">**ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6c6ef-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="6c6ef-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="6c6ef-122">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="6c6ef-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6c6ef-123">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-123">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c6ef-124">資料類型： **uint32** 陣列</span><span class="sxs-lookup"><span data-stu-id="6c6ef-124">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="6c6ef-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c6ef-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c6ef-126">支援同步作業的設定服務方法。</span><span class="sxs-lookup"><span data-stu-id="6c6ef-126">The methods of the configuration service that are supported for synchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="6c6ef-127"> (2) **支援 CreateResourcePool**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-127">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="6c6ef-128"> (3) **支援 CreateChild ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-128">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="6c6ef-129"> (4) **支援 DeleteResourcePool**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-129">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="6c6ef-130"> (5) **支援 AddResourcesToResourcePool**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-130">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="6c6ef-131"> (6) **支援 RemoveResourcesFromResourcePool**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-131">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CIM_ChangeParentResourcePool_is_supported"></span><span id="cim_changeparentresourcepool_is_supported"></span><span id="CIM_CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="6c6ef-132">**CIM \_** (7) 支援 ChangeParentResourcePool</span><span class="sxs-lookup"><span data-stu-id="6c6ef-132">**CIM\_ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6c6ef-133">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="6c6ef-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="6c6ef-134">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="6c6ef-134">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="6c6ef-135"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6c6ef-135"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="6c6ef-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c6ef-136">Requirements</span></span>



| <span data-ttu-id="6c6ef-137">需求</span><span class="sxs-lookup"><span data-stu-id="6c6ef-137">Requirement</span></span> | <span data-ttu-id="6c6ef-138">值</span><span class="sxs-lookup"><span data-stu-id="6c6ef-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6ef-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c6ef-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6c6ef-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6c6ef-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6c6ef-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c6ef-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6c6ef-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6c6ef-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6c6ef-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="6c6ef-143">Namespace</span></span><br/>                | <span data-ttu-id="6c6ef-144">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="6c6ef-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6c6ef-145">MOF</span><span class="sxs-lookup"><span data-stu-id="6c6ef-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c6ef-146"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6c6ef-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c6ef-147">DLL</span><span class="sxs-lookup"><span data-stu-id="6c6ef-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c6ef-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6c6ef-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6c6ef-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c6ef-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6ef-150">**CIM \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="6c6ef-150">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

 




