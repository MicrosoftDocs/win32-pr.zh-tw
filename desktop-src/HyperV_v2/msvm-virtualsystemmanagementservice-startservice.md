---
description: 啟動服務。
ms.assetid: 1a1819de-823e-4e97-9c04-fcaeea2c67d9
title: Msvm_VirtualSystemManagementService 類別的 StartService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 887999e19276c29a9501ddd5d86fba45bdbaeb92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510994"
---
# <a name="startservice-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="57aa9-103">Msvm VirtualSystemManagementService 類別的 StartService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="57aa9-103">StartService method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="57aa9-104">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="57aa9-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="57aa9-105">語法</span><span class="sxs-lookup"><span data-stu-id="57aa9-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="57aa9-106">參數</span><span class="sxs-lookup"><span data-stu-id="57aa9-106">Parameters</span></span>

<span data-ttu-id="57aa9-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="57aa9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="57aa9-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="57aa9-108">Return value</span></span>

<span data-ttu-id="57aa9-109">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="57aa9-109">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="57aa9-110">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="57aa9-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="57aa9-111">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="57aa9-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="57aa9-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="57aa9-112">Requirements</span></span>



| <span data-ttu-id="57aa9-113">需求</span><span class="sxs-lookup"><span data-stu-id="57aa9-113">Requirement</span></span> | <span data-ttu-id="57aa9-114">值</span><span class="sxs-lookup"><span data-stu-id="57aa9-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57aa9-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57aa9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="57aa9-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="57aa9-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="57aa9-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57aa9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="57aa9-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="57aa9-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="57aa9-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="57aa9-119">Namespace</span></span><br/>                | <span data-ttu-id="57aa9-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="57aa9-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="57aa9-121">MOF</span><span class="sxs-lookup"><span data-stu-id="57aa9-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57aa9-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="57aa9-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="57aa9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="57aa9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57aa9-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="57aa9-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="57aa9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57aa9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57aa9-126">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="57aa9-126">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




