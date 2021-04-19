---
description: 代表 managed 系統專案集合與集合成員之間的泛型關聯。
ms.assetid: c9e2bbca-67be-41f2-a94c-cf4eaf5f4694
title: 'CIM_CollectedMSEs 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdf5c5d682f1b6e1b47b64100b3e00f5f79cebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978273"
---
# <a name="cim_collectedmses-class-hyper-v-management"></a><span data-ttu-id="bde9f-103">CIM_CollectedMSEs 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="bde9f-103">CIM_CollectedMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="bde9f-104">代表 managed 系統專案集合與集合成員之間的泛型關聯。</span><span class="sxs-lookup"><span data-stu-id="bde9f-104">Represents a generic association between a collection of managed system elements and the members of the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bde9f-105">語法</span><span class="sxs-lookup"><span data-stu-id="bde9f-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectedMSEs : CIM_MemberOfCollection
{
  CIM_CollectionOfMSEs     REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="bde9f-106">成員</span><span class="sxs-lookup"><span data-stu-id="bde9f-106">Members</span></span>

<span data-ttu-id="bde9f-107">**CIM \_ CollectedMSEs** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bde9f-107">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="bde9f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="bde9f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bde9f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="bde9f-109">Properties</span></span>

<span data-ttu-id="bde9f-110">**CIM \_ CollectedMSEs** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bde9f-110">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bde9f-111">**集合**</span><span class="sxs-lookup"><span data-stu-id="bde9f-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bde9f-112">資料類型： **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="bde9f-112">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="bde9f-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bde9f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bde9f-114">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Collection" ) </span><span class="sxs-lookup"><span data-stu-id="bde9f-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="bde9f-115">集合。</span><span class="sxs-lookup"><span data-stu-id="bde9f-115">The collection.</span></span>

</dd> <dt>

<span data-ttu-id="bde9f-116">**成員**</span><span class="sxs-lookup"><span data-stu-id="bde9f-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bde9f-117">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="bde9f-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="bde9f-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bde9f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bde9f-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Member" ) </span><span class="sxs-lookup"><span data-stu-id="bde9f-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="bde9f-120">集合的成員。</span><span class="sxs-lookup"><span data-stu-id="bde9f-120">The members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bde9f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="bde9f-121">Requirements</span></span>



| <span data-ttu-id="bde9f-122">需求</span><span class="sxs-lookup"><span data-stu-id="bde9f-122">Requirement</span></span> | <span data-ttu-id="bde9f-123">值</span><span class="sxs-lookup"><span data-stu-id="bde9f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bde9f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bde9f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bde9f-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bde9f-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bde9f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bde9f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bde9f-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bde9f-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bde9f-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="bde9f-128">Namespace</span></span><br/>                | <span data-ttu-id="bde9f-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="bde9f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bde9f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="bde9f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bde9f-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="bde9f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bde9f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bde9f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bde9f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bde9f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bde9f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bde9f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde9f-135">**CIM \_ MemberOfCollection**</span><span class="sxs-lookup"><span data-stu-id="bde9f-135">**CIM\_MemberOfCollection**</span></span>](cim-memberofcollection.md)
</dt> </dl>

 

