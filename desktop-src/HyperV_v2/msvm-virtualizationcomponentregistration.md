---
description: 表示 Microsoft Hyper-V 平臺中的服務註冊。
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Msvm_VirtualizationComponentRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e9704dcade0474a10ca60383280941ec2e3591b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998058"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a><span data-ttu-id="1caca-103">Msvm \_ VirtualizationComponentRegistration 類別</span><span class="sxs-lookup"><span data-stu-id="1caca-103">Msvm\_VirtualizationComponentRegistration class</span></span>

<span data-ttu-id="1caca-104">表示 Microsoft Hyper-V 平臺中的服務註冊。</span><span class="sxs-lookup"><span data-stu-id="1caca-104">Represents the registration of a service in the Microsoft Hyper-V platform.</span></span>

<span data-ttu-id="1caca-105">下列語法已簡化受控物件格式 (MOF) 程式碼。</span><span class="sxs-lookup"><span data-stu-id="1caca-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1caca-106">語法</span><span class="sxs-lookup"><span data-stu-id="1caca-106">Syntax</span></span>

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a><span data-ttu-id="1caca-107">成員</span><span class="sxs-lookup"><span data-stu-id="1caca-107">Members</span></span>

<span data-ttu-id="1caca-108">**Msvm \_ VirtualizationComponentRegistration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1caca-108">The **Msvm\_VirtualizationComponentRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="1caca-109">屬性</span><span class="sxs-lookup"><span data-stu-id="1caca-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1caca-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1caca-110">Properties</span></span>

<span data-ttu-id="1caca-111">**Msvm \_ VirtualizationComponentRegistration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1caca-111">The **Msvm\_VirtualizationComponentRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1caca-112">**元件**</span><span class="sxs-lookup"><span data-stu-id="1caca-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1caca-113">資料類型： **[ **Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="1caca-113">Data type: **[**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1caca-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1caca-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1caca-115">實例的參考，該實例描述實此類別的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="1caca-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="1caca-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="1caca-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1caca-117">資料類型： **[ **Msvm \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="1caca-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1caca-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1caca-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1caca-119">描述服務所支援之資源類型之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="1caca-119">A reference to an instance that describes a resource type supported by the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1caca-120">備註</span><span class="sxs-lookup"><span data-stu-id="1caca-120">Remarks</span></span>

<span data-ttu-id="1caca-121">存取 **Msvm \_ VirtualizationComponentRegistration** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="1caca-121">Access to the **Msvm\_VirtualizationComponentRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1caca-122">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="1caca-122">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1caca-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="1caca-123">Requirements</span></span>



| <span data-ttu-id="1caca-124">需求</span><span class="sxs-lookup"><span data-stu-id="1caca-124">Requirement</span></span> | <span data-ttu-id="1caca-125">值</span><span class="sxs-lookup"><span data-stu-id="1caca-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1caca-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1caca-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1caca-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1caca-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1caca-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1caca-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1caca-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1caca-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1caca-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1caca-130">End of client support</span></span><br/>    | <span data-ttu-id="1caca-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1caca-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1caca-132">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1caca-132">End of server support</span></span><br/>    | <span data-ttu-id="1caca-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1caca-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1caca-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="1caca-134">Namespace</span></span><br/>                | <span data-ttu-id="1caca-135">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="1caca-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1caca-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1caca-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1caca-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1caca-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1caca-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1caca-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1caca-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1caca-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

