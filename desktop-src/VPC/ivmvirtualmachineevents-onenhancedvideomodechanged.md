---
title: 'IVMVirtualMachineEvents OnEnhancedVideoModeChanged 方法 (VPCCOMInterfaces .h) '
description: 收到虛擬機器的增強型影片模式支援已變更的通知。
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- OnEnhancedVideoModeChanged 方法 Virtual PC
- OnEnhancedVideoModeChanged 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnEnhancedVideoModeChanged 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bbc67fe298c1a47d853072d8c58ab5b3ce1988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464181"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a><span data-ttu-id="f18f5-106">IVMVirtualMachineEvents：： OnEnhancedVideoModeChanged 方法</span><span class="sxs-lookup"><span data-stu-id="f18f5-106">IVMVirtualMachineEvents::OnEnhancedVideoModeChanged method</span></span>

<span data-ttu-id="f18f5-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="f18f5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f18f5-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="f18f5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f18f5-109">收到虛擬機器的增強型影片模式支援已變更的通知。</span><span class="sxs-lookup"><span data-stu-id="f18f5-109">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f18f5-110">語法</span><span class="sxs-lookup"><span data-stu-id="f18f5-110">Syntax</span></span>


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a><span data-ttu-id="f18f5-111">參數</span><span class="sxs-lookup"><span data-stu-id="f18f5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f18f5-112">*enhancedVideoMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f18f5-112">*enhancedVideoMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f18f5-113">指出是否有增強的影片模式可用。</span><span class="sxs-lookup"><span data-stu-id="f18f5-113">Indicates whether enhanced video mode is available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f18f5-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f18f5-114">Return value</span></span>

<span data-ttu-id="f18f5-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f18f5-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f18f5-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f18f5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f18f5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f18f5-117">Requirements</span></span>



| <span data-ttu-id="f18f5-118">需求</span><span class="sxs-lookup"><span data-stu-id="f18f5-118">Requirement</span></span> | <span data-ttu-id="f18f5-119">值</span><span class="sxs-lookup"><span data-stu-id="f18f5-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f18f5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f18f5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f18f5-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f18f5-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f18f5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f18f5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f18f5-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="f18f5-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f18f5-124">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f18f5-124">End of client support</span></span><br/>    | <span data-ttu-id="f18f5-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f18f5-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f18f5-126">產品</span><span class="sxs-lookup"><span data-stu-id="f18f5-126">Product</span></span><br/>                  | <span data-ttu-id="f18f5-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f18f5-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f18f5-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f18f5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f18f5-129"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="f18f5-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f18f5-130">IID</span><span class="sxs-lookup"><span data-stu-id="f18f5-130">IID</span></span><br/>                      | <span data-ttu-id="f18f5-131">DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="f18f5-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="f18f5-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f18f5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f18f5-133">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="f18f5-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

