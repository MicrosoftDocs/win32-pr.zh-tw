---
title: 'IVMVirtualMachine RdpPipeName 屬性 (VPCCOMInterfaces .h) '
description: 抓取用於影片和輸入的 RDP 連接具名管道名稱。
ms.assetid: 0c2d0f23-40cd-4a86-96dd-546fb3570871
keywords:
- RdpPipeName 屬性 Virtual PC
- RdpPipeName 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，RdpPipeName 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RdpPipeName
- IVMVirtualMachine.get_RdpPipeName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86e49463c5e443a07d1fa86736047435eaf60a06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024531"
---
# <a name="ivmvirtualmachinerdppipename-property"></a><span data-ttu-id="0bc94-106">IVMVirtualMachine：： RdpPipeName 屬性</span><span class="sxs-lookup"><span data-stu-id="0bc94-106">IVMVirtualMachine::RdpPipeName property</span></span>

<span data-ttu-id="0bc94-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="0bc94-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0bc94-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="0bc94-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0bc94-109">抓取用於影片和輸入的 RDP 連接具名管道名稱。</span><span class="sxs-lookup"><span data-stu-id="0bc94-109">Retrieves the name of the RDP connection named pipe used for video and input.</span></span>

<span data-ttu-id="0bc94-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0bc94-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc94-111">語法</span><span class="sxs-lookup"><span data-stu-id="0bc94-111">Syntax</span></span>


```C++
HRESULT get_RdpPipeName(
  [out, retval] BSTR *RdpPipeName
);
```



## <a name="property-value"></a><span data-ttu-id="0bc94-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="0bc94-112">Property value</span></span>

<span data-ttu-id="0bc94-113">用於影片和輸入的 RDP 連接具名管道的名稱。</span><span class="sxs-lookup"><span data-stu-id="0bc94-113">Name of the RDP connection named pipe used for video and input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0bc94-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0bc94-114">Error codes</span></span>

<span data-ttu-id="0bc94-115">如果方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0bc94-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0bc94-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0bc94-116">Otherwise, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="0bc94-117">名稱/值</span><span class="sxs-lookup"><span data-stu-id="0bc94-117">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="0bc94-118">意義</span><span class="sxs-lookup"><span data-stu-id="0bc94-118">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="0bc94-119"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0bc94-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="0bc94-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="0bc94-120">The operation was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="0bc94-121"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0bc94-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="0bc94-122">RdpPipeName 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0bc94-122">The RdpPipeName parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="0bc94-123"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="0bc94-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="0bc94-124">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="0bc94-124">The virtual machine is not running.</span></span><br/>    |
| <dl> <span data-ttu-id="0bc94-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0bc94-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="0bc94-126">發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0bc94-126">An unknown error occurred.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="0bc94-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bc94-127">Requirements</span></span>



| <span data-ttu-id="0bc94-128">需求</span><span class="sxs-lookup"><span data-stu-id="0bc94-128">Requirement</span></span> | <span data-ttu-id="0bc94-129">值</span><span class="sxs-lookup"><span data-stu-id="0bc94-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc94-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0bc94-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0bc94-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0bc94-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0bc94-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0bc94-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0bc94-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="0bc94-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0bc94-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0bc94-134">End of client support</span></span><br/>    | <span data-ttu-id="0bc94-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0bc94-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0bc94-136">產品</span><span class="sxs-lookup"><span data-stu-id="0bc94-136">Product</span></span><br/>                  | <span data-ttu-id="0bc94-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0bc94-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0bc94-138">標頭</span><span class="sxs-lookup"><span data-stu-id="0bc94-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bc94-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="0bc94-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0bc94-140">IID</span><span class="sxs-lookup"><span data-stu-id="0bc94-140">IID</span></span><br/>                      | <span data-ttu-id="0bc94-141">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="0bc94-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="0bc94-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0bc94-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc94-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="0bc94-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

