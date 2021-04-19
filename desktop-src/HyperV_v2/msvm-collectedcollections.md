---
description: 將 Msvm \_ VirtualSystemCollection 與包含的 Msvm 不會產生的物件產生關聯 \_ 。
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Msvm_CollectedCollections 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedCollections
- Msvm_CollectedCollections.Collection
- Msvm_CollectedCollections.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16ec6ad77c44e0a4e9001a0cb77d227573635ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989085"
---
# <a name="msvm_collectedcollections-class"></a><span data-ttu-id="4050e-103">Msvm \_ CollectedCollections 類別</span><span class="sxs-lookup"><span data-stu-id="4050e-103">Msvm\_CollectedCollections class</span></span>

<span data-ttu-id="4050e-104">將 [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md)與包含的 Msvm 不會產生的物件產生關聯。 [**\_**](msvm-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="4050e-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="4050e-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4050e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4050e-106">語法</span><span class="sxs-lookup"><span data-stu-id="4050e-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a><span data-ttu-id="4050e-107">成員</span><span class="sxs-lookup"><span data-stu-id="4050e-107">Members</span></span>

<span data-ttu-id="4050e-108">**Msvm \_ CollectedCollections** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4050e-108">The **Msvm\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="4050e-109">屬性</span><span class="sxs-lookup"><span data-stu-id="4050e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4050e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4050e-110">Properties</span></span>

<span data-ttu-id="4050e-111">**Msvm \_ CollectedCollections** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4050e-111">The **Msvm\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4050e-112">**集合**</span><span class="sxs-lookup"><span data-stu-id="4050e-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4050e-113">資料類型： **Msvm \_ ManagementCollection**</span><span class="sxs-lookup"><span data-stu-id="4050e-113">Data type: **Msvm\_ManagementCollection**</span></span>
</dt> <dt>

<span data-ttu-id="4050e-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4050e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4050e-115">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Collection" ) </span><span class="sxs-lookup"><span data-stu-id="4050e-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="4050e-116">代表集合的 [**Msvm \_ ManagementCollection**](msvm-managementcollection.md) 群組或 ' 包 ' 物件。</span><span class="sxs-lookup"><span data-stu-id="4050e-116">An [**Msvm\_ManagementCollection**](msvm-managementcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="4050e-117">**成員**</span><span class="sxs-lookup"><span data-stu-id="4050e-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4050e-118">資料類型： **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="4050e-118">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="4050e-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4050e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4050e-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Member" ) </span><span class="sxs-lookup"><span data-stu-id="4050e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="4050e-121">包含集合成員的 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 。</span><span class="sxs-lookup"><span data-stu-id="4050e-121">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4050e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4050e-122">Requirements</span></span>



| <span data-ttu-id="4050e-123">需求</span><span class="sxs-lookup"><span data-stu-id="4050e-123">Requirement</span></span> | <span data-ttu-id="4050e-124">值</span><span class="sxs-lookup"><span data-stu-id="4050e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4050e-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4050e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4050e-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4050e-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4050e-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4050e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4050e-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4050e-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4050e-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="4050e-129">Namespace</span></span><br/>                | <span data-ttu-id="4050e-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="4050e-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4050e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4050e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4050e-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4050e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4050e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4050e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4050e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4050e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4050e-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4050e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4050e-136">**CIM \_ CollectedMSEs**</span><span class="sxs-lookup"><span data-stu-id="4050e-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

