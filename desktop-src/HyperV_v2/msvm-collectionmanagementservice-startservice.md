---
description: 停止服務。
ms.assetid: 0f9a015d-b895-496a-a4c6-2737c0742746
title: Msvm_CollectionManagementService 類別的 StartService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f76fa9e5069c2a9e19b83a8ab83136879c6657e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979843"
---
# <a name="startservice-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="942b9-103">Msvm CollectionManagementService 類別的 StartService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="942b9-103">StartService method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="942b9-104">停止服務。</span><span class="sxs-lookup"><span data-stu-id="942b9-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="942b9-105">語法</span><span class="sxs-lookup"><span data-stu-id="942b9-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="942b9-106">參數</span><span class="sxs-lookup"><span data-stu-id="942b9-106">Parameters</span></span>

<span data-ttu-id="942b9-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="942b9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="942b9-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="942b9-108">Return value</span></span>

<span data-ttu-id="942b9-109">如果成功，則傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="942b9-109">Returns 0 if successful; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="942b9-110">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="942b9-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="942b9-111">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="942b9-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="942b9-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="942b9-112">Requirements</span></span>



| <span data-ttu-id="942b9-113">需求</span><span class="sxs-lookup"><span data-stu-id="942b9-113">Requirement</span></span> | <span data-ttu-id="942b9-114">值</span><span class="sxs-lookup"><span data-stu-id="942b9-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="942b9-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="942b9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="942b9-116">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="942b9-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="942b9-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="942b9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="942b9-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="942b9-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="942b9-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="942b9-119">Namespace</span></span><br/>                | <span data-ttu-id="942b9-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="942b9-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="942b9-121">MOF</span><span class="sxs-lookup"><span data-stu-id="942b9-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="942b9-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="942b9-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="942b9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="942b9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="942b9-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="942b9-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="942b9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="942b9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="942b9-126">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="942b9-126">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




