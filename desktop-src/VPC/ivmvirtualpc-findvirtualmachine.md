---
title: 'IVMVirtualPC FindVirtualMachine 方法 (VPCCOMInterfaces .h) '
description: 抓取符合所要求設定的虛擬機器物件。
ms.assetid: 1c73d6f7-5662-485e-a864-e8e48197f8e4
keywords:
- FindVirtualMachine 方法 Virtual PC
- FindVirtualMachine 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，FindVirtualMachine 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e5702738e16fa7b4f4a263264b0574966d1fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105203"
---
# <a name="ivmvirtualpcfindvirtualmachine-method"></a><span data-ttu-id="4bd9e-106">IVMVirtualPC：： FindVirtualMachine 方法</span><span class="sxs-lookup"><span data-stu-id="4bd9e-106">IVMVirtualPC::FindVirtualMachine method</span></span>

<span data-ttu-id="4bd9e-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="4bd9e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4bd9e-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="4bd9e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4bd9e-109">抓取符合所要求設定的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="4bd9e-109">Retrieves a virtual machine object that matches the requested configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bd9e-110">語法</span><span class="sxs-lookup"><span data-stu-id="4bd9e-110">Syntax</span></span>


```C++
HRESULT FindVirtualMachine(
  [in]          BSTR              configurationName,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="4bd9e-111">參數</span><span class="sxs-lookup"><span data-stu-id="4bd9e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bd9e-112">*configurationName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bd9e-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bd9e-113">要尋找之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bd9e-113">The name of the virtual machine to be found.</span></span>

</dd> <dt>

<span data-ttu-id="4bd9e-114">*virtualMachine* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="4bd9e-114">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4bd9e-115">代表此虛擬機器的新 [**IVMVirtualMachine**](ivmvirtualmachine.md) 物件指標。</span><span class="sxs-lookup"><span data-stu-id="4bd9e-115">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bd9e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bd9e-116">Return value</span></span>

<span data-ttu-id="4bd9e-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4bd9e-117">This method can return one of these values.</span></span>



| <span data-ttu-id="4bd9e-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="4bd9e-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="4bd9e-119">Description</span><span class="sxs-lookup"><span data-stu-id="4bd9e-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4bd9e-120"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4bd9e-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="4bd9e-121">作業成功。</span><span class="sxs-lookup"><span data-stu-id="4bd9e-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4bd9e-122"><dt>**S \_FALSE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4bd9e-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="4bd9e-123">找不到指定的設定。</span><span class="sxs-lookup"><span data-stu-id="4bd9e-123">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="4bd9e-124"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4bd9e-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="4bd9e-125">*ConfigurationName* 參數無效，或 *virtualMachine* 為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4bd9e-125">The *configurationName* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="4bd9e-126"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4bd9e-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="4bd9e-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4bd9e-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="4bd9e-128"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="4bd9e-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="4bd9e-129">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="4bd9e-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4bd9e-130">備註</span><span class="sxs-lookup"><span data-stu-id="4bd9e-130">Remarks</span></span>

<span data-ttu-id="4bd9e-131">虛擬機器名稱不區分大小寫，例如 "MyVM" 和 "MyVM" 指的是相同的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4bd9e-131">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bd9e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bd9e-132">Requirements</span></span>



| <span data-ttu-id="4bd9e-133">需求</span><span class="sxs-lookup"><span data-stu-id="4bd9e-133">Requirement</span></span> | <span data-ttu-id="4bd9e-134">值</span><span class="sxs-lookup"><span data-stu-id="4bd9e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd9e-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bd9e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4bd9e-136">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bd9e-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4bd9e-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bd9e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4bd9e-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="4bd9e-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4bd9e-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4bd9e-139">End of client support</span></span><br/>    | <span data-ttu-id="4bd9e-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4bd9e-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4bd9e-141">產品</span><span class="sxs-lookup"><span data-stu-id="4bd9e-141">Product</span></span><br/>                  | <span data-ttu-id="4bd9e-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4bd9e-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4bd9e-143">標頭</span><span class="sxs-lookup"><span data-stu-id="4bd9e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bd9e-144"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="4bd9e-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4bd9e-145">IID</span><span class="sxs-lookup"><span data-stu-id="4bd9e-145">IID</span></span><br/>                      | <span data-ttu-id="4bd9e-146">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="4bd9e-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4bd9e-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bd9e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bd9e-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="4bd9e-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

