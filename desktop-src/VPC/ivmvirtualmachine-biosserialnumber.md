---
title: 'IVMVirtualMachine BIOSSerialNumber 屬性 (VPCCOMInterfaces .h) '
description: BIOS 序號。
ms.assetid: a105009d-1c44-4079-a7d4-103cb02bad71
keywords:
- BIOSSerialNumber 屬性 Virtual PC
- BIOSSerialNumber 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，BIOSSerialNumber 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSSerialNumber
- IVMVirtualMachine.get_BIOSSerialNumber
- IVMVirtualMachine.put_BIOSSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8bd3f240d863a6f43dabbdb0a26429c4a77219
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025398"
---
# <a name="ivmvirtualmachinebiosserialnumber-property"></a><span data-ttu-id="86b6f-106">IVMVirtualMachine：： BIOSSerialNumber 屬性</span><span class="sxs-lookup"><span data-stu-id="86b6f-106">IVMVirtualMachine::BIOSSerialNumber property</span></span>

<span data-ttu-id="86b6f-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="86b6f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="86b6f-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="86b6f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="86b6f-109">捕獲並設定 BIOS 序號。</span><span class="sxs-lookup"><span data-stu-id="86b6f-109">Retrieves and sets the BIOS serial number.</span></span>

<span data-ttu-id="86b6f-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="86b6f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="86b6f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="86b6f-111">Syntax</span></span>


```C++
HRESULT put_BIOSSerialNumber(
  [in]          BSTR biosSerialNumber
);

HRESULT get_BIOSSerialNumber(
  [out, retval] BSTR *biosSerialNumber
);
```



## <a name="property-value"></a><span data-ttu-id="86b6f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="86b6f-112">Property value</span></span>

<span data-ttu-id="86b6f-113">指定 BIOS 序號。</span><span class="sxs-lookup"><span data-stu-id="86b6f-113">Specifies the BIOS serial number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="86b6f-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="86b6f-114">Error codes</span></span>



| <span data-ttu-id="86b6f-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="86b6f-115">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="86b6f-116">意義</span><span class="sxs-lookup"><span data-stu-id="86b6f-116">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86b6f-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="86b6f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="86b6f-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="86b6f-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="86b6f-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="86b6f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="86b6f-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="86b6f-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="86b6f-121"><dt>E \_INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="86b6f-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="86b6f-122">參數大於32個字元、空字串或無效。</span><span class="sxs-lookup"><span data-stu-id="86b6f-122">The parameter is greater than 32 characters, an empty string, or not valid.</span></span><br/> |
| <dl> <span data-ttu-id="86b6f-123"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="86b6f-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="86b6f-124">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="86b6f-124">The configuration is unknown.</span></span><br/>                                               |
| <dl> <span data-ttu-id="86b6f-125"><dt>VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="86b6f-125"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="86b6f-126">虛擬機器處於執行中或已儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="86b6f-126">The virtual machine is in a running or saved state.</span></span><br/>                         |
| <dl> <span data-ttu-id="86b6f-127"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="86b6f-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="86b6f-128">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="86b6f-128">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="remarks"></a><span data-ttu-id="86b6f-129">備註</span><span class="sxs-lookup"><span data-stu-id="86b6f-129">Remarks</span></span>

<span data-ttu-id="86b6f-130">在虛擬機器第一次啟動之後，此屬性才會包含有效的資訊。</span><span class="sxs-lookup"><span data-stu-id="86b6f-130">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="86b6f-131">如果在初始啟動之前讀取了空字串，則會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="86b6f-131">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="86b6f-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="86b6f-132">Requirements</span></span>



| <span data-ttu-id="86b6f-133">需求</span><span class="sxs-lookup"><span data-stu-id="86b6f-133">Requirement</span></span> | <span data-ttu-id="86b6f-134">值</span><span class="sxs-lookup"><span data-stu-id="86b6f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="86b6f-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86b6f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="86b6f-136">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86b6f-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86b6f-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86b6f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="86b6f-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="86b6f-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="86b6f-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="86b6f-139">End of client support</span></span><br/>    | <span data-ttu-id="86b6f-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="86b6f-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="86b6f-141">產品</span><span class="sxs-lookup"><span data-stu-id="86b6f-141">Product</span></span><br/>                  | <span data-ttu-id="86b6f-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="86b6f-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="86b6f-143">標頭</span><span class="sxs-lookup"><span data-stu-id="86b6f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="86b6f-144"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="86b6f-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="86b6f-145">IID</span><span class="sxs-lookup"><span data-stu-id="86b6f-145">IID</span></span><br/>                      | <span data-ttu-id="86b6f-146">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="86b6f-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="86b6f-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86b6f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b6f-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="86b6f-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

