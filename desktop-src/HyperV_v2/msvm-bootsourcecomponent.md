---
description: 將 Msvm \_ BootSourceSettingData 與整體 Msvm VirtualSystemSettingData 建立關聯 \_ 。
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Msvm_BootSourceComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dfe86fa7882b1b20e5b5abbbdaa9d4f37f231f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972471"
---
# <a name="msvm_bootsourcecomponent-class"></a><span data-ttu-id="2c005-103">Msvm \_ BootSourceComponent 類別</span><span class="sxs-lookup"><span data-stu-id="2c005-103">Msvm\_BootSourceComponent class</span></span>

<span data-ttu-id="2c005-104">將 [**Msvm \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md) 與整體 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)建立關聯。</span><span class="sxs-lookup"><span data-stu-id="2c005-104">Associates the [**Msvm\_BootSourceSettingData**](msvm-bootsourcesettingdata.md) to the overall [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).</span></span> <span data-ttu-id="2c005-105">此類別衍生自 [**CIM \_ 元件**](/windows/desktop/CIMWin32Prov/cim-component)。</span><span class="sxs-lookup"><span data-stu-id="2c005-105">This class derives from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

<span data-ttu-id="2c005-106">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2c005-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c005-107">語法</span><span class="sxs-lookup"><span data-stu-id="2c005-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="2c005-108">成員</span><span class="sxs-lookup"><span data-stu-id="2c005-108">Members</span></span>

<span data-ttu-id="2c005-109">**Msvm \_ BootSourceComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2c005-109">The **Msvm\_BootSourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="2c005-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2c005-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c005-111">屬性</span><span class="sxs-lookup"><span data-stu-id="2c005-111">Properties</span></span>

<span data-ttu-id="2c005-112">**Msvm \_ BootSourceComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2c005-112">The **Msvm\_BootSourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c005-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2c005-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c005-114">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="2c005-114">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="2c005-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c005-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c005-116">關聯中父元素的參考。</span><span class="sxs-lookup"><span data-stu-id="2c005-116">Reference to the parent element in the association.</span></span> <span data-ttu-id="2c005-117">這個屬性繼承自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="2c005-117">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c005-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2c005-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c005-119">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="2c005-119">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="2c005-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c005-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c005-121">關聯中子項目的參考。</span><span class="sxs-lookup"><span data-stu-id="2c005-121">Reference to the child element in the association.</span></span> <span data-ttu-id="2c005-122">這個屬性繼承自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="2c005-122">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c005-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c005-123">Requirements</span></span>



| <span data-ttu-id="2c005-124">需求</span><span class="sxs-lookup"><span data-stu-id="2c005-124">Requirement</span></span> | <span data-ttu-id="2c005-125">值</span><span class="sxs-lookup"><span data-stu-id="2c005-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c005-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c005-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2c005-127">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c005-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2c005-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c005-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2c005-129">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c005-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2c005-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="2c005-130">Namespace</span></span><br/>                | <span data-ttu-id="2c005-131">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="2c005-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2c005-132">MOF</span><span class="sxs-lookup"><span data-stu-id="2c005-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c005-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2c005-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c005-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2c005-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c005-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c005-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2c005-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c005-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c005-137">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="2c005-137">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="2c005-138">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="2c005-138">**CIM\_Component**</span></span>](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[<span data-ttu-id="2c005-139">**Msvm \_ BootSourceSettingData**</span><span class="sxs-lookup"><span data-stu-id="2c005-139">**Msvm\_BootSourceSettingData**</span></span>](msvm-bootsourcesettingdata.md)
</dt> <dt>

[<span data-ttu-id="2c005-140">**Msvm \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="2c005-140">**Msvm\_VirtualSystemSettingData**</span></span>](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 

