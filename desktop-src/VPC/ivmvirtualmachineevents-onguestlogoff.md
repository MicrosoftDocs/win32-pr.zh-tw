---
title: 'IVMVirtualMachineEvents OnGuestLogoff 方法 (VPCCOMInterfaces .h) '
description: 接收使用者已從客體作業系統登出的通知。
ms.assetid: 3771ba28-eea9-4c8b-9224-231b00d2f2f5
keywords:
- OnGuestLogoff 方法 Virtual PC
- OnGuestLogoff 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnGuestLogoff 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestLogoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce5100c3901b3de32a769b6bae0e16fcffe26a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933876"
---
# <a name="ivmvirtualmachineeventsonguestlogoff-method"></a><span data-ttu-id="86bc2-106">IVMVirtualMachineEvents：： OnGuestLogoff 方法</span><span class="sxs-lookup"><span data-stu-id="86bc2-106">IVMVirtualMachineEvents::OnGuestLogoff method</span></span>

<span data-ttu-id="86bc2-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="86bc2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="86bc2-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="86bc2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="86bc2-109">接收使用者已從客體作業系統登出的通知。</span><span class="sxs-lookup"><span data-stu-id="86bc2-109">Receives notification that a user has logged off from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="86bc2-110">語法</span><span class="sxs-lookup"><span data-stu-id="86bc2-110">Syntax</span></span>


```C++
HRESULT OnGuestLogoff(
  [in] VMLogoffType logoffType
);
```



## <a name="parameters"></a><span data-ttu-id="86bc2-111">參數</span><span class="sxs-lookup"><span data-stu-id="86bc2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86bc2-112">*logoffType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86bc2-112">*logoffType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86bc2-113">描述登出類型之 [**VMLogoffType**](vmlogofftype.md) 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="86bc2-113">Value from the [**VMLogoffType**](vmlogofftype.md) enumeration that describes the type of logoff.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86bc2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="86bc2-114">Return value</span></span>

<span data-ttu-id="86bc2-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="86bc2-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="86bc2-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="86bc2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="86bc2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="86bc2-117">Requirements</span></span>



| <span data-ttu-id="86bc2-118">需求</span><span class="sxs-lookup"><span data-stu-id="86bc2-118">Requirement</span></span> | <span data-ttu-id="86bc2-119">值</span><span class="sxs-lookup"><span data-stu-id="86bc2-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="86bc2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86bc2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="86bc2-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86bc2-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86bc2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86bc2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="86bc2-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="86bc2-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="86bc2-124">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="86bc2-124">End of client support</span></span><br/>    | <span data-ttu-id="86bc2-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="86bc2-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="86bc2-126">產品</span><span class="sxs-lookup"><span data-stu-id="86bc2-126">Product</span></span><br/>                  | <span data-ttu-id="86bc2-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="86bc2-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="86bc2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="86bc2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="86bc2-129"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="86bc2-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="86bc2-130">IID</span><span class="sxs-lookup"><span data-stu-id="86bc2-130">IID</span></span><br/>                      | <span data-ttu-id="86bc2-131">DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="86bc2-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="86bc2-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86bc2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86bc2-133">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="86bc2-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> <dt>

[<span data-ttu-id="86bc2-134">**VMLogoffType**</span><span class="sxs-lookup"><span data-stu-id="86bc2-134">**VMLogoffType**</span></span>](vmlogofftype.md)
</dt> </dl>

 

