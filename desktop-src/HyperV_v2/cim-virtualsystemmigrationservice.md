---
description: 代表控制主機系統間虛擬系統移轉的服務。 此類別也會確認暫止的遷移是否可能成功。
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: CIM_VirtualSystemMigrationService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6343cec0573a97656368d66426ec9b46c7255e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849018"
---
# <a name="cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="d5a8e-104">CIM \_ VirtualSystemMigrationService 類別</span><span class="sxs-lookup"><span data-stu-id="d5a8e-104">CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="d5a8e-105">代表控制主機系統間虛擬系統移轉的服務。</span><span class="sxs-lookup"><span data-stu-id="d5a8e-105">Represents a service that controls the migration of virtual systems between host systems.</span></span> <span data-ttu-id="d5a8e-106">此類別也會確認暫止的遷移是否可能成功。</span><span class="sxs-lookup"><span data-stu-id="d5a8e-106">This class also verifies whether a pending migration is likely to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5a8e-107">語法</span><span class="sxs-lookup"><span data-stu-id="d5a8e-107">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="d5a8e-108">成員</span><span class="sxs-lookup"><span data-stu-id="d5a8e-108">Members</span></span>

<span data-ttu-id="d5a8e-109">**CIM \_ VirtualSystemMigrationService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d5a8e-109">The **CIM\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="d5a8e-110">方法</span><span class="sxs-lookup"><span data-stu-id="d5a8e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d5a8e-111">方法</span><span class="sxs-lookup"><span data-stu-id="d5a8e-111">Methods</span></span>

<span data-ttu-id="d5a8e-112">**CIM \_ VirtualSystemMigrationService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d5a8e-112">The **CIM\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="d5a8e-113">方法</span><span class="sxs-lookup"><span data-stu-id="d5a8e-113">Method</span></span>                                                                                                                     | <span data-ttu-id="d5a8e-114">描述</span><span class="sxs-lookup"><span data-stu-id="d5a8e-114">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5a8e-115">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="d5a8e-115">**CheckVirtualSystemIsMigratableToHost**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | <span data-ttu-id="d5a8e-116">確認暫止的虛擬系統移轉至主機是否可能成功。</span><span class="sxs-lookup"><span data-stu-id="d5a8e-116">Verifies whether a pending virtual system migration to a host is likely to succeed.</span></span><br/>   |
| [<span data-ttu-id="d5a8e-117">**CheckVirtualSystemIsMigratableToSystem**</span><span class="sxs-lookup"><span data-stu-id="d5a8e-117">**CheckVirtualSystemIsMigratableToSystem**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | <span data-ttu-id="d5a8e-118">確認暫止的虛擬系統移轉至系統是否可能成功。</span><span class="sxs-lookup"><span data-stu-id="d5a8e-118">Verifies whether a pending virtual system migration to a system is likely to succeed.</span></span><br/> |
| [<span data-ttu-id="d5a8e-119">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="d5a8e-119">**MigrateVirtualSystemToHost**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | <span data-ttu-id="d5a8e-120">將虛擬系統移轉至目標主機。</span><span class="sxs-lookup"><span data-stu-id="d5a8e-120">Migrates a virtual system to a target host.</span></span><br/>                                           |
| [<span data-ttu-id="d5a8e-121">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="d5a8e-121">**MigrateVirtualSystemToSystem**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | <span data-ttu-id="d5a8e-122">將虛擬系統移轉至目標系統。</span><span class="sxs-lookup"><span data-stu-id="d5a8e-122">Migrates a virtual system to target system.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="d5a8e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5a8e-123">Requirements</span></span>



| <span data-ttu-id="d5a8e-124">需求</span><span class="sxs-lookup"><span data-stu-id="d5a8e-124">Requirement</span></span> | <span data-ttu-id="d5a8e-125">值</span><span class="sxs-lookup"><span data-stu-id="d5a8e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a8e-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5a8e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d5a8e-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d5a8e-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d5a8e-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5a8e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d5a8e-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5a8e-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d5a8e-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="d5a8e-130">Namespace</span></span><br/>                | <span data-ttu-id="d5a8e-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d5a8e-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d5a8e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d5a8e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5a8e-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d5a8e-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5a8e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d5a8e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5a8e-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d5a8e-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d5a8e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5a8e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5a8e-137">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="d5a8e-137">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




