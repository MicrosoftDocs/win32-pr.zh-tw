---
description: 表示虛擬系統快照集的集合。
ms.assetid: c9b64421-232c-4f32-a088-6b98602ca3f4
title: Msvm_SnapshotCollection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotCollection
- Msvm_SnapshotCollection.CollectionID
- Msvm_SnapshotCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e24566f1f5c5500258f14f88cbe2b7c4fa29e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114577"
---
# <a name="msvm_snapshotcollection-class"></a><span data-ttu-id="16a52-103">Msvm \_ SnapshotCollection 類別</span><span class="sxs-lookup"><span data-stu-id="16a52-103">Msvm\_SnapshotCollection class</span></span>

<span data-ttu-id="16a52-104">表示虛擬系統快照集的集合。</span><span class="sxs-lookup"><span data-stu-id="16a52-104">Represents a collection of virtual system snapshots.</span></span>

<span data-ttu-id="16a52-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="16a52-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a52-106">語法</span><span class="sxs-lookup"><span data-stu-id="16a52-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotCollection : CIM_Collection
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="16a52-107">成員</span><span class="sxs-lookup"><span data-stu-id="16a52-107">Members</span></span>

<span data-ttu-id="16a52-108">**Msvm \_ SnapshotCollection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="16a52-108">The **Msvm\_SnapshotCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="16a52-109">屬性</span><span class="sxs-lookup"><span data-stu-id="16a52-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16a52-110">屬性</span><span class="sxs-lookup"><span data-stu-id="16a52-110">Properties</span></span>

<span data-ttu-id="16a52-111">**Msvm \_ SnapshotCollection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="16a52-111">The **Msvm\_SnapshotCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16a52-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="16a52-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16a52-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16a52-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16a52-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16a52-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16a52-115">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CollectionID" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="16a52-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="16a52-116">集合物件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="16a52-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="16a52-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="16a52-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16a52-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16a52-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16a52-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16a52-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16a52-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ElementName" ) </span><span class="sxs-lookup"><span data-stu-id="16a52-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="16a52-121">集合的使用者定義名稱。</span><span class="sxs-lookup"><span data-stu-id="16a52-121">An user-defined name for the collection.</span></span> <span data-ttu-id="16a52-122">請注意，這不一定是唯一的。</span><span class="sxs-lookup"><span data-stu-id="16a52-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16a52-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="16a52-123">Requirements</span></span>



| <span data-ttu-id="16a52-124">需求</span><span class="sxs-lookup"><span data-stu-id="16a52-124">Requirement</span></span> | <span data-ttu-id="16a52-125">值</span><span class="sxs-lookup"><span data-stu-id="16a52-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16a52-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16a52-126">Minimum supported client</span></span><br/> | <span data-ttu-id="16a52-127">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16a52-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="16a52-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16a52-128">Minimum supported server</span></span><br/> | <span data-ttu-id="16a52-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="16a52-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="16a52-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="16a52-130">Namespace</span></span><br/>                | <span data-ttu-id="16a52-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="16a52-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="16a52-132">MOF</span><span class="sxs-lookup"><span data-stu-id="16a52-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16a52-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="16a52-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16a52-134">DLL</span><span class="sxs-lookup"><span data-stu-id="16a52-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16a52-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16a52-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="16a52-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16a52-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a52-137">**CIM \_ 集合**</span><span class="sxs-lookup"><span data-stu-id="16a52-137">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

