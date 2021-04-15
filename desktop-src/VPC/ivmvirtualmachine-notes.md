---
title: 'IVMVirtualMachine Notes 屬性 (VPCCOMInterfaces .h) '
description: 虛擬機器的附注。
ms.assetid: 4be6842b-31b2-4619-a6ab-b728be1e2174
keywords:
- Notes 屬性虛擬電腦
- Notes 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine interface Virtual PC，Notes 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Notes
- IVMVirtualMachine.get_Notes
- IVMVirtualMachine.put_Notes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8fba8659a8f9546866129f21299e44006eb496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466617"
---
# <a name="ivmvirtualmachinenotes-property"></a><span data-ttu-id="56bed-106">IVMVirtualMachine：： Notes 屬性</span><span class="sxs-lookup"><span data-stu-id="56bed-106">IVMVirtualMachine::Notes property</span></span>

<span data-ttu-id="56bed-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="56bed-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="56bed-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="56bed-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="56bed-109">抓取和設定虛擬機器的附注。</span><span class="sxs-lookup"><span data-stu-id="56bed-109">Retrieves and sets the notes for the virtual machine.</span></span>

<span data-ttu-id="56bed-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="56bed-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="56bed-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="56bed-111">Syntax</span></span>


```C++
HRESULT put_Notes(
  [in]          BSTR virtualMachineNotes
);

HRESULT get_Notes(
  [out, retval] BSTR *virtualMachineNotes
);
```



## <a name="property-value"></a><span data-ttu-id="56bed-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="56bed-112">Property value</span></span>

<span data-ttu-id="56bed-113">指定虛擬機器的附注。</span><span class="sxs-lookup"><span data-stu-id="56bed-113">Specifies the notes for the virtual machine.</span></span> <span data-ttu-id="56bed-114">字串的最大長度是65536個字元。</span><span class="sxs-lookup"><span data-stu-id="56bed-114">The maximum length of the string is 65,536 characters.</span></span>

<span data-ttu-id="56bed-115">若要移除任何附注，請傳遞空字串。</span><span class="sxs-lookup"><span data-stu-id="56bed-115">To remove any notes, pass an empty string.</span></span>

## <a name="error-codes"></a><span data-ttu-id="56bed-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="56bed-116">Error codes</span></span>



| <span data-ttu-id="56bed-117">名稱/值</span><span class="sxs-lookup"><span data-stu-id="56bed-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="56bed-118">意義</span><span class="sxs-lookup"><span data-stu-id="56bed-118">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56bed-119"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="56bed-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="56bed-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="56bed-120">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="56bed-121"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="56bed-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="56bed-122">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="56bed-122">The parameter is **NULL**.</span></span><br/>                                          |
| <dl> <span data-ttu-id="56bed-123"><dt>E \_INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="56bed-123"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="56bed-124">參數無效或包含超過65536個字元。</span><span class="sxs-lookup"><span data-stu-id="56bed-124">The parameter is not valid or contains more than 65,536 characters.</span></span><br/> |
| <dl> <span data-ttu-id="56bed-125"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="56bed-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="56bed-126">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="56bed-126">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="56bed-127"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="56bed-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="56bed-128">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="56bed-128">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="56bed-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="56bed-129">Requirements</span></span>



| <span data-ttu-id="56bed-130">需求</span><span class="sxs-lookup"><span data-stu-id="56bed-130">Requirement</span></span> | <span data-ttu-id="56bed-131">值</span><span class="sxs-lookup"><span data-stu-id="56bed-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="56bed-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56bed-132">Minimum supported client</span></span><br/> | <span data-ttu-id="56bed-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56bed-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56bed-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56bed-134">Minimum supported server</span></span><br/> | <span data-ttu-id="56bed-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="56bed-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="56bed-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="56bed-136">End of client support</span></span><br/>    | <span data-ttu-id="56bed-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="56bed-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="56bed-138">產品</span><span class="sxs-lookup"><span data-stu-id="56bed-138">Product</span></span><br/>                  | <span data-ttu-id="56bed-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="56bed-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="56bed-140">標頭</span><span class="sxs-lookup"><span data-stu-id="56bed-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="56bed-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="56bed-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="56bed-142">IID</span><span class="sxs-lookup"><span data-stu-id="56bed-142">IID</span></span><br/>                      | <span data-ttu-id="56bed-143">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="56bed-143">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="56bed-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56bed-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56bed-145">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="56bed-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

