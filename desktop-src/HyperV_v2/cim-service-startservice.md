---
description: 將服務置於啟動狀態。
ms.assetid: 8977b806-150c-4ddc-a471-3fdafdcb4a55
title: 'CIM_Service 類別的 StartService 方法 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 73b89f7fc789639fb45acbde61da4c7962650177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972244"
---
# <a name="startservice-method-of-the-cim_service-class-hyper-v-management"></a><span data-ttu-id="a21b7-103">CIM_Service 類別的 StartService 方法 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="a21b7-103">StartService method of the CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="a21b7-104">將服務置於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="a21b7-104">Places the service in the started state.</span></span>

> [!Note]
>
> <span data-ttu-id="a21b7-105">這個方法的語法與繼承自 [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)的 **RequestStateChange** 方法重迭。</span><span class="sxs-lookup"><span data-stu-id="a21b7-105">The semantics of this method overlap with the **RequestStateChange** method that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span> <span data-ttu-id="a21b7-106">因為此方法已廣泛實行，所以會維護此方法，且其簡單的 "start" 語義很方便使用。</span><span class="sxs-lookup"><span data-stu-id="a21b7-106">This method is maintained because it has been widely implemented, and its simple "start" semantics are convenient to use.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a21b7-107">語法</span><span class="sxs-lookup"><span data-stu-id="a21b7-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="a21b7-108">參數</span><span class="sxs-lookup"><span data-stu-id="a21b7-108">Parameters</span></span>

<span data-ttu-id="a21b7-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a21b7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a21b7-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a21b7-110">Return value</span></span>

<span data-ttu-id="a21b7-111">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a21b7-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a21b7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a21b7-112">Requirements</span></span>



| <span data-ttu-id="a21b7-113">需求</span><span class="sxs-lookup"><span data-stu-id="a21b7-113">Requirement</span></span> | <span data-ttu-id="a21b7-114">值</span><span class="sxs-lookup"><span data-stu-id="a21b7-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a21b7-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a21b7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a21b7-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a21b7-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a21b7-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a21b7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a21b7-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a21b7-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a21b7-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="a21b7-119">Namespace</span></span><br/>                | <span data-ttu-id="a21b7-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a21b7-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a21b7-121">MOF</span><span class="sxs-lookup"><span data-stu-id="a21b7-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a21b7-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a21b7-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a21b7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a21b7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a21b7-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a21b7-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a21b7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a21b7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a21b7-126">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="a21b7-126">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




