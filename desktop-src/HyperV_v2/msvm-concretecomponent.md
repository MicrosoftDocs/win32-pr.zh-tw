---
description: 泛型關聯，用來建立 managed 元素之間的部分關聯性。
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Msvm_ConcreteComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2ef9e286f4c7ca296ee6b3638ffb9511ccea4115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980371"
---
# <a name="msvm_concretecomponent-class"></a><span data-ttu-id="1853c-103">Msvm \_ ConcreteComponent 類別</span><span class="sxs-lookup"><span data-stu-id="1853c-103">Msvm\_ConcreteComponent class</span></span>

<span data-ttu-id="1853c-104">用來在 managed 元素之間建立「部分」關聯性的泛型關聯。</span><span class="sxs-lookup"><span data-stu-id="1853c-104">A generic association used to establish 'part of' relationships between managed elements.</span></span> <span data-ttu-id="1853c-105">[**CIM \_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) 會定義為抽象 [**CIM \_ 元件**](/windows/desktop/CIMWin32Prov/cim-component) 類別的具體子類別，用來取代元件的許多特定子類別，而這個子類別不會加入任何語義 (不會明確說明組合、更新基數或加入或移除限定詞的子類別。 ) </span><span class="sxs-lookup"><span data-stu-id="1853c-105">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) is defined as a concrete subclass of the abstract [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component) class, to be used in place of many specific subclasses of component that add no semantics (that is subclasses that do not clarify the type of composition, update cardinalities, or add or remove qualifiers.)</span></span>

<span data-ttu-id="1853c-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1853c-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1853c-107">語法</span><span class="sxs-lookup"><span data-stu-id="1853c-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="1853c-108">成員</span><span class="sxs-lookup"><span data-stu-id="1853c-108">Members</span></span>

<span data-ttu-id="1853c-109">**Msvm \_ ConcreteComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1853c-109">The **Msvm\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="1853c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1853c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1853c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1853c-111">Properties</span></span>

<span data-ttu-id="1853c-112">**Msvm \_ ConcreteComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1853c-112">The **Msvm\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1853c-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="1853c-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1853c-114">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="1853c-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="1853c-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1853c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1853c-116">關聯中的父元素。</span><span class="sxs-lookup"><span data-stu-id="1853c-116">The parent element in the association.</span></span> <span data-ttu-id="1853c-117">這個屬性繼承自 [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1853c-117">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1853c-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1853c-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1853c-119">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="1853c-119">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="1853c-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1853c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1853c-121">關聯中的子項目。</span><span class="sxs-lookup"><span data-stu-id="1853c-121">The child element in the association.</span></span> <span data-ttu-id="1853c-122">這個屬性繼承自 [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1853c-122">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1853c-123">備註</span><span class="sxs-lookup"><span data-stu-id="1853c-123">Remarks</span></span>

<span data-ttu-id="1853c-124">存取 **Msvm \_ ConcreteComponent** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="1853c-124">Access to the **Msvm\_ConcreteComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1853c-125">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="1853c-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1853c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1853c-126">Requirements</span></span>



| <span data-ttu-id="1853c-127">需求</span><span class="sxs-lookup"><span data-stu-id="1853c-127">Requirement</span></span> | <span data-ttu-id="1853c-128">值</span><span class="sxs-lookup"><span data-stu-id="1853c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1853c-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1853c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1853c-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1853c-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1853c-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1853c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1853c-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1853c-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1853c-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="1853c-133">Namespace</span></span><br/>                | <span data-ttu-id="1853c-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="1853c-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1853c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="1853c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1853c-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1853c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1853c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1853c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1853c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1853c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1853c-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1853c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1853c-140">**CIM \_ ConcreteComponent**</span><span class="sxs-lookup"><span data-stu-id="1853c-140">**CIM\_ConcreteComponent**</span></span>](cim-concretecomponent.md)
</dt> <dt>

<span data-ttu-id="1853c-141">[**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1853c-141">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1853c-142">虛擬系統類別</span><span class="sxs-lookup"><span data-stu-id="1853c-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

