---
description: 描述虛擬系統參考點服務。
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Msvm_VirtualSystemReferencePointService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0614349ed6f6358316826bbfc2cd10ac55cba953
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106979851"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="d3067-103">Msvm \_ VirtualSystemReferencePointService 類別</span><span class="sxs-lookup"><span data-stu-id="d3067-103">Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="d3067-104">描述虛擬系統參考點服務。</span><span class="sxs-lookup"><span data-stu-id="d3067-104">Describes a virtual system reference point service.</span></span>

<span data-ttu-id="d3067-105">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d3067-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3067-106">語法</span><span class="sxs-lookup"><span data-stu-id="d3067-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="d3067-107">成員</span><span class="sxs-lookup"><span data-stu-id="d3067-107">Members</span></span>

<span data-ttu-id="d3067-108">**Msvm \_ VirtualSystemReferencePointService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d3067-108">The **Msvm\_VirtualSystemReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="d3067-109">方法</span><span class="sxs-lookup"><span data-stu-id="d3067-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d3067-110">方法</span><span class="sxs-lookup"><span data-stu-id="d3067-110">Methods</span></span>

<span data-ttu-id="d3067-111">**Msvm \_ VirtualSystemReferencePointService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d3067-111">The **Msvm\_VirtualSystemReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="d3067-112">方法</span><span class="sxs-lookup"><span data-stu-id="d3067-112">Method</span></span>                                                                                                       | <span data-ttu-id="d3067-113">描述</span><span class="sxs-lookup"><span data-stu-id="d3067-113">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="d3067-114">**CreateReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="d3067-114">**CreateReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | <span data-ttu-id="d3067-115">建立虛擬系統的參考點。</span><span class="sxs-lookup"><span data-stu-id="d3067-115">Creates a reference point of a virtual system.</span></span><br/>            |
| [<span data-ttu-id="d3067-116">**DestroyReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="d3067-116">**DestroyReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | <span data-ttu-id="d3067-117">刪除指定的參考點。</span><span class="sxs-lookup"><span data-stu-id="d3067-117">Deletes the specified reference point.</span></span><br/>                    |
| [<span data-ttu-id="d3067-118">**ExportReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="d3067-118">**ExportReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | <span data-ttu-id="d3067-119">匯出虛擬系統的參考點。</span><span class="sxs-lookup"><span data-stu-id="d3067-119">Exports the reference point of the virtual system.</span></span><br/>        |
| [<span data-ttu-id="d3067-120">**ImportReferencePointMetadata**</span><span class="sxs-lookup"><span data-stu-id="d3067-120">**ImportReferencePointMetadata**</span></span>](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | <span data-ttu-id="d3067-121">匯入虛擬系統的參考點中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d3067-121">Imports reference point metadata of the virtual system.</span></span><br/>   |
| [<span data-ttu-id="d3067-122">**RemoveAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="d3067-122">**RemoveAssociatedData**</span></span>](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | <span data-ttu-id="d3067-123">移除與參考點關聯的資料記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d3067-123">Removes the data log associated with the reference point.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d3067-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3067-124">Requirements</span></span>



| <span data-ttu-id="d3067-125">需求</span><span class="sxs-lookup"><span data-stu-id="d3067-125">Requirement</span></span> | <span data-ttu-id="d3067-126">值</span><span class="sxs-lookup"><span data-stu-id="d3067-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3067-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3067-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d3067-128">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3067-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d3067-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3067-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d3067-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d3067-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d3067-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="d3067-131">Namespace</span></span><br/>                | <span data-ttu-id="d3067-132">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d3067-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d3067-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d3067-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3067-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d3067-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3067-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d3067-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3067-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3067-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d3067-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3067-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3067-138">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="d3067-138">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




