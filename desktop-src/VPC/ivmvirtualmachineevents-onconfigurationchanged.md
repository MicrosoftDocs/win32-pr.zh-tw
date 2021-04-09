---
title: 'IVMVirtualMachineEvents OnConfigurationChanged 方法 (VPCCOMInterfaces .h) '
description: 接收此虛擬機器設定中的值已變更的通知。
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- OnConfigurationChanged 方法 Virtual PC
- OnConfigurationChanged 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnConfigurationChanged 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10459562da2d87b8c883217e003cd822ef923fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933877"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a><span data-ttu-id="8bd21-106">IVMVirtualMachineEvents：： OnConfigurationChanged 方法</span><span class="sxs-lookup"><span data-stu-id="8bd21-106">IVMVirtualMachineEvents::OnConfigurationChanged method</span></span>

<span data-ttu-id="8bd21-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="8bd21-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8bd21-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="8bd21-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8bd21-109">接收此虛擬機器設定中的值已變更的通知。</span><span class="sxs-lookup"><span data-stu-id="8bd21-109">Receives notification that a value in the configuration for this virtual machine has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bd21-110">語法</span><span class="sxs-lookup"><span data-stu-id="8bd21-110">Syntax</span></span>


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a><span data-ttu-id="8bd21-111">參數</span><span class="sxs-lookup"><span data-stu-id="8bd21-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bd21-112">*configKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8bd21-112">*configKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bd21-113">設定中已變更的值。</span><span class="sxs-lookup"><span data-stu-id="8bd21-113">The value inside the configuration that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="8bd21-114">*configData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8bd21-114">*configData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bd21-115">設定的新值。</span><span class="sxs-lookup"><span data-stu-id="8bd21-115">The new value for the configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bd21-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8bd21-116">Return value</span></span>

<span data-ttu-id="8bd21-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8bd21-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8bd21-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8bd21-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bd21-119">備註</span><span class="sxs-lookup"><span data-stu-id="8bd21-119">Remarks</span></span>

<span data-ttu-id="8bd21-120">此虛擬機器的設定變更時，會呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="8bd21-120">This method is called when the configuration changes for this virtual machine.</span></span> <span data-ttu-id="8bd21-121">用戶端程式必須執行這個介面方法，以接收來自 IVMVirtualMachine 的 vmVirtualMachineEvent \_ ConfigurationChanged 事件的[](ivmvirtualmachine.md)通知。</span><span class="sxs-lookup"><span data-stu-id="8bd21-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_ConfigurationChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bd21-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bd21-122">Requirements</span></span>



| <span data-ttu-id="8bd21-123">需求</span><span class="sxs-lookup"><span data-stu-id="8bd21-123">Requirement</span></span> | <span data-ttu-id="8bd21-124">值</span><span class="sxs-lookup"><span data-stu-id="8bd21-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd21-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8bd21-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8bd21-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bd21-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8bd21-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8bd21-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8bd21-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="8bd21-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8bd21-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8bd21-129">End of client support</span></span><br/>    | <span data-ttu-id="8bd21-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8bd21-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8bd21-131">產品</span><span class="sxs-lookup"><span data-stu-id="8bd21-131">Product</span></span><br/>                  | <span data-ttu-id="8bd21-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8bd21-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8bd21-133">標頭</span><span class="sxs-lookup"><span data-stu-id="8bd21-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bd21-134"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="8bd21-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8bd21-135">IID</span><span class="sxs-lookup"><span data-stu-id="8bd21-135">IID</span></span><br/>                      | <span data-ttu-id="8bd21-136">DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="8bd21-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="8bd21-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bd21-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bd21-138">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="8bd21-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

