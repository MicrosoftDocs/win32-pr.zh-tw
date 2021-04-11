---
description: 註冊提供全域資源集區相關物件的服務。
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Msvm_ResourcePoolRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolRegistration
- Msvm_ResourcePoolRegistration.ResourceType
- Msvm_ResourcePoolRegistration.Component
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6eecfefc8c542eeb3a06c509533060f8036d447e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115724"
---
# <a name="msvm_resourcepoolregistration-class"></a><span data-ttu-id="841c4-103">Msvm \_ ResourcePoolRegistration 類別</span><span class="sxs-lookup"><span data-stu-id="841c4-103">Msvm\_ResourcePoolRegistration class</span></span>

<span data-ttu-id="841c4-104">註冊提供全域資源集區相關物件的服務。</span><span class="sxs-lookup"><span data-stu-id="841c4-104">Registers a service that provides global resource pool-related objects.</span></span>

<span data-ttu-id="841c4-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="841c4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="841c4-106">語法</span><span class="sxs-lookup"><span data-stu-id="841c4-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a><span data-ttu-id="841c4-107">成員</span><span class="sxs-lookup"><span data-stu-id="841c4-107">Members</span></span>

<span data-ttu-id="841c4-108">**Msvm \_ ResourcePoolRegistration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="841c4-108">The **Msvm\_ResourcePoolRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="841c4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="841c4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="841c4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="841c4-110">Properties</span></span>

<span data-ttu-id="841c4-111">**Msvm \_ ResourcePoolRegistration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="841c4-111">The **Msvm\_ResourcePoolRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="841c4-112">**元件**</span><span class="sxs-lookup"><span data-stu-id="841c4-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841c4-113">資料類型： **[ **Msvm \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="841c4-113">Data type: **[**Msvm\_ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="841c4-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="841c4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="841c4-115">實例的參考，該實例描述實此類別的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="841c4-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="841c4-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="841c4-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841c4-117">資料類型： **[ **Msvm \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="841c4-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="841c4-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="841c4-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="841c4-119">描述服務所支援之資源類型之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="841c4-119">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="841c4-120">這個屬性繼承自 [**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="841c4-120">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="841c4-121">備註</span><span class="sxs-lookup"><span data-stu-id="841c4-121">Remarks</span></span>

<span data-ttu-id="841c4-122">存取 **Msvm \_ ResourcePoolRegistration** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="841c4-122">Access to the **Msvm\_ResourcePoolRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="841c4-123">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="841c4-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="841c4-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="841c4-124">Requirements</span></span>



| <span data-ttu-id="841c4-125">需求</span><span class="sxs-lookup"><span data-stu-id="841c4-125">Requirement</span></span> | <span data-ttu-id="841c4-126">值</span><span class="sxs-lookup"><span data-stu-id="841c4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="841c4-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="841c4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="841c4-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="841c4-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="841c4-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="841c4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="841c4-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="841c4-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="841c4-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="841c4-131">End of client support</span></span><br/>    | <span data-ttu-id="841c4-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="841c4-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="841c4-133">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="841c4-133">End of server support</span></span><br/>    | <span data-ttu-id="841c4-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="841c4-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="841c4-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="841c4-135">Namespace</span></span><br/>                | <span data-ttu-id="841c4-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="841c4-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="841c4-137">MOF</span><span class="sxs-lookup"><span data-stu-id="841c4-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="841c4-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="841c4-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="841c4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="841c4-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="841c4-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="841c4-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="841c4-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="841c4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841c4-142">**Msvm \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="841c4-142">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="841c4-143">**Msvm \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="841c4-143">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

