---
description: 表示管理虛擬系統的服務。
ms.assetid: b2645546-3c04-4d3f-8d53-019a6db08e24
title: CIM_VirtualSystemManagementService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9db9e85e158f546a3a8780f1211ecd7a7dfc3c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979110"
---
# <a name="cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="1548f-103">CIM \_ VirtualSystemManagementService 類別</span><span class="sxs-lookup"><span data-stu-id="1548f-103">CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="1548f-104">表示管理虛擬系統的服務。</span><span class="sxs-lookup"><span data-stu-id="1548f-104">Represents a service that manages virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="1548f-105">語法</span><span class="sxs-lookup"><span data-stu-id="1548f-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="1548f-106">成員</span><span class="sxs-lookup"><span data-stu-id="1548f-106">Members</span></span>

<span data-ttu-id="1548f-107">**CIM \_ VirtualSystemManagementService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1548f-107">The **CIM\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="1548f-108">方法</span><span class="sxs-lookup"><span data-stu-id="1548f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1548f-109">方法</span><span class="sxs-lookup"><span data-stu-id="1548f-109">Methods</span></span>

<span data-ttu-id="1548f-110">**CIM \_ VirtualSystemManagementService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1548f-110">The **CIM\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="1548f-111">方法</span><span class="sxs-lookup"><span data-stu-id="1548f-111">Method</span></span>                                                                                      | <span data-ttu-id="1548f-112">描述</span><span class="sxs-lookup"><span data-stu-id="1548f-112">Description</span></span>                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="1548f-113">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="1548f-113">**AddResourceSettings**</span></span>](cim-virtualsystemmanagementservice-addresourcesettings.md)       | <span data-ttu-id="1548f-114">將資源新增至虛擬系統設定。</span><span class="sxs-lookup"><span data-stu-id="1548f-114">Adds resources to a virtual system configuration.</span></span><br/>                          |
| [<span data-ttu-id="1548f-115">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="1548f-115">**DefineSystem**</span></span>](cim-virtualsystemmanagementservice-definesystem.md)                     | <span data-ttu-id="1548f-116">定義虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="1548f-116">Defines a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="1548f-117">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="1548f-117">**DestroySystem**</span></span>](cim-virtualsystemmanagementservice-destroysystem.md)                   | <span data-ttu-id="1548f-118">刪除虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="1548f-118">Deletes a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="1548f-119">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="1548f-119">**ModifyResourceSettings**</span></span>](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | <span data-ttu-id="1548f-120">修改虛擬系統組態的虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="1548f-120">Modifies the virtual resource settings for a virtual system configuration.</span></span><br/> |
| [<span data-ttu-id="1548f-121">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="1548f-121">**ModifySystemSettings**</span></span>](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | <span data-ttu-id="1548f-122">修改虛擬系統設定。</span><span class="sxs-lookup"><span data-stu-id="1548f-122">Modifies virtual system settings.</span></span><br/>                                          |
| [<span data-ttu-id="1548f-123">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="1548f-123">**RemoveResourceSettings**</span></span>](cim-virtualsystemmanagementservice-removeresourcesettings.md) | <span data-ttu-id="1548f-124">從虛擬系統組態移除虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="1548f-124">Removes virtual resource settings from a virtual system configuration.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="1548f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="1548f-125">Requirements</span></span>



| <span data-ttu-id="1548f-126">需求</span><span class="sxs-lookup"><span data-stu-id="1548f-126">Requirement</span></span> | <span data-ttu-id="1548f-127">值</span><span class="sxs-lookup"><span data-stu-id="1548f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1548f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1548f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1548f-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1548f-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1548f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1548f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1548f-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1548f-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1548f-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="1548f-132">Namespace</span></span><br/>                | <span data-ttu-id="1548f-133">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="1548f-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1548f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1548f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1548f-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1548f-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1548f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1548f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1548f-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1548f-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1548f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1548f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1548f-139">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="1548f-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




