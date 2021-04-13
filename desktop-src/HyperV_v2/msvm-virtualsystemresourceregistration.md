---
description: 註冊可提供虛擬機器特定資源相關物件的服務。
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Msvm_VirtualSystemResourceRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510991"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a><span data-ttu-id="0c48e-103">Msvm \_ VirtualSystemResourceRegistration 類別</span><span class="sxs-lookup"><span data-stu-id="0c48e-103">Msvm\_VirtualSystemResourceRegistration class</span></span>

<span data-ttu-id="0c48e-104">註冊可提供虛擬機器特定資源相關物件的服務。</span><span class="sxs-lookup"><span data-stu-id="0c48e-104">Registers a service that provides virtual machine-specific resource-related objects.</span></span>

<span data-ttu-id="0c48e-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0c48e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c48e-106">語法</span><span class="sxs-lookup"><span data-stu-id="0c48e-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a><span data-ttu-id="0c48e-107">成員</span><span class="sxs-lookup"><span data-stu-id="0c48e-107">Members</span></span>

<span data-ttu-id="0c48e-108">**Msvm \_ VirtualSystemResourceRegistration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0c48e-108">The **Msvm\_VirtualSystemResourceRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="0c48e-109">屬性</span><span class="sxs-lookup"><span data-stu-id="0c48e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c48e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0c48e-110">Properties</span></span>

<span data-ttu-id="0c48e-111">**Msvm \_ VirtualSystemResourceRegistration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0c48e-111">The **Msvm\_VirtualSystemResourceRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c48e-112">**元件**</span><span class="sxs-lookup"><span data-stu-id="0c48e-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c48e-113">資料類型： **[ **Msvm \_ VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="0c48e-113">Data type: **[**Msvm\_VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="0c48e-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c48e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c48e-115">實例的參考，該實例描述實此類別的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c48e-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="0c48e-116">**IsRootDevice**</span><span class="sxs-lookup"><span data-stu-id="0c48e-116">**IsRootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c48e-117">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0c48e-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c48e-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c48e-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c48e-119">如果這個註冊指出指定的資源類型是此服務的根 (或不是父系的) 裝置，則為 **True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="0c48e-119">**True** if this registration indicates whether the specified resource type is the root (or parent-less) device for this service; otherwise, **False**.</span></span> <span data-ttu-id="0c48e-120">當 **IsRootDevice** 設定為 **True** 時，只有一個註冊可以存在。</span><span class="sxs-lookup"><span data-stu-id="0c48e-120">Only one registration can exist when **IsRootDevice** is set to **True**.</span></span> <span data-ttu-id="0c48e-121">否則，此註冊代表子裝置的對應。</span><span class="sxs-lookup"><span data-stu-id="0c48e-121">Otherwise, this registration represents a mapping to a sub-device.</span></span> <span data-ttu-id="0c48e-122">此屬性一律設為 **False**。</span><span class="sxs-lookup"><span data-stu-id="0c48e-122">This property is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="0c48e-123">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="0c48e-123">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c48e-124">資料類型： **[ **Msvm \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="0c48e-124">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="0c48e-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c48e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c48e-126">描述服務所支援之資源類型之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="0c48e-126">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="0c48e-127">這個屬性繼承自 [**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="0c48e-127">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c48e-128">備註</span><span class="sxs-lookup"><span data-stu-id="0c48e-128">Remarks</span></span>

<span data-ttu-id="0c48e-129">存取 **Msvm \_ VirtualSystemResourceRegistration** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="0c48e-129">Access to the **Msvm\_VirtualSystemResourceRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0c48e-130">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="0c48e-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c48e-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c48e-131">Requirements</span></span>



| <span data-ttu-id="0c48e-132">需求</span><span class="sxs-lookup"><span data-stu-id="0c48e-132">Requirement</span></span> | <span data-ttu-id="0c48e-133">值</span><span class="sxs-lookup"><span data-stu-id="0c48e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c48e-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c48e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0c48e-135">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c48e-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0c48e-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c48e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0c48e-137">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c48e-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c48e-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0c48e-138">End of client support</span></span><br/>    | <span data-ttu-id="0c48e-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0c48e-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0c48e-140">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="0c48e-140">End of server support</span></span><br/>    | <span data-ttu-id="0c48e-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0c48e-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0c48e-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="0c48e-142">Namespace</span></span><br/>                | <span data-ttu-id="0c48e-143">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="0c48e-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0c48e-144">MOF</span><span class="sxs-lookup"><span data-stu-id="0c48e-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c48e-145"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0c48e-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c48e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0c48e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c48e-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c48e-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0c48e-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c48e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c48e-149">**Msvm \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="0c48e-149">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="0c48e-150">**Msvm \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="0c48e-150">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

