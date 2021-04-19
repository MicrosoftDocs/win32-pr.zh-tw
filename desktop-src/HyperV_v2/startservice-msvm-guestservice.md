---
description: 將來賓服務置於啟動狀態。
ms.assetid: 1DC6A5B3-0F91-4AC1-99D5-0E8CF5ED35A2
title: Msvm_GuestService：： StartService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1a87bc9933bd7b3a54bd59169b0099e34eb04c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985508"
---
# <a name="msvm_guestservicestartservice-method"></a><span data-ttu-id="922a7-103">Msvm \_ GuestService：： StartService 方法</span><span class="sxs-lookup"><span data-stu-id="922a7-103">Msvm\_GuestService::StartService method</span></span>

<span data-ttu-id="922a7-104">將來賓服務置於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="922a7-104">Puts the guest service in a started state.</span></span>

## <a name="syntax"></a><span data-ttu-id="922a7-105">語法</span><span class="sxs-lookup"><span data-stu-id="922a7-105">Syntax</span></span>


```C++
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="922a7-106">參數</span><span class="sxs-lookup"><span data-stu-id="922a7-106">Parameters</span></span>

<span data-ttu-id="922a7-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="922a7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="922a7-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="922a7-108">Return value</span></span>

<span data-ttu-id="922a7-109">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="922a7-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="922a7-110">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="922a7-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="922a7-111">Description</span><span class="sxs-lookup"><span data-stu-id="922a7-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="922a7-112"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="922a7-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="922a7-113">成功。</span><span class="sxs-lookup"><span data-stu-id="922a7-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="922a7-114"><dt>**不支援**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="922a7-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="922a7-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="922a7-115">Requirements</span></span>



| <span data-ttu-id="922a7-116">需求</span><span class="sxs-lookup"><span data-stu-id="922a7-116">Requirement</span></span> | <span data-ttu-id="922a7-117">值</span><span class="sxs-lookup"><span data-stu-id="922a7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="922a7-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="922a7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="922a7-119">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="922a7-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="922a7-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="922a7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="922a7-121">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="922a7-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="922a7-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="922a7-122">Namespace</span></span><br/>                | <span data-ttu-id="922a7-123">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="922a7-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="922a7-124">MOF</span><span class="sxs-lookup"><span data-stu-id="922a7-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="922a7-125"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="922a7-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="922a7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="922a7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="922a7-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="922a7-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="922a7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="922a7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="922a7-129">**Msvm \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="922a7-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




