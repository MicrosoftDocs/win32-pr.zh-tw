---
description: 子類別的抽象類別，代表 CIM \_ ManagedSystemElement 物件的集合。 這些集合允許將 managed 系統專案分組以進行識別，以及簡化設定和設定的關聯。
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: 'CIM_CollectionOfMSEs 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e467e775c78364718f25cc732d6689d9fb2b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848793"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a><span data-ttu-id="01e38-104">CIM_CollectionOfMSEs 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="01e38-104">CIM_CollectionOfMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="01e38-105">子類別的抽象類別，代表 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="01e38-105">An abstract class for subclasses that represent a collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span> <span data-ttu-id="01e38-106">這些集合允許將 managed 系統專案分組以進行識別，以及簡化設定和設定的關聯。</span><span class="sxs-lookup"><span data-stu-id="01e38-106">These collections allow managed system elements to be grouped for identification purposes and to simplify the association of settings and configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="01e38-107">語法</span><span class="sxs-lookup"><span data-stu-id="01e38-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a><span data-ttu-id="01e38-108">成員</span><span class="sxs-lookup"><span data-stu-id="01e38-108">Members</span></span>

<span data-ttu-id="01e38-109">**CIM \_ CollectionOfMSEs** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="01e38-109">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="01e38-110">屬性</span><span class="sxs-lookup"><span data-stu-id="01e38-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01e38-111">屬性</span><span class="sxs-lookup"><span data-stu-id="01e38-111">Properties</span></span>

<span data-ttu-id="01e38-112">**CIM \_ CollectionOfMSEs** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="01e38-112">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01e38-113">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="01e38-113">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e38-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01e38-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e38-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01e38-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e38-116">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="01e38-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01e38-117">集合物件的識別。</span><span class="sxs-lookup"><span data-stu-id="01e38-117">The identification of the collection object.</span></span> <span data-ttu-id="01e38-118">子類別化時， **CollectionID** 屬性可以覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="01e38-118">When subclassed, the **CollectionID** property can be overridden as a key property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01e38-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="01e38-119">Requirements</span></span>



| <span data-ttu-id="01e38-120">需求</span><span class="sxs-lookup"><span data-stu-id="01e38-120">Requirement</span></span> | <span data-ttu-id="01e38-121">值</span><span class="sxs-lookup"><span data-stu-id="01e38-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01e38-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01e38-122">Minimum supported client</span></span><br/> | <span data-ttu-id="01e38-123">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01e38-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="01e38-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01e38-124">Minimum supported server</span></span><br/> | <span data-ttu-id="01e38-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="01e38-125">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="01e38-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="01e38-126">Namespace</span></span><br/>                | <span data-ttu-id="01e38-127">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="01e38-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="01e38-128">MOF</span><span class="sxs-lookup"><span data-stu-id="01e38-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01e38-129"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="01e38-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="01e38-130">DLL</span><span class="sxs-lookup"><span data-stu-id="01e38-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01e38-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="01e38-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="01e38-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01e38-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01e38-133">**CIM \_ 集合**</span><span class="sxs-lookup"><span data-stu-id="01e38-133">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

