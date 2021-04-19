---
description: 用來建立、摧毀和匯出虛擬系統快照集集合的服務。
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Msvm_CollectionSnapshotService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9e835ad54773d69fab19861c7a9c417ac7d8a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993059"
---
# <a name="msvm_collectionsnapshotservice-class"></a><span data-ttu-id="68949-103">Msvm \_ CollectionSnapshotService 類別</span><span class="sxs-lookup"><span data-stu-id="68949-103">Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="68949-104">用來建立、摧毀和匯出虛擬系統快照集集合的服務。</span><span class="sxs-lookup"><span data-stu-id="68949-104">Service to create, destroy and export snapshot collection of virtual systems.</span></span>

<span data-ttu-id="68949-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="68949-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="68949-106">語法</span><span class="sxs-lookup"><span data-stu-id="68949-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="68949-107">成員</span><span class="sxs-lookup"><span data-stu-id="68949-107">Members</span></span>

<span data-ttu-id="68949-108">**Msvm \_ CollectionSnapshotService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="68949-108">The **Msvm\_CollectionSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="68949-109">方法</span><span class="sxs-lookup"><span data-stu-id="68949-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="68949-110">方法</span><span class="sxs-lookup"><span data-stu-id="68949-110">Methods</span></span>

<span data-ttu-id="68949-111">**Msvm \_ CollectionSnapshotService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="68949-111">The **Msvm\_CollectionSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="68949-112">方法</span><span class="sxs-lookup"><span data-stu-id="68949-112">Method</span></span>                                                                                    | <span data-ttu-id="68949-113">描述</span><span class="sxs-lookup"><span data-stu-id="68949-113">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68949-114">**ApplySnapshot**</span><span class="sxs-lookup"><span data-stu-id="68949-114">**ApplySnapshot**</span></span>](msvm-collectionsnapshotservice-applysnapshot.md)                     | <span data-ttu-id="68949-115">將快照集集合套用至虛擬電腦系統的集合。</span><span class="sxs-lookup"><span data-stu-id="68949-115">Applies a snapshot collection to the collection of virtual computer system.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="68949-116">**ConvertToReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="68949-116">**ConvertToReferencePoint**</span></span>](msvm-collectionsnapshotservice-converttoreferencepoint.md) | <span data-ttu-id="68949-117">將現有的集合快照集轉換為參考點集合。</span><span class="sxs-lookup"><span data-stu-id="68949-117">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="68949-118">快照集集合被刪除為副作用。</span><span class="sxs-lookup"><span data-stu-id="68949-118">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="68949-119">只有修復快照集可以轉換成參考點。</span><span class="sxs-lookup"><span data-stu-id="68949-119">Only recovery snapshots can be converted to reference points.</span></span><br/>                      |
| [<span data-ttu-id="68949-120">**>icloudblob.createsnapshot**</span><span class="sxs-lookup"><span data-stu-id="68949-120">**CreateSnapshot**</span></span>](msvm-collectionsnapshotservice-createsnapshot.md)                   | <span data-ttu-id="68949-121">建立虛擬系統集合的快照集。</span><span class="sxs-lookup"><span data-stu-id="68949-121">Creates a snapshot of a virtual system collection.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="68949-122">**DestroySnapshot**</span><span class="sxs-lookup"><span data-stu-id="68949-122">**DestroySnapshot**</span></span>](msvm-collectionsnapshotservice-destroysnapshot.md)                 | <span data-ttu-id="68949-123">終結虛擬系統集合的現有快照集。</span><span class="sxs-lookup"><span data-stu-id="68949-123">Destroy an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="68949-124">這個方法可能會損毀其他相依于受影響快照集的快照集。</span><span class="sxs-lookup"><span data-stu-id="68949-124">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span><br/>                                                   |
| [<span data-ttu-id="68949-125">**ExportSnapshot**</span><span class="sxs-lookup"><span data-stu-id="68949-125">**ExportSnapshot**</span></span>](msvm-collectionsnapshotservice-exportsnapshot.md)                   | <span data-ttu-id="68949-126">將虛擬電腦系統的快照集集合匯出到檔案。</span><span class="sxs-lookup"><span data-stu-id="68949-126">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="68949-127">快照集集合、其相關聯的設定設定，以及其相關聯的資源設定將會保留在產生的檔案中。</span><span class="sxs-lookup"><span data-stu-id="68949-127">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="68949-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="68949-128">Requirements</span></span>



| <span data-ttu-id="68949-129">需求</span><span class="sxs-lookup"><span data-stu-id="68949-129">Requirement</span></span> | <span data-ttu-id="68949-130">值</span><span class="sxs-lookup"><span data-stu-id="68949-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68949-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68949-131">Minimum supported client</span></span><br/> | <span data-ttu-id="68949-132">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68949-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="68949-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68949-133">Minimum supported server</span></span><br/> | <span data-ttu-id="68949-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="68949-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="68949-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="68949-135">Namespace</span></span><br/>                | <span data-ttu-id="68949-136">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="68949-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="68949-137">MOF</span><span class="sxs-lookup"><span data-stu-id="68949-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68949-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="68949-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="68949-139">DLL</span><span class="sxs-lookup"><span data-stu-id="68949-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68949-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68949-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="68949-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68949-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68949-142">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="68949-142">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




