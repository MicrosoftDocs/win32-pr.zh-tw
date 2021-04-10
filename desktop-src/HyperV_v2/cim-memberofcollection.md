---
description: 表示 managed 專案為其成員的關聯性，而且是由集合所匯總。
ms.assetid: 324284fa-ece6-41df-9891-040a7561dce4
title: CIM_MemberOfCollection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemberOfCollection
- CIM_MemberOfCollection.Collection
- CIM_MemberOfCollection.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9bcebfb08cbbc0cb18e00f1b0e5e2646ca086faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027039"
---
# <a name="cim_memberofcollection-class"></a><span data-ttu-id="d115b-103">CIM \_ MemberOfCollection 類別</span><span class="sxs-lookup"><span data-stu-id="d115b-103">CIM\_MemberOfCollection class</span></span>

<span data-ttu-id="d115b-104">表示 managed 專案為其成員的關聯性，而且是由集合所匯總。</span><span class="sxs-lookup"><span data-stu-id="d115b-104">Represents a relationship in which a managed element is a member of and is aggregated by a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d115b-105">語法</span><span class="sxs-lookup"><span data-stu-id="d115b-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_MemberOfCollection
{
  CIM_Collection     REF Collection;
  CIM_ManagedElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="d115b-106">成員</span><span class="sxs-lookup"><span data-stu-id="d115b-106">Members</span></span>

<span data-ttu-id="d115b-107">**CIM \_ MemberOfCollection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d115b-107">The **CIM\_MemberOfCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="d115b-108">屬性</span><span class="sxs-lookup"><span data-stu-id="d115b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d115b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d115b-109">Properties</span></span>

<span data-ttu-id="d115b-110">**CIM \_ MemberOfCollection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d115b-110">The **CIM\_MemberOfCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d115b-111">**集合**</span><span class="sxs-lookup"><span data-stu-id="d115b-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d115b-112">資料類型： **CIM \_ 集合**</span><span class="sxs-lookup"><span data-stu-id="d115b-112">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="d115b-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d115b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d115b-114">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、 [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d115b-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d115b-115">匯總成員的集合。</span><span class="sxs-lookup"><span data-stu-id="d115b-115">The collection that aggregates members.</span></span>

</dd> <dt>

<span data-ttu-id="d115b-116">**成員**</span><span class="sxs-lookup"><span data-stu-id="d115b-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d115b-117">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="d115b-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d115b-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d115b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d115b-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d115b-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d115b-120">集合的成員。</span><span class="sxs-lookup"><span data-stu-id="d115b-120">The member of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d115b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d115b-121">Requirements</span></span>



| <span data-ttu-id="d115b-122">需求</span><span class="sxs-lookup"><span data-stu-id="d115b-122">Requirement</span></span> | <span data-ttu-id="d115b-123">值</span><span class="sxs-lookup"><span data-stu-id="d115b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d115b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d115b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d115b-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d115b-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d115b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d115b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d115b-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d115b-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d115b-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="d115b-128">Namespace</span></span><br/>                | <span data-ttu-id="d115b-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d115b-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d115b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d115b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d115b-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d115b-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d115b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d115b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d115b-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d115b-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

