---
description: 表示用來建立 managed 元素之間關聯性元件的泛型關聯。
ms.assetid: 9785ea8b-fb76-4ffe-8649-aa2fe1b01d5f
title: CIM_ConcreteComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteComponent
- CIM_ConcreteComponent.GroupComponent
- CIM_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77ee0f33f540bfd215ec10a24c3c574976189d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849667"
---
# <a name="cim_concretecomponent-class"></a><span data-ttu-id="1026a-103">CIM \_ ConcreteComponent 類別</span><span class="sxs-lookup"><span data-stu-id="1026a-103">CIM\_ConcreteComponent class</span></span>

<span data-ttu-id="1026a-104">表示用來建立 managed 元素之間關聯性元件的泛型關聯。</span><span class="sxs-lookup"><span data-stu-id="1026a-104">Represents a generic association used to establish the parts of a relationship between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="1026a-105">語法</span><span class="sxs-lookup"><span data-stu-id="1026a-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteComponent : CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="1026a-106">成員</span><span class="sxs-lookup"><span data-stu-id="1026a-106">Members</span></span>

<span data-ttu-id="1026a-107">**CIM \_ ConcreteComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1026a-107">The **CIM\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="1026a-108">屬性</span><span class="sxs-lookup"><span data-stu-id="1026a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1026a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="1026a-109">Properties</span></span>

<span data-ttu-id="1026a-110">**CIM \_ ConcreteComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1026a-110">The **CIM\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1026a-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="1026a-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1026a-112">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="1026a-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="1026a-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1026a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1026a-114">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="1026a-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="1026a-115">關聯中的父元素。</span><span class="sxs-lookup"><span data-stu-id="1026a-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="1026a-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1026a-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1026a-117">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="1026a-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="1026a-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1026a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1026a-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="1026a-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="1026a-120">關聯中的子項目。</span><span class="sxs-lookup"><span data-stu-id="1026a-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1026a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1026a-121">Requirements</span></span>



| <span data-ttu-id="1026a-122">需求</span><span class="sxs-lookup"><span data-stu-id="1026a-122">Requirement</span></span> | <span data-ttu-id="1026a-123">值</span><span class="sxs-lookup"><span data-stu-id="1026a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1026a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1026a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1026a-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1026a-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1026a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1026a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1026a-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1026a-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1026a-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="1026a-128">Namespace</span></span><br/>                | <span data-ttu-id="1026a-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="1026a-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1026a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1026a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1026a-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1026a-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1026a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1026a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1026a-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1026a-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1026a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1026a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1026a-135">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="1026a-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

