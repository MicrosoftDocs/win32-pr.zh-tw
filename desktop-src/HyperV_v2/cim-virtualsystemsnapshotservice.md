---
description: 代表可建立、套用及刪除虛擬系統快照集的服務。
ms.assetid: 8d5d54a2-08f1-4f24-bca3-601dc698d018
title: CIM_VirtualSystemSnapshotService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ae74f85d1af9867b7a95c23aeda670b8f06f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853167"
---
# <a name="cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="678d6-103">CIM \_ VirtualSystemSnapshotService 類別</span><span class="sxs-lookup"><span data-stu-id="678d6-103">CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="678d6-104">代表可建立、套用及刪除虛擬系統快照集的服務。</span><span class="sxs-lookup"><span data-stu-id="678d6-104">Represents a service that can create, apply, and delete snapshots of virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="678d6-105">語法</span><span class="sxs-lookup"><span data-stu-id="678d6-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="678d6-106">成員</span><span class="sxs-lookup"><span data-stu-id="678d6-106">Members</span></span>

<span data-ttu-id="678d6-107">**CIM \_ VirtualSystemSnapshotService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="678d6-107">The **CIM\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="678d6-108">方法</span><span class="sxs-lookup"><span data-stu-id="678d6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="678d6-109">方法</span><span class="sxs-lookup"><span data-stu-id="678d6-109">Methods</span></span>

<span data-ttu-id="678d6-110">**CIM \_ VirtualSystemSnapshotService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="678d6-110">The **CIM\_VirtualSystemSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="678d6-111">方法</span><span class="sxs-lookup"><span data-stu-id="678d6-111">Method</span></span>                                                                      | <span data-ttu-id="678d6-112">描述</span><span class="sxs-lookup"><span data-stu-id="678d6-112">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="678d6-113">**ApplySnapshot**</span><span class="sxs-lookup"><span data-stu-id="678d6-113">**ApplySnapshot**</span></span>](cim-virtualsystemsnapshotservice-applysnapshot.md)     | <span data-ttu-id="678d6-114">將虛擬系統快照集套用至虛擬系統，以進行來源虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="678d6-114">Applies a virtual system snapshot to the virtual system to the source virtual system.</span></span><br/> |
| [<span data-ttu-id="678d6-115">**>icloudblob.createsnapshot**</span><span class="sxs-lookup"><span data-stu-id="678d6-115">**CreateSnapshot**</span></span>](cim-virtualsystemsnapshotservice-createsnapshot.md)   | <span data-ttu-id="678d6-116">建立虛擬系統的快照集。</span><span class="sxs-lookup"><span data-stu-id="678d6-116">Creates a snapshot of a virtual system.</span></span><br/>                                               |
| [<span data-ttu-id="678d6-117">**DestroySnapshot**</span><span class="sxs-lookup"><span data-stu-id="678d6-117">**DestroySnapshot**</span></span>](cim-virtualsystemsnapshotservice-destroysnapshot.md) | <span data-ttu-id="678d6-118">刪除虛擬系統快照集。</span><span class="sxs-lookup"><span data-stu-id="678d6-118">Deletes a virtual system snapshot.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="678d6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="678d6-119">Requirements</span></span>



| <span data-ttu-id="678d6-120">需求</span><span class="sxs-lookup"><span data-stu-id="678d6-120">Requirement</span></span> | <span data-ttu-id="678d6-121">值</span><span class="sxs-lookup"><span data-stu-id="678d6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="678d6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="678d6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="678d6-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="678d6-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="678d6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="678d6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="678d6-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="678d6-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="678d6-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="678d6-126">Namespace</span></span><br/>                | <span data-ttu-id="678d6-127">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="678d6-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="678d6-128">MOF</span><span class="sxs-lookup"><span data-stu-id="678d6-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="678d6-129"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="678d6-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="678d6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="678d6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="678d6-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="678d6-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="678d6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="678d6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="678d6-133">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="678d6-133">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




