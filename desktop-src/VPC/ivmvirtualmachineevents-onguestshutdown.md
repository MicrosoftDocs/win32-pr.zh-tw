---
title: 'IVMVirtualMachineEvents OnGuestShutdown 方法 (VPCCOMInterfaces .h) '
description: 收到客體作業系統關機的通知。
ms.assetid: a70c746a-f1ce-4f93-b41b-b03dc83f3da2
keywords:
- OnGuestShutdown 方法 Virtual PC
- OnGuestShutdown 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnGuestShutdown 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481b6dd6e13dc17d7f9a22ef366e984c2663279c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509100"
---
# <a name="ivmvirtualmachineeventsonguestshutdown-method"></a><span data-ttu-id="7d4fa-106">IVMVirtualMachineEvents：： OnGuestShutdown 方法</span><span class="sxs-lookup"><span data-stu-id="7d4fa-106">IVMVirtualMachineEvents::OnGuestShutdown method</span></span>

<span data-ttu-id="7d4fa-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="7d4fa-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7d4fa-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="7d4fa-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7d4fa-109">收到客體作業系統關機的通知。</span><span class="sxs-lookup"><span data-stu-id="7d4fa-109">Receives notification that guest operating system shuts down.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d4fa-110">語法</span><span class="sxs-lookup"><span data-stu-id="7d4fa-110">Syntax</span></span>


```C++
HRESULT OnGuestShutdown();
```



## <a name="parameters"></a><span data-ttu-id="7d4fa-111">參數</span><span class="sxs-lookup"><span data-stu-id="7d4fa-111">Parameters</span></span>

<span data-ttu-id="7d4fa-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7d4fa-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d4fa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d4fa-113">Return value</span></span>

<span data-ttu-id="7d4fa-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="7d4fa-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7d4fa-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7d4fa-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d4fa-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d4fa-116">Requirements</span></span>



| <span data-ttu-id="7d4fa-117">需求</span><span class="sxs-lookup"><span data-stu-id="7d4fa-117">Requirement</span></span> | <span data-ttu-id="7d4fa-118">值</span><span class="sxs-lookup"><span data-stu-id="7d4fa-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d4fa-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d4fa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7d4fa-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d4fa-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d4fa-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d4fa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7d4fa-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="7d4fa-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7d4fa-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7d4fa-123">End of client support</span></span><br/>    | <span data-ttu-id="7d4fa-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d4fa-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7d4fa-125">產品</span><span class="sxs-lookup"><span data-stu-id="7d4fa-125">Product</span></span><br/>                  | <span data-ttu-id="7d4fa-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7d4fa-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7d4fa-127">標頭</span><span class="sxs-lookup"><span data-stu-id="7d4fa-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d4fa-128"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d4fa-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7d4fa-129">IID</span><span class="sxs-lookup"><span data-stu-id="7d4fa-129">IID</span></span><br/>                      | <span data-ttu-id="7d4fa-130">DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="7d4fa-130">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="7d4fa-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d4fa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d4fa-132">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="7d4fa-132">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

