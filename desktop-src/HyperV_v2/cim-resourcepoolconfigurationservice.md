---
description: 使用作業管理資源集區的設定。
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: CIM_ResourcePoolConfigurationService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e8dbbce21f7749b7f436e2f49acb7ce6c7340faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848164"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="719fa-103">CIM \_ ResourcePoolConfigurationService 類別</span><span class="sxs-lookup"><span data-stu-id="719fa-103">CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="719fa-104">使用作業管理資源集區的設定。</span><span class="sxs-lookup"><span data-stu-id="719fa-104">Manages the configuration of resource pools by using jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="719fa-105">語法</span><span class="sxs-lookup"><span data-stu-id="719fa-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="719fa-106">成員</span><span class="sxs-lookup"><span data-stu-id="719fa-106">Members</span></span>

<span data-ttu-id="719fa-107">**CIM \_ ResourcePoolConfigurationService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="719fa-107">The **CIM\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="719fa-108">方法</span><span class="sxs-lookup"><span data-stu-id="719fa-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="719fa-109">方法</span><span class="sxs-lookup"><span data-stu-id="719fa-109">Methods</span></span>

<span data-ttu-id="719fa-110">**CIM \_ ResourcePoolConfigurationService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="719fa-110">The **CIM\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="719fa-111">方法</span><span class="sxs-lookup"><span data-stu-id="719fa-111">Method</span></span>                                                                                                          | <span data-ttu-id="719fa-112">描述</span><span class="sxs-lookup"><span data-stu-id="719fa-112">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="719fa-113">**AddResourcesToResourcePool**</span><span class="sxs-lookup"><span data-stu-id="719fa-113">**AddResourcesToResourcePool**</span></span>](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | <span data-ttu-id="719fa-114">啟動將資源新增至資源集區的作業。</span><span class="sxs-lookup"><span data-stu-id="719fa-114">Starts a job to add resources to a resource pool.</span></span><br/>                  |
| [<span data-ttu-id="719fa-115">**ChangeParentResourcePool**</span><span class="sxs-lookup"><span data-stu-id="719fa-115">**ChangeParentResourcePool**</span></span>](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | <span data-ttu-id="719fa-116">開始作業來變更資源集區的父資源集區。</span><span class="sxs-lookup"><span data-stu-id="719fa-116">Start a job to change the parent resource pool of a resource pool.</span></span><br/> |
| [<span data-ttu-id="719fa-117">**CreateChildResourcePool**</span><span class="sxs-lookup"><span data-stu-id="719fa-117">**CreateChildResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | <span data-ttu-id="719fa-118">啟動作業，從父資源集區建立資源集區。</span><span class="sxs-lookup"><span data-stu-id="719fa-118">Start a job to create a resource pool from a parent resource pool.</span></span><br/> |
| [<span data-ttu-id="719fa-119">**CreateResourcePool**</span><span class="sxs-lookup"><span data-stu-id="719fa-119">**CreateResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | <span data-ttu-id="719fa-120">啟動建立根資源集區的作業。</span><span class="sxs-lookup"><span data-stu-id="719fa-120">Starts a job to create a root resource pool.</span></span><br/>                       |
| [<span data-ttu-id="719fa-121">**DeleteResourcePool**</span><span class="sxs-lookup"><span data-stu-id="719fa-121">**DeleteResourcePool**</span></span>](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | <span data-ttu-id="719fa-122">啟動工作以刪除資源集區。</span><span class="sxs-lookup"><span data-stu-id="719fa-122">Start a job to delete a resource pool.</span></span><br/>                             |
| [<span data-ttu-id="719fa-123">**RemoveResourcesFromResourcePool**</span><span class="sxs-lookup"><span data-stu-id="719fa-123">**RemoveResourcesFromResourcePool**</span></span>](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | <span data-ttu-id="719fa-124">啟動作業，以從資源集區中移除資源。</span><span class="sxs-lookup"><span data-stu-id="719fa-124">Starts a job to remove resources from a resource pool.</span></span><br/>             |



 

## <a name="requirements"></a><span data-ttu-id="719fa-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="719fa-125">Requirements</span></span>



| <span data-ttu-id="719fa-126">需求</span><span class="sxs-lookup"><span data-stu-id="719fa-126">Requirement</span></span> | <span data-ttu-id="719fa-127">值</span><span class="sxs-lookup"><span data-stu-id="719fa-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="719fa-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="719fa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="719fa-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="719fa-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="719fa-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="719fa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="719fa-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="719fa-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="719fa-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="719fa-132">Namespace</span></span><br/>                | <span data-ttu-id="719fa-133">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="719fa-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="719fa-134">MOF</span><span class="sxs-lookup"><span data-stu-id="719fa-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="719fa-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="719fa-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="719fa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="719fa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="719fa-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="719fa-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="719fa-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="719fa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="719fa-139">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="719fa-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




