---
description: 描述相關聯 Msvm \_ ResourcePoolConfigurationService 類別的功能。
ms.assetid: 3e6857f9-62a0-420b-8f1d-8aad685a7ff7
title: Msvm_ResourcePoolConfigurationCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationCapabilities
- Msvm_ResourcePoolConfigurationCapabilities.InstanceID
- Msvm_ResourcePoolConfigurationCapabilities.Caption
- Msvm_ResourcePoolConfigurationCapabilities.Description
- Msvm_ResourcePoolConfigurationCapabilities.ElementName
- Msvm_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- Msvm_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b70d9e84e2c85d4c5b702a638982df0b47d62193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849995"
---
# <a name="msvm_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="5b193-103">Msvm \_ ResourcePoolConfigurationCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="5b193-103">Msvm\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="5b193-104">描述相關聯 [**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) 類別的功能。</span><span class="sxs-lookup"><span data-stu-id="5b193-104">Describes the capabilities of the associated [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class.</span></span> <span data-ttu-id="5b193-105">用戶端可以使用這個類別的實例，判斷哪些方法會以同步或非同步方式支援。</span><span class="sxs-lookup"><span data-stu-id="5b193-105">Clients can use instances of this class to determine which methods are supported synchronously or asynchronously.</span></span> <span data-ttu-id="5b193-106">這兩個清單中都不能有相同的方法。</span><span class="sxs-lookup"><span data-stu-id="5b193-106">The same method must not be in both lists.</span></span> <span data-ttu-id="5b193-107">方法實現必須是同步或非同步。</span><span class="sxs-lookup"><span data-stu-id="5b193-107">Method implementations must either be synchronous or asynchronous.</span></span>

<span data-ttu-id="5b193-108">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5b193-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b193-109">語法</span><span class="sxs-lookup"><span data-stu-id="5b193-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = "Resource Pool Configuration Capabilities";
  string Description = "Microsoft Resource Pool Configuration Capabilities";
  string ElementName = "Resource Pool Configuration Capabilities";
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="5b193-110">成員</span><span class="sxs-lookup"><span data-stu-id="5b193-110">Members</span></span>

<span data-ttu-id="5b193-111">**Msvm \_ ResourcePoolConfigurationCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5b193-111">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="5b193-112">屬性</span><span class="sxs-lookup"><span data-stu-id="5b193-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b193-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5b193-113">Properties</span></span>

<span data-ttu-id="5b193-114">**Msvm \_ ResourcePoolConfigurationCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5b193-114">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b193-115">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="5b193-115">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b193-116">資料類型： **uint32** 陣列</span><span class="sxs-lookup"><span data-stu-id="5b193-116">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="5b193-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b193-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b193-118">方法識別碼的陣列，每個都識別 [**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) 類別的方法，此方法是由實作為非同步支援。</span><span class="sxs-lookup"><span data-stu-id="5b193-118">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5b193-119">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="5b193-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="5b193-120"> (32768 **支援 >batchclient.pooloperations.createpool**) </span><span class="sxs-lookup"><span data-stu-id="5b193-120">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="5b193-121"> (32769 **支援 ChangePoolResources**) </span><span class="sxs-lookup"><span data-stu-id="5b193-121">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="5b193-122"> (32770 **支援 ChangePoolSettings**) </span><span class="sxs-lookup"><span data-stu-id="5b193-122">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="5b193-123"> (32771 **支援 DeletePool**) </span><span class="sxs-lookup"><span data-stu-id="5b193-123">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="5b193-124">**廠商保留** (32772： 65535) </span><span class="sxs-lookup"><span data-stu-id="5b193-124">**Vendor Reserved** (32772..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b193-125">**標題**</span><span class="sxs-lookup"><span data-stu-id="5b193-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b193-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b193-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b193-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b193-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b193-128">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="5b193-128">A short description of the object.</span></span> <span data-ttu-id="5b193-129">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「資源集區設定功能」。</span><span class="sxs-lookup"><span data-stu-id="5b193-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="5b193-130">**說明**</span><span class="sxs-lookup"><span data-stu-id="5b193-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b193-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b193-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b193-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b193-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b193-133">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="5b193-133">A description of the object.</span></span> <span data-ttu-id="5b193-134">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 資源集區設定功能」。</span><span class="sxs-lookup"><span data-stu-id="5b193-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="5b193-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5b193-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b193-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b193-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b193-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b193-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b193-138">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5b193-138">A display name for the object.</span></span> <span data-ttu-id="5b193-139">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「資源集區設定功能」。</span><span class="sxs-lookup"><span data-stu-id="5b193-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="5b193-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5b193-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b193-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b193-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b193-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b193-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b193-143">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="5b193-143">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5b193-144">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="5b193-144">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5b193-145">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5b193-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5b193-146">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="5b193-146">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b193-147">資料類型： **uint32** 陣列</span><span class="sxs-lookup"><span data-stu-id="5b193-147">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="5b193-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b193-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b193-149">方法識別碼的陣列，每個都識別 [**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) 類別的方法，此方法會由實作為同步支援。</span><span class="sxs-lookup"><span data-stu-id="5b193-149">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5b193-150">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="5b193-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="5b193-151"> (32768 **支援 >batchclient.pooloperations.createpool**) </span><span class="sxs-lookup"><span data-stu-id="5b193-151">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="5b193-152"> (32769 **支援 ChangePoolResources**) </span><span class="sxs-lookup"><span data-stu-id="5b193-152">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="5b193-153"> (32770 **支援 ChangePoolSettings**) </span><span class="sxs-lookup"><span data-stu-id="5b193-153">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="5b193-154"> (32771 **支援 DeletePool**) </span><span class="sxs-lookup"><span data-stu-id="5b193-154">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="5b193-155">**廠商保留** (32772： 65535) </span><span class="sxs-lookup"><span data-stu-id="5b193-155">**Vendor Reserved** (32772..65535)</span></span>


<span data-ttu-id="5b193-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5b193-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5b193-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b193-157">Requirements</span></span>



| <span data-ttu-id="5b193-158">需求</span><span class="sxs-lookup"><span data-stu-id="5b193-158">Requirement</span></span> | <span data-ttu-id="5b193-159">值</span><span class="sxs-lookup"><span data-stu-id="5b193-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b193-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b193-160">Minimum supported client</span></span><br/> | <span data-ttu-id="5b193-161">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b193-161">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5b193-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b193-162">Minimum supported server</span></span><br/> | <span data-ttu-id="5b193-163">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b193-163">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5b193-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="5b193-164">Namespace</span></span><br/>                | <span data-ttu-id="5b193-165">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="5b193-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5b193-166">MOF</span><span class="sxs-lookup"><span data-stu-id="5b193-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b193-167"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5b193-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b193-168">DLL</span><span class="sxs-lookup"><span data-stu-id="5b193-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b193-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5b193-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

