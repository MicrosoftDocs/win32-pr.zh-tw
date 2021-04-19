---
description: 代表 managed 元素相依于另一個的泛型關聯。 CIM \_ ConcreteDependency 子類別 cim 相依性 \_ ，以提供實體類別版本的 cim 相依性 \_ 。
ms.assetid: c0e1527d-d350-410d-9b5f-c9d4dedf7393
title: CIM_ConcreteDependency 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteDependency
- CIM_ConcreteDependency.Antecedent
- CIM_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 253f57b1fd29c3844f0e87d488974ced7bec98bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997852"
---
# <a name="cim_concretedependency-class"></a><span data-ttu-id="d340e-104">CIM \_ ConcreteDependency 類別</span><span class="sxs-lookup"><span data-stu-id="d340e-104">CIM\_ConcreteDependency class</span></span>

<span data-ttu-id="d340e-105">代表 managed 元素相依于另一個的泛型關聯。</span><span class="sxs-lookup"><span data-stu-id="d340e-105">Represents a generic association in which a managed element depends on another.</span></span> <span data-ttu-id="d340e-106">**CIM \_ConcreteDependency** 子類別 cim 相依性，以提供實體類別版本的 [**\_**](cim-dependency.md) cim 相依性。 **\_**</span><span class="sxs-lookup"><span data-stu-id="d340e-106">**CIM\_ConcreteDependency** subclasses [**CIM\_Dependency**](cim-dependency.md) to provide a concrete class version of **CIM\_Dependency**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d340e-107">語法</span><span class="sxs-lookup"><span data-stu-id="d340e-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d340e-108">成員</span><span class="sxs-lookup"><span data-stu-id="d340e-108">Members</span></span>

<span data-ttu-id="d340e-109">**CIM \_ ConcreteDependency** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d340e-109">The **CIM\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="d340e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d340e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d340e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d340e-111">Properties</span></span>

<span data-ttu-id="d340e-112">**CIM \_ ConcreteDependency** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d340e-112">The **CIM\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d340e-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="d340e-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d340e-114">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="d340e-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d340e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d340e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d340e-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="d340e-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d340e-117">關聯中的獨立物件。</span><span class="sxs-lookup"><span data-stu-id="d340e-117">The independent object in the association.</span></span>

</dd> <dt>

<span data-ttu-id="d340e-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="d340e-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d340e-119">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="d340e-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d340e-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d340e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d340e-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="d340e-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d340e-122">關聯中的相依物件。</span><span class="sxs-lookup"><span data-stu-id="d340e-122">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d340e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d340e-123">Requirements</span></span>



| <span data-ttu-id="d340e-124">需求</span><span class="sxs-lookup"><span data-stu-id="d340e-124">Requirement</span></span> | <span data-ttu-id="d340e-125">值</span><span class="sxs-lookup"><span data-stu-id="d340e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d340e-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d340e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d340e-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d340e-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d340e-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d340e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d340e-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d340e-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d340e-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="d340e-130">Namespace</span></span><br/>                | <span data-ttu-id="d340e-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d340e-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d340e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d340e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d340e-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d340e-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d340e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d340e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d340e-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d340e-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d340e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d340e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d340e-137">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="d340e-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

