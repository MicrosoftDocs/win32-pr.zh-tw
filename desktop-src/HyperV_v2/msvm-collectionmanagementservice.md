---
description: 管理 Hyper-v 主機上的集合。
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Msvm_CollectionManagementService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695639"
---
# <a name="msvm_collectionmanagementservice-class"></a><span data-ttu-id="e380b-103">Msvm \_ CollectionManagementService 類別</span><span class="sxs-lookup"><span data-stu-id="e380b-103">Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="e380b-104">管理 Hyper-v 主機上的集合。</span><span class="sxs-lookup"><span data-stu-id="e380b-104">Manages the collections on the Hyper-V host.</span></span>

<span data-ttu-id="e380b-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e380b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e380b-106">語法</span><span class="sxs-lookup"><span data-stu-id="e380b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="e380b-107">成員</span><span class="sxs-lookup"><span data-stu-id="e380b-107">Members</span></span>

<span data-ttu-id="e380b-108">**Msvm \_ CollectionManagementService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e380b-108">The **Msvm\_CollectionManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="e380b-109">方法</span><span class="sxs-lookup"><span data-stu-id="e380b-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e380b-110">方法</span><span class="sxs-lookup"><span data-stu-id="e380b-110">Methods</span></span>

<span data-ttu-id="e380b-111">**Msvm \_ CollectionManagementService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e380b-111">The **Msvm\_CollectionManagementService** class has these methods.</span></span>



| <span data-ttu-id="e380b-112">方法</span><span class="sxs-lookup"><span data-stu-id="e380b-112">Method</span></span>                                                                          | <span data-ttu-id="e380b-113">描述</span><span class="sxs-lookup"><span data-stu-id="e380b-113">Description</span></span>                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e380b-114">**AddMember**</span><span class="sxs-lookup"><span data-stu-id="e380b-114">**AddMember**</span></span>](msvm-collectionmanagementservice-addmember.md)                 | <span data-ttu-id="e380b-115">將指定的 ManagedElement 加入為指定之 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件的成員。</span><span class="sxs-lookup"><span data-stu-id="e380b-115">Adds the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                           |
| [<span data-ttu-id="e380b-116">**DefineCollection**</span><span class="sxs-lookup"><span data-stu-id="e380b-116">**DefineCollection**</span></span>](msvm-collectionmanagementservice-definecollection.md)   | <span data-ttu-id="e380b-117">建立新的 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e380b-117">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="e380b-118">**DestroyCollection**</span><span class="sxs-lookup"><span data-stu-id="e380b-118">**DestroyCollection**</span></span>](msvm-collectionmanagementservice-destroycollection.md) | <span data-ttu-id="e380b-119">刪除指定的 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e380b-119">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="e380b-120">**RemoveMember**</span><span class="sxs-lookup"><span data-stu-id="e380b-120">**RemoveMember**</span></span>](msvm-collectionmanagementservice-removemember.md)           | <span data-ttu-id="e380b-121">將指定的 ManagedElement 移除為指定之 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件的成員。</span><span class="sxs-lookup"><span data-stu-id="e380b-121">Removes the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="e380b-122">**RemoveMemberById**</span><span class="sxs-lookup"><span data-stu-id="e380b-122">**RemoveMemberById**</span></span>](msvm-collectionmanagementservice-removememberbyid.md)   | <span data-ttu-id="e380b-123">使用指定的識別碼，將指定的 ManagedElement 移除為 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 的成員。</span><span class="sxs-lookup"><span data-stu-id="e380b-123">Removes the specified ManagedElement as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="e380b-124">即使具有該識別碼的物件不存在，也會成功。</span><span class="sxs-lookup"><span data-stu-id="e380b-124">This will succeed even if the object with that identifier is not present.</span></span><br/> |
| [<span data-ttu-id="e380b-125">**RenameCollection**</span><span class="sxs-lookup"><span data-stu-id="e380b-125">**RenameCollection**</span></span>](msvm-collectionmanagementservice-renamecollection.md)   | <span data-ttu-id="e380b-126">更新指定之 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件的 ElementName。</span><span class="sxs-lookup"><span data-stu-id="e380b-126">Updates the ElementName the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="e380b-127">**StartService**</span><span class="sxs-lookup"><span data-stu-id="e380b-127">**StartService**</span></span>](msvm-collectionmanagementservice-startservice.md)           | <span data-ttu-id="e380b-128">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="e380b-128">Starts the service.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="e380b-129">**StopService**</span><span class="sxs-lookup"><span data-stu-id="e380b-129">**StopService**</span></span>](msvm-collectionmanagementservice-stopservice.md)             | <span data-ttu-id="e380b-130">停止服務。</span><span class="sxs-lookup"><span data-stu-id="e380b-130">Stops the service.</span></span><br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="e380b-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="e380b-131">Requirements</span></span>



| <span data-ttu-id="e380b-132">需求</span><span class="sxs-lookup"><span data-stu-id="e380b-132">Requirement</span></span> | <span data-ttu-id="e380b-133">值</span><span class="sxs-lookup"><span data-stu-id="e380b-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e380b-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e380b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e380b-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e380b-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e380b-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e380b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e380b-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e380b-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e380b-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="e380b-138">Namespace</span></span><br/>                | <span data-ttu-id="e380b-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e380b-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e380b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e380b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e380b-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e380b-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e380b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e380b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e380b-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e380b-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e380b-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e380b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e380b-145">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="e380b-145">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




