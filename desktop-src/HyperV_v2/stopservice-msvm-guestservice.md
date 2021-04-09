---
description: 停止來賓服務。
ms.assetid: 67FFA46C-0B61-4845-A617-BA10F4D42CBC
title: Msvm_GuestService：： StopService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6c396078e2bd623a768f391a645091679694f453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847913"
---
# <a name="msvm_guestservicestopservice-method"></a><span data-ttu-id="244bb-103">Msvm \_ GuestService：： StopService 方法</span><span class="sxs-lookup"><span data-stu-id="244bb-103">Msvm\_GuestService::StopService method</span></span>

<span data-ttu-id="244bb-104">停止來賓服務。</span><span class="sxs-lookup"><span data-stu-id="244bb-104">Stops the guest service.</span></span>

## <a name="syntax"></a><span data-ttu-id="244bb-105">語法</span><span class="sxs-lookup"><span data-stu-id="244bb-105">Syntax</span></span>


```C++
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="244bb-106">參數</span><span class="sxs-lookup"><span data-stu-id="244bb-106">Parameters</span></span>

<span data-ttu-id="244bb-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="244bb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="244bb-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="244bb-108">Return value</span></span>

<span data-ttu-id="244bb-109">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="244bb-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="244bb-110">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="244bb-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="244bb-111">Description</span><span class="sxs-lookup"><span data-stu-id="244bb-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="244bb-112"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="244bb-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="244bb-113">成功。</span><span class="sxs-lookup"><span data-stu-id="244bb-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="244bb-114"><dt>**不支援**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="244bb-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="244bb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="244bb-115">Requirements</span></span>



| <span data-ttu-id="244bb-116">需求</span><span class="sxs-lookup"><span data-stu-id="244bb-116">Requirement</span></span> | <span data-ttu-id="244bb-117">值</span><span class="sxs-lookup"><span data-stu-id="244bb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bb-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="244bb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="244bb-119">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="244bb-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="244bb-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="244bb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="244bb-121">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="244bb-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="244bb-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="244bb-122">Namespace</span></span><br/>                | <span data-ttu-id="244bb-123">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="244bb-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="244bb-124">MOF</span><span class="sxs-lookup"><span data-stu-id="244bb-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="244bb-125"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="244bb-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="244bb-126">DLL</span><span class="sxs-lookup"><span data-stu-id="244bb-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="244bb-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="244bb-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="244bb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="244bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="244bb-129">**Msvm \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="244bb-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




