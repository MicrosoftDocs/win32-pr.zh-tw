---
title: 'IVMVirtualMachineEvents OnAdditionsUninstalled 方法 (VPCCOMInterfaces .h) '
description: 接收在虛擬機器中卸載整合元件的通知。
ms.assetid: bbbc01b6-adb1-491e-a5b0-ff463dca7dfd
keywords:
- OnAdditionsUninstalled 方法 Virtual PC
- OnAdditionsUninstalled 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnAdditionsUninstalled 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsUninstalled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 514a88249ad34d51965df75feab6f129bd9fa5a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093748"
---
# <a name="ivmvirtualmachineeventsonadditionsuninstalled-method"></a><span data-ttu-id="429cc-106">IVMVirtualMachineEvents：： OnAdditionsUninstalled 方法</span><span class="sxs-lookup"><span data-stu-id="429cc-106">IVMVirtualMachineEvents::OnAdditionsUninstalled method</span></span>

<span data-ttu-id="429cc-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="429cc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="429cc-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="429cc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="429cc-109">接收在虛擬機器中卸載整合元件的通知。</span><span class="sxs-lookup"><span data-stu-id="429cc-109">Receives notification that integration components are uninstalled in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="429cc-110">語法</span><span class="sxs-lookup"><span data-stu-id="429cc-110">Syntax</span></span>


```C++
HRESULT OnAdditionsUninstalled();
```



## <a name="parameters"></a><span data-ttu-id="429cc-111">參數</span><span class="sxs-lookup"><span data-stu-id="429cc-111">Parameters</span></span>

<span data-ttu-id="429cc-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="429cc-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="429cc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="429cc-113">Return value</span></span>

<span data-ttu-id="429cc-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="429cc-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="429cc-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="429cc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="429cc-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="429cc-116">Requirements</span></span>



| <span data-ttu-id="429cc-117">需求</span><span class="sxs-lookup"><span data-stu-id="429cc-117">Requirement</span></span> | <span data-ttu-id="429cc-118">值</span><span class="sxs-lookup"><span data-stu-id="429cc-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="429cc-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="429cc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="429cc-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="429cc-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="429cc-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="429cc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="429cc-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="429cc-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="429cc-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="429cc-123">End of client support</span></span><br/>    | <span data-ttu-id="429cc-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="429cc-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="429cc-125">產品</span><span class="sxs-lookup"><span data-stu-id="429cc-125">Product</span></span><br/>                  | <span data-ttu-id="429cc-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="429cc-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="429cc-127">標頭</span><span class="sxs-lookup"><span data-stu-id="429cc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="429cc-128"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="429cc-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="429cc-129">IID</span><span class="sxs-lookup"><span data-stu-id="429cc-129">IID</span></span><br/>                      | <span data-ttu-id="429cc-130">DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="429cc-130">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="429cc-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="429cc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="429cc-132">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="429cc-132">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

