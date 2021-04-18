---
description: 用來建立、摧毀和匯出參考點的服務。
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Msvm_CollectionReferencePointService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6ba56fcb75a177521b8f3ea3ae0675cfdd8a8dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971451"
---
# <a name="msvm_collectionreferencepointservice-class"></a><span data-ttu-id="b876f-103">Msvm \_ CollectionReferencePointService 類別</span><span class="sxs-lookup"><span data-stu-id="b876f-103">Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="b876f-104">用來建立、摧毀和匯出參考點的服務</span><span class="sxs-lookup"><span data-stu-id="b876f-104">Service to create, destroy and export reference points</span></span>

<span data-ttu-id="b876f-105">的虛擬系統集合。</span><span class="sxs-lookup"><span data-stu-id="b876f-105">of virtual system collections.</span></span>

<span data-ttu-id="b876f-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b876f-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b876f-107">語法</span><span class="sxs-lookup"><span data-stu-id="b876f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="b876f-108">成員</span><span class="sxs-lookup"><span data-stu-id="b876f-108">Members</span></span>

<span data-ttu-id="b876f-109">**Msvm \_ CollectionReferencePointService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b876f-109">The **Msvm\_CollectionReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="b876f-110">方法</span><span class="sxs-lookup"><span data-stu-id="b876f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b876f-111">方法</span><span class="sxs-lookup"><span data-stu-id="b876f-111">Methods</span></span>

<span data-ttu-id="b876f-112">**Msvm \_ CollectionReferencePointService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b876f-112">The **Msvm\_CollectionReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="b876f-113">方法</span><span class="sxs-lookup"><span data-stu-id="b876f-113">Method</span></span>                                                                                      | <span data-ttu-id="b876f-114">描述</span><span class="sxs-lookup"><span data-stu-id="b876f-114">Description</span></span>                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b876f-115">**CreateReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="b876f-115">**CreateReferencePoint**</span></span>](msvm-collectionreferencepointservice-createreferencepoint.md)   | <span data-ttu-id="b876f-116">建立虛擬系統集合的參考點。</span><span class="sxs-lookup"><span data-stu-id="b876f-116">Creates a reference point of a virtual system collection.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="b876f-117">**DestroyReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="b876f-117">**DestroyReferencePoint**</span></span>](msvm-collectionreferencepointservice-destroyreferencepoint.md) | <span data-ttu-id="b876f-118">終結現有的參考點集合。</span><span class="sxs-lookup"><span data-stu-id="b876f-118">Destroys an existing reference point collection.</span></span> <span data-ttu-id="b876f-119">這個方法可能會損毀其他相依于受影響之參考點集合的參考點。</span><span class="sxs-lookup"><span data-stu-id="b876f-119">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span><br/>                      |
| [<span data-ttu-id="b876f-120">**ExportReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="b876f-120">**ExportReferencePoint**</span></span>](msvm-collectionreferencepointservice-exportreferencepoint.md)   | <span data-ttu-id="b876f-121">將參考點集合匯出到檔案。</span><span class="sxs-lookup"><span data-stu-id="b876f-121">Exports a reference point collection to a file.</span></span> <span data-ttu-id="b876f-122">參考點集合、其相關聯的設定設定，以及其相關聯的資源設定將會保留在產生的檔案中。</span><span class="sxs-lookup"><span data-stu-id="b876f-122">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |
| [<span data-ttu-id="b876f-123">**RemoveAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="b876f-123">**RemoveAssociatedData**</span></span>](msvm-collectionreferencepointservice-removeassociateddata.md)   | <span data-ttu-id="b876f-124">移除與參考點關聯的資料記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b876f-124">Removes the data log associated with the reference point.</span></span><br/>                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="b876f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b876f-125">Requirements</span></span>



| <span data-ttu-id="b876f-126">需求</span><span class="sxs-lookup"><span data-stu-id="b876f-126">Requirement</span></span> | <span data-ttu-id="b876f-127">值</span><span class="sxs-lookup"><span data-stu-id="b876f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b876f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b876f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b876f-129">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b876f-129">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b876f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b876f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b876f-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b876f-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b876f-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="b876f-132">Namespace</span></span><br/>                | <span data-ttu-id="b876f-133">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b876f-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b876f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b876f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b876f-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b876f-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b876f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b876f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b876f-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b876f-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b876f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b876f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b876f-139">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="b876f-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




