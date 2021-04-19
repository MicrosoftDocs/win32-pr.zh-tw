---
description: 表示父 managed 專案和子受管理專案之間的泛型關聯，該子系代表子系的元件或部分的父元素。
ms.assetid: b5cef452-2d00-483c-8e70-f804f1e3536b
title: 'CIM_Component 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56ff83a4da51ba18205a8d8ab5e6e57ea1a7794b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998298"
---
# <a name="cim_component-class-hyper-v-management"></a><span data-ttu-id="d5df4-103">CIM_Component 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="d5df4-103">CIM_Component class (Hyper-V management)</span></span>

<span data-ttu-id="d5df4-104">表示父 managed 專案和子受管理專案之間的泛型關聯，該子系代表子系的元件或部分的父元素。</span><span class="sxs-lookup"><span data-stu-id="d5df4-104">Represents a generic association between a parent managed element and a child managed element where the child represents a component or part of the parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5df4-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5df4-105">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, Version("2.7.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="d5df4-106">成員</span><span class="sxs-lookup"><span data-stu-id="d5df4-106">Members</span></span>

<span data-ttu-id="d5df4-107">**CIM \_ 元件** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d5df4-107">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="d5df4-108">屬性</span><span class="sxs-lookup"><span data-stu-id="d5df4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5df4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d5df4-109">Properties</span></span>

<span data-ttu-id="d5df4-110">**CIM \_ 元件** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d5df4-110">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5df4-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d5df4-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5df4-112">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="d5df4-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d5df4-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5df4-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5df4-114">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、 [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d5df4-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d5df4-115">關聯中的父元素。</span><span class="sxs-lookup"><span data-stu-id="d5df4-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="d5df4-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d5df4-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5df4-117">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="d5df4-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d5df4-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5df4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5df4-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d5df4-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d5df4-120">關聯中的子項目。</span><span class="sxs-lookup"><span data-stu-id="d5df4-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5df4-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5df4-121">Requirements</span></span>



| <span data-ttu-id="d5df4-122">需求</span><span class="sxs-lookup"><span data-stu-id="d5df4-122">Requirement</span></span> | <span data-ttu-id="d5df4-123">值</span><span class="sxs-lookup"><span data-stu-id="d5df4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5df4-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5df4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d5df4-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d5df4-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d5df4-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5df4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d5df4-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5df4-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d5df4-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="d5df4-128">Namespace</span></span><br/>                | <span data-ttu-id="d5df4-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d5df4-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d5df4-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d5df4-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5df4-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d5df4-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5df4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d5df4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5df4-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d5df4-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

