---
description: 建立 &\# 0034;&\# 0034 的一部分; 系統與其組成之任何 managed 系統專案之間的關聯性。
ms.assetid: 6BF72E36-9B6C-4853-A553-DDAF65991C86
title: Msvm_SystemComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemComponent
- Msvm_SystemComponent.GroupComponent
- Msvm_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee150793143b549c90d280eef287ee6a5afb66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386108"
---
# <a name="msvm_systemcomponent-class"></a><span data-ttu-id="50e6e-103">Msvm \_ SystemComponent 類別</span><span class="sxs-lookup"><span data-stu-id="50e6e-103">Msvm\_SystemComponent class</span></span>

<span data-ttu-id="50e6e-104">建立系統與其組成之任何 managed 系統專案之間的「部分」關聯性。</span><span class="sxs-lookup"><span data-stu-id="50e6e-104">Establishes a "part of" relationship between a system and any managed system element of which it is composed.</span></span>

<span data-ttu-id="50e6e-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="50e6e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e6e-106">語法</span><span class="sxs-lookup"><span data-stu-id="50e6e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), Association, Aggregation]
class Msvm_SystemComponent : CIM_SystemComponent
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="50e6e-107">成員</span><span class="sxs-lookup"><span data-stu-id="50e6e-107">Members</span></span>

<span data-ttu-id="50e6e-108">**Msvm \_ SystemComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="50e6e-108">The **Msvm\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="50e6e-109">屬性</span><span class="sxs-lookup"><span data-stu-id="50e6e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50e6e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="50e6e-110">Properties</span></span>

<span data-ttu-id="50e6e-111">**Msvm \_ SystemComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="50e6e-111">The **Msvm\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50e6e-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="50e6e-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e6e-113">資料類型： **[ **CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="50e6e-113">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="50e6e-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50e6e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50e6e-115">關聯中的父元素。</span><span class="sxs-lookup"><span data-stu-id="50e6e-115">The parent element in the association.</span></span> <span data-ttu-id="50e6e-116">這個屬性繼承自 [**CIM \_ SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent)。</span><span class="sxs-lookup"><span data-stu-id="50e6e-116">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> <dt>

<span data-ttu-id="50e6e-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="50e6e-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e6e-118">資料類型： **[ **CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span><span class="sxs-lookup"><span data-stu-id="50e6e-118">Data type: **[**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span></span>
</dt> <dt>

<span data-ttu-id="50e6e-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50e6e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50e6e-120">關聯中的子項目。</span><span class="sxs-lookup"><span data-stu-id="50e6e-120">The child element in the association.</span></span> <span data-ttu-id="50e6e-121">這個屬性繼承自 [**CIM \_ SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent)。</span><span class="sxs-lookup"><span data-stu-id="50e6e-121">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50e6e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="50e6e-122">Requirements</span></span>



| <span data-ttu-id="50e6e-123">需求</span><span class="sxs-lookup"><span data-stu-id="50e6e-123">Requirement</span></span> | <span data-ttu-id="50e6e-124">值</span><span class="sxs-lookup"><span data-stu-id="50e6e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50e6e-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50e6e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="50e6e-126">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50e6e-126">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="50e6e-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50e6e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="50e6e-128">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50e6e-128">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="50e6e-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="50e6e-129">Namespace</span></span><br/>                | <span data-ttu-id="50e6e-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="50e6e-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="50e6e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="50e6e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50e6e-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="50e6e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="50e6e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="50e6e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50e6e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="50e6e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

