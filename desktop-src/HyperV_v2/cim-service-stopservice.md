---
description: 步調處于已停止狀態的服務。
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: 'CIM_Service 類別的 StopService 方法 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4eb354a48b074bad8adac4d5635e204844c31b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848163"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a><span data-ttu-id="c488a-103">CIM_Service 類別的 StopService 方法 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="c488a-103">StopService method of the CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="c488a-104">步調處于已停止狀態的服務。</span><span class="sxs-lookup"><span data-stu-id="c488a-104">Paces the service in the stopped state.</span></span>

> [!Note]
>
> <span data-ttu-id="c488a-105">這個方法的語法與繼承自 [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)的 **RequestStateChange** 方法重迭。</span><span class="sxs-lookup"><span data-stu-id="c488a-105">The semantics of this method overlap with the **RequestStateChange** method that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span> <span data-ttu-id="c488a-106">因為此方法已廣泛實行，所以會維護此方法，且其簡單的「停止」語義很方便使用。</span><span class="sxs-lookup"><span data-stu-id="c488a-106">This method is maintained because it has been widely implemented, and its simple "stop" semantics are convenient to use.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c488a-107">語法</span><span class="sxs-lookup"><span data-stu-id="c488a-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="c488a-108">參數</span><span class="sxs-lookup"><span data-stu-id="c488a-108">Parameters</span></span>

<span data-ttu-id="c488a-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c488a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c488a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c488a-110">Return value</span></span>

<span data-ttu-id="c488a-111">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c488a-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c488a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c488a-112">Requirements</span></span>



| <span data-ttu-id="c488a-113">需求</span><span class="sxs-lookup"><span data-stu-id="c488a-113">Requirement</span></span> | <span data-ttu-id="c488a-114">值</span><span class="sxs-lookup"><span data-stu-id="c488a-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c488a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c488a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c488a-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c488a-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c488a-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c488a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c488a-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c488a-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c488a-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="c488a-119">Namespace</span></span><br/>                | <span data-ttu-id="c488a-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c488a-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c488a-121">MOF</span><span class="sxs-lookup"><span data-stu-id="c488a-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c488a-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c488a-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c488a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c488a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c488a-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c488a-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c488a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c488a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c488a-126">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="c488a-126">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




