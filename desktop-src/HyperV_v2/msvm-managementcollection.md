---
description: 表示其他集合的集合。
ms.assetid: 1f7f5517-55d9-44a3-b0ca-444a9d7d5941
title: Msvm_ManagementCollection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ManagementCollection
- Msvm_ManagementCollection.CollectionID
- Msvm_ManagementCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2d3499bb161495152b6de4b8aebd7c64d041d069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979391"
---
# <a name="msvm_managementcollection-class"></a><span data-ttu-id="e3853-103">Msvm \_ ManagementCollection 類別</span><span class="sxs-lookup"><span data-stu-id="e3853-103">Msvm\_ManagementCollection class</span></span>

<span data-ttu-id="e3853-104">表示其他集合的集合。</span><span class="sxs-lookup"><span data-stu-id="e3853-104">Represents a collection of other collections.</span></span>

<span data-ttu-id="e3853-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e3853-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3853-106">語法</span><span class="sxs-lookup"><span data-stu-id="e3853-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ManagementCollection : CIM_CollectionOfMSEs
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="e3853-107">成員</span><span class="sxs-lookup"><span data-stu-id="e3853-107">Members</span></span>

<span data-ttu-id="e3853-108">**Msvm \_ ManagementCollection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e3853-108">The **Msvm\_ManagementCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="e3853-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e3853-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3853-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e3853-110">Properties</span></span>

<span data-ttu-id="e3853-111">**Msvm \_ ManagementCollection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e3853-111">The **Msvm\_ManagementCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3853-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="e3853-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3853-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e3853-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3853-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e3853-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3853-115">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CollectionID" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e3853-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e3853-116">集合物件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3853-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="e3853-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e3853-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3853-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e3853-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3853-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e3853-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3853-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ElementName" ) </span><span class="sxs-lookup"><span data-stu-id="e3853-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="e3853-121">集合的使用者定義名稱。</span><span class="sxs-lookup"><span data-stu-id="e3853-121">An user-defined name for the collection.</span></span> <span data-ttu-id="e3853-122">請注意，這不一定是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e3853-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3853-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3853-123">Requirements</span></span>



| <span data-ttu-id="e3853-124">需求</span><span class="sxs-lookup"><span data-stu-id="e3853-124">Requirement</span></span> | <span data-ttu-id="e3853-125">值</span><span class="sxs-lookup"><span data-stu-id="e3853-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3853-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3853-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e3853-127">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3853-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e3853-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3853-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e3853-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e3853-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e3853-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="e3853-130">Namespace</span></span><br/>                | <span data-ttu-id="e3853-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e3853-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e3853-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e3853-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3853-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e3853-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3853-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e3853-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3853-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e3853-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e3853-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3853-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3853-137">**CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="e3853-137">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

