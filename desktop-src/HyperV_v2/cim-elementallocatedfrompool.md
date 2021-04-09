---
description: 表示一種關聯，其中 CIM \_ LogicalElement 物件代表從 CIM ResourcePool 物件配置的資源 \_ 。
ms.assetid: 5e3c95c5-1cbb-40de-b285-0bf9b34a5ca8
title: CIM_ElementAllocatedFromPool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementAllocatedFromPool
- CIM_ElementAllocatedFromPool.Antecedent
- CIM_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5fc6d58f5ebf82013f38b39027e0cd02e0e3595a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848290"
---
# <a name="cim_elementallocatedfrompool-class"></a><span data-ttu-id="e5033-103">CIM \_ ElementAllocatedFromPool 類別</span><span class="sxs-lookup"><span data-stu-id="e5033-103">CIM\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="e5033-104">表示一種關聯，其中 [**cim \_ LogicalElement**](cim-logicalelement.md) 物件代表從 [**CIM \_ ResourcePool**](cim-resourcepool.md) 物件配置的資源。</span><span class="sxs-lookup"><span data-stu-id="e5033-104">Represents an association in which a [**CIM\_LogicalElement**](cim-logicalelement.md) object represents a resource allocated from a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5033-105">語法</span><span class="sxs-lookup"><span data-stu-id="e5033-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ElementAllocatedFromPool : CIM_Dependency
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e5033-106">成員</span><span class="sxs-lookup"><span data-stu-id="e5033-106">Members</span></span>

<span data-ttu-id="e5033-107">**CIM \_ ElementAllocatedFromPool** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e5033-107">The **CIM\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="e5033-108">屬性</span><span class="sxs-lookup"><span data-stu-id="e5033-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5033-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e5033-109">Properties</span></span>

<span data-ttu-id="e5033-110">**CIM \_ ElementAllocatedFromPool** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e5033-110">The **CIM\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5033-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="e5033-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5033-112">資料類型： **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="e5033-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="e5033-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5033-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5033-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Antecedent」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="e5033-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e5033-115">資源集區。</span><span class="sxs-lookup"><span data-stu-id="e5033-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="e5033-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="e5033-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5033-117">資料類型： **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="e5033-117">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="e5033-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5033-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5033-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="e5033-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e5033-120">配置的資源。</span><span class="sxs-lookup"><span data-stu-id="e5033-120">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5033-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5033-121">Requirements</span></span>



| <span data-ttu-id="e5033-122">需求</span><span class="sxs-lookup"><span data-stu-id="e5033-122">Requirement</span></span> | <span data-ttu-id="e5033-123">值</span><span class="sxs-lookup"><span data-stu-id="e5033-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5033-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5033-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e5033-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e5033-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e5033-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5033-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e5033-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5033-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e5033-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="e5033-128">Namespace</span></span><br/>                | <span data-ttu-id="e5033-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e5033-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e5033-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e5033-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5033-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e5033-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5033-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e5033-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5033-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e5033-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e5033-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5033-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5033-135">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="e5033-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

