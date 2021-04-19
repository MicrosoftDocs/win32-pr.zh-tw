---
description: 將非遮罩式插斷插入虛擬機器中。
ms.assetid: 897AD1B9-0EDD-4DCE-963D-D5DE03AF55A9
title: Msvm_ComputerSystem：： InjectNonMaskableInterrupt 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.InjectNonMaskableInterrupt
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5798079a8866d9fb67356adff43c0ac1e993e6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973227"
---
# <a name="msvm_computersysteminjectnonmaskableinterrupt-method"></a><span data-ttu-id="455cd-103">Msvm \_ ：： InjectNonMaskableInterrupt 方法</span><span class="sxs-lookup"><span data-stu-id="455cd-103">Msvm\_ComputerSystem::InjectNonMaskableInterrupt method</span></span>

<span data-ttu-id="455cd-104">將非遮罩式插斷插入虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="455cd-104">Injects a non-maskable interrupt into the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="455cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="455cd-105">Syntax</span></span>


```C++
uint32 InjectNonMaskableInterrupt(
  [out] CIM_ConcreteJob Job
);
```



## <a name="parameters"></a><span data-ttu-id="455cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="455cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="455cd-107">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="455cd-107">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="455cd-108">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) 之物件的參考，以追蹤中斷插入的狀態。</span><span class="sxs-lookup"><span data-stu-id="455cd-108">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) to track the status of the interrupt injection.</span></span> <span data-ttu-id="455cd-109">如果工作已完成，此參考可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="455cd-109">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="455cd-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="455cd-110">Return value</span></span>

<span data-ttu-id="455cd-111">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="455cd-111">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="455cd-112">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="455cd-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="455cd-113">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="455cd-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="455cd-114">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="455cd-114">**Access Denied** (32769)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="455cd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="455cd-115">Requirements</span></span>



| <span data-ttu-id="455cd-116">需求</span><span class="sxs-lookup"><span data-stu-id="455cd-116">Requirement</span></span> | <span data-ttu-id="455cd-117">值</span><span class="sxs-lookup"><span data-stu-id="455cd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="455cd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="455cd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="455cd-119">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="455cd-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="455cd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="455cd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="455cd-121">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="455cd-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="455cd-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="455cd-122">Namespace</span></span><br/>                | <span data-ttu-id="455cd-123">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="455cd-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="455cd-124">MOF</span><span class="sxs-lookup"><span data-stu-id="455cd-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="455cd-125"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="455cd-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="455cd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="455cd-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="455cd-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="455cd-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="455cd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="455cd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="455cd-129">**Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="455cd-129">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

