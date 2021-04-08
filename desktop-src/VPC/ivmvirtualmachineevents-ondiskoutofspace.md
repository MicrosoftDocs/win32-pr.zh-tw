---
title: 'IVMVirtualMachineEvents OnDiskOutOfSpace 方法 (VPCCOMInterfaces .h) '
description: 接收 VM 所需磁片的可用空間不足的通知。
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- OnDiskOutOfSpace 方法 Virtual PC
- OnDiskOutOfSpace 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnDiskOutOfSpace 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac2d5f45068dc8cd7341d0a599b2da4e5c7655a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843035"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a><span data-ttu-id="ab179-106">IVMVirtualMachineEvents：： OnDiskOutOfSpace 方法</span><span class="sxs-lookup"><span data-stu-id="ab179-106">IVMVirtualMachineEvents::OnDiskOutOfSpace method</span></span>

<span data-ttu-id="ab179-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="ab179-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ab179-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="ab179-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ab179-109">收到通知，表示虛擬機器 (VM) 所需磁片的可用空間不足。</span><span class="sxs-lookup"><span data-stu-id="ab179-109">Receives notification that a disk required for a virtual machine (VM) is low on free space.</span></span> <span data-ttu-id="ab179-110">如果可用空間低於 100 MB，則會以警告的形式接收此事件，如果可用空間低於 20 MB，則會再次收到此事件作為錯誤，VM 將會暫停。</span><span class="sxs-lookup"><span data-stu-id="ab179-110">If free space drops below 100 MB this event is received as a warning and if free space drops below 20 MB this event is received again as an error and the VM will be paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab179-111">語法</span><span class="sxs-lookup"><span data-stu-id="ab179-111">Syntax</span></span>


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a><span data-ttu-id="ab179-112">參數</span><span class="sxs-lookup"><span data-stu-id="ab179-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab179-113">*criticallyLow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab179-113">*criticallyLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab179-114">如果磁片的可用空間小於 20 mb，則設定為 **variant \_ TRUE** ，如果可用空間超過 20 mb 但小於 100 mb，則設定為 **variant \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ab179-114">Set to **VARIANT\_TRUE** if the disk has less than 20 MB free and to **VARIANT\_FALSE** if the free space is more than 20 MB but less than 100 MB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab179-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab179-115">Return value</span></span>

<span data-ttu-id="ab179-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ab179-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab179-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ab179-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab179-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab179-118">Requirements</span></span>



| <span data-ttu-id="ab179-119">需求</span><span class="sxs-lookup"><span data-stu-id="ab179-119">Requirement</span></span> | <span data-ttu-id="ab179-120">值</span><span class="sxs-lookup"><span data-stu-id="ab179-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab179-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab179-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ab179-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab179-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab179-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab179-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ab179-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="ab179-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ab179-125">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ab179-125">End of client support</span></span><br/>    | <span data-ttu-id="ab179-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ab179-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ab179-127">產品</span><span class="sxs-lookup"><span data-stu-id="ab179-127">Product</span></span><br/>                  | <span data-ttu-id="ab179-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ab179-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ab179-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ab179-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab179-130"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab179-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ab179-131">IID</span><span class="sxs-lookup"><span data-stu-id="ab179-131">IID</span></span><br/>                      | <span data-ttu-id="ab179-132">DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="ab179-132">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="ab179-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab179-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab179-134">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="ab179-134">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

