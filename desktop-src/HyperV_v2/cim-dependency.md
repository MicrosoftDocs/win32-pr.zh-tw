---
description: 表示用來建立 managed 元素之間相依性關聯性的泛型關聯。
ms.assetid: a81beedc-5473-49a6-8e7f-67e831d3e8bc
title: 'CIM_Dependency 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e85f59b190e0024fc34489315fa2fae1c0d6b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966764"
---
# <a name="cim_dependency-class-hyper-v-management"></a><span data-ttu-id="83712-103">CIM_Dependency 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="83712-103">CIM_Dependency class (Hyper-V management)</span></span>

<span data-ttu-id="83712-104">表示用來建立 managed 元素之間相依性關聯性的泛型關聯。</span><span class="sxs-lookup"><span data-stu-id="83712-104">Represents a generic association used to establish dependency relationships between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="83712-105">語法</span><span class="sxs-lookup"><span data-stu-id="83712-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="83712-106">成員</span><span class="sxs-lookup"><span data-stu-id="83712-106">Members</span></span>

<span data-ttu-id="83712-107">**CIM 相依 \_** 性類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="83712-107">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="83712-108">屬性</span><span class="sxs-lookup"><span data-stu-id="83712-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83712-109">屬性</span><span class="sxs-lookup"><span data-stu-id="83712-109">Properties</span></span>

<span data-ttu-id="83712-110">**CIM 相依 \_** 性類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="83712-110">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83712-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="83712-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83712-112">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="83712-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="83712-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83712-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83712-114">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="83712-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="83712-115">此關聯中的獨立物件。</span><span class="sxs-lookup"><span data-stu-id="83712-115">The independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="83712-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="83712-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83712-117">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="83712-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="83712-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83712-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83712-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="83712-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="83712-120">關聯中的相依物件。</span><span class="sxs-lookup"><span data-stu-id="83712-120">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83712-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="83712-121">Requirements</span></span>



| <span data-ttu-id="83712-122">需求</span><span class="sxs-lookup"><span data-stu-id="83712-122">Requirement</span></span> | <span data-ttu-id="83712-123">值</span><span class="sxs-lookup"><span data-stu-id="83712-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83712-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83712-124">Minimum supported client</span></span><br/> | <span data-ttu-id="83712-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="83712-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="83712-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83712-126">Minimum supported server</span></span><br/> | <span data-ttu-id="83712-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="83712-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="83712-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="83712-128">Namespace</span></span><br/>                | <span data-ttu-id="83712-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="83712-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="83712-130">MOF</span><span class="sxs-lookup"><span data-stu-id="83712-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83712-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="83712-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="83712-132">DLL</span><span class="sxs-lookup"><span data-stu-id="83712-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83712-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83712-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

