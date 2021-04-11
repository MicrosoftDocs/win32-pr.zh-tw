---
title: 'IVMKeyboard HasExclusiveAccess 屬性 (VPCCOMInterfaces .h) '
description: 指出此物件是否具有 VM 鍵盤裝置的獨佔控制。
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- HasExclusiveAccess 屬性 Virtual PC
- HasExclusiveAccess 屬性 Virtual PC，IVMKeyboard 介面
- IVMKeyboard 介面 Virtual PC，HasExclusiveAccess 屬性
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62c235f3b4325a70a939239ac1e44360b3b5d9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105678"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a><span data-ttu-id="cfded-106">IVMKeyboard：： HasExclusiveAccess 屬性</span><span class="sxs-lookup"><span data-stu-id="cfded-106">IVMKeyboard::HasExclusiveAccess property</span></span>

<span data-ttu-id="cfded-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="cfded-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cfded-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="cfded-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cfded-109">指出此物件是否有虛擬機器 (VM) 鍵盤裝置的獨佔控制。</span><span class="sxs-lookup"><span data-stu-id="cfded-109">Indicates whether this object has exclusive control over the virtual machine's (VM) keyboard device.</span></span>

<span data-ttu-id="cfded-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="cfded-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfded-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfded-111">Syntax</span></span>


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a><span data-ttu-id="cfded-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="cfded-112">Property value</span></span>

<span data-ttu-id="cfded-113">如果已取得對 VM 鍵盤裝置的獨佔存取權，**則為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="cfded-113">**TRUE** if exclusive access to the VM's keyboard device has been acquired, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cfded-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="cfded-114">Error codes</span></span>



| <span data-ttu-id="cfded-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="cfded-115">Name/value</span></span>                                                                                                                                                                   | <span data-ttu-id="cfded-116">意義</span><span class="sxs-lookup"><span data-stu-id="cfded-116">Meaning</span></span>                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cfded-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cfded-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                      | <span data-ttu-id="cfded-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="cfded-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="cfded-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cfded-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                        | <span data-ttu-id="cfded-120">*IsExclusive* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cfded-120">The *isExclusive* parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="cfded-121"><dt>S \_FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cfded-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                   | <span data-ttu-id="cfded-122">已為此裝置設定要求的獨佔模式。</span><span class="sxs-lookup"><span data-stu-id="cfded-122">The requested exclusive mode is already set for this device.</span></span> <span data-ttu-id="cfded-123">當您嘗試在取得獨佔模式時，或在先前未取得時嘗試釋放獨佔模式時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="cfded-123">This can happen when trying to set exclusive mode when it has already been acquired, or when trying to release exclusive mode when it had not been previously acquired.</span></span><br/> |
| <dl> <span data-ttu-id="cfded-124"><dt>VM \_E \_ 設定 \_ 獨佔 \_ 模式 \_ 失敗</dt> <dt>0xA0040825</dt></span><span class="sxs-lookup"><span data-stu-id="cfded-124"><dt>VM\_E\_SET\_EXCLUSIVE\_MODE\_FAIL</dt> <dt>0xA0040825</dt></span></span> </dl> | <span data-ttu-id="cfded-125">無法依要求設定或發行獨佔模式。</span><span class="sxs-lookup"><span data-stu-id="cfded-125">Failed to set or release exclusive mode as requested.</span></span> <span data-ttu-id="cfded-126">這可能是因為 VM 已不再執行，或因為另一個進程已在 VM 的鍵盤裝置上取得獨佔模式。</span><span class="sxs-lookup"><span data-stu-id="cfded-126">This could be because the VM is no longer running, or because another process has already acquired exclusive mode on the VM's keyboard device.</span></span><br/>                                 |
| <dl> <span data-ttu-id="cfded-127"><dt>E \_INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="cfded-127"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                     | <span data-ttu-id="cfded-128">指定的字串是空的，或包含不正確按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="cfded-128">The specified string is empty, or contains an invalid key code.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="cfded-129"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cfded-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                | <span data-ttu-id="cfded-130">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cfded-130">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="cfded-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfded-131">Requirements</span></span>



| <span data-ttu-id="cfded-132">需求</span><span class="sxs-lookup"><span data-stu-id="cfded-132">Requirement</span></span> | <span data-ttu-id="cfded-133">值</span><span class="sxs-lookup"><span data-stu-id="cfded-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfded-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfded-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cfded-135">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfded-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cfded-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfded-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cfded-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="cfded-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cfded-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="cfded-138">End of client support</span></span><br/>    | <span data-ttu-id="cfded-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cfded-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cfded-140">產品</span><span class="sxs-lookup"><span data-stu-id="cfded-140">Product</span></span><br/>                  | <span data-ttu-id="cfded-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cfded-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cfded-142">標頭</span><span class="sxs-lookup"><span data-stu-id="cfded-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfded-143"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="cfded-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cfded-144">IID</span><span class="sxs-lookup"><span data-stu-id="cfded-144">IID</span></span><br/>                      | <span data-ttu-id="cfded-145">IID \_ IVMKeyboard 定義為00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="cfded-145">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="cfded-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfded-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfded-147">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="cfded-147">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

