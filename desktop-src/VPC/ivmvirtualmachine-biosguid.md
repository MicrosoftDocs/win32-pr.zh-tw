---
title: 'IVMVirtualMachine BIOSGUID 屬性 (VPCCOMInterfaces .h) '
description: BIOS GUID。
ms.assetid: d866838d-31e9-41f1-be57-43e778b9db95
keywords:
- BIOSGUID 屬性 Virtual PC
- BIOSGUID 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，BIOSGUID 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSGUID
- IVMVirtualMachine.get_BIOSGUID
- IVMVirtualMachine.put_BIOSGUID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10263e32ab71c2a5b9533b3dde6547f774d6b302
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843511"
---
# <a name="ivmvirtualmachinebiosguid-property"></a><span data-ttu-id="80b3e-106">IVMVirtualMachine：： BIOSGUID 屬性</span><span class="sxs-lookup"><span data-stu-id="80b3e-106">IVMVirtualMachine::BIOSGUID property</span></span>

<span data-ttu-id="80b3e-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="80b3e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="80b3e-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="80b3e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="80b3e-109">抓取並設定 BIOS GUID。</span><span class="sxs-lookup"><span data-stu-id="80b3e-109">Retrieves and sets the BIOS GUID.</span></span>

<span data-ttu-id="80b3e-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="80b3e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="80b3e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="80b3e-111">Syntax</span></span>


```C++
HRESULT put_BIOSGUID(
  [in]          BSTR biosGUID
);

HRESULT get_BIOSGUID(
  [out, retval] BSTR *biosGUID
);
```



## <a name="property-value"></a><span data-ttu-id="80b3e-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="80b3e-112">Property value</span></span>

<span data-ttu-id="80b3e-113">指定 BIOS GUID。</span><span class="sxs-lookup"><span data-stu-id="80b3e-113">Specifies the BIOS GUID.</span></span> <span data-ttu-id="80b3e-114">在十六進位數位前後加上左和右大括弧。</span><span class="sxs-lookup"><span data-stu-id="80b3e-114">Include left and right braces around the hex digits.</span></span>

## <a name="error-codes"></a><span data-ttu-id="80b3e-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="80b3e-115">Error codes</span></span>



| <span data-ttu-id="80b3e-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="80b3e-116">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="80b3e-117">意義</span><span class="sxs-lookup"><span data-stu-id="80b3e-117">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="80b3e-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="80b3e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="80b3e-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="80b3e-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="80b3e-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="80b3e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="80b3e-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="80b3e-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="80b3e-122"><dt>E \_INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="80b3e-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="80b3e-123">參數無效或為空字串。</span><span class="sxs-lookup"><span data-stu-id="80b3e-123">The parameter is not valid or is an empty string.</span></span><br/>   |
| <dl> <span data-ttu-id="80b3e-124"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="80b3e-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="80b3e-125">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="80b3e-125">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="80b3e-126"><dt>VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="80b3e-126"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="80b3e-127">虛擬機器處於執行中或已儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="80b3e-127">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="80b3e-128"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="80b3e-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="80b3e-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="80b3e-129">An unexpected error has occurred.</span></span><br/>                   |



## <a name="remarks"></a><span data-ttu-id="80b3e-130">備註</span><span class="sxs-lookup"><span data-stu-id="80b3e-130">Remarks</span></span>

<span data-ttu-id="80b3e-131">在虛擬機器第一次啟動之後，此屬性才會包含有效的資訊。</span><span class="sxs-lookup"><span data-stu-id="80b3e-131">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="80b3e-132">如果在初始啟動之前讀取了空字串，則會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="80b3e-132">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="80b3e-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="80b3e-133">Requirements</span></span>



| <span data-ttu-id="80b3e-134">需求</span><span class="sxs-lookup"><span data-stu-id="80b3e-134">Requirement</span></span> | <span data-ttu-id="80b3e-135">值</span><span class="sxs-lookup"><span data-stu-id="80b3e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b3e-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80b3e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="80b3e-137">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80b3e-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80b3e-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80b3e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="80b3e-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="80b3e-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="80b3e-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="80b3e-140">End of client support</span></span><br/>    | <span data-ttu-id="80b3e-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="80b3e-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="80b3e-142">產品</span><span class="sxs-lookup"><span data-stu-id="80b3e-142">Product</span></span><br/>                  | <span data-ttu-id="80b3e-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="80b3e-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="80b3e-144">標頭</span><span class="sxs-lookup"><span data-stu-id="80b3e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="80b3e-145"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="80b3e-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="80b3e-146">IID</span><span class="sxs-lookup"><span data-stu-id="80b3e-146">IID</span></span><br/>                      | <span data-ttu-id="80b3e-147">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="80b3e-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="80b3e-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80b3e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b3e-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="80b3e-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

