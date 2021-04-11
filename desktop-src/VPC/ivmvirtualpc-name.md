---
title: 'IVMVirtualPC Name 屬性 (VPCCOMInterfaces .h) '
description: 抓取 Windows Virtual PC 應用程式的名稱。
ms.assetid: d33af684-ecba-4177-9ef3-cf6dff5bee4d
keywords:
- Name 屬性 Virtual PC
- Name 屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，Name 屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.Name
- IVMVirtualPC.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0bab8dbb624a63d5278560f8285abeac49166a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685965"
---
# <a name="ivmvirtualpcname-property"></a><span data-ttu-id="484d6-106">IVMVirtualPC：： Name 屬性</span><span class="sxs-lookup"><span data-stu-id="484d6-106">IVMVirtualPC::Name property</span></span>

<span data-ttu-id="484d6-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="484d6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="484d6-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="484d6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="484d6-109">抓取 Windows Virtual PC 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="484d6-109">Retrieves the name of the Windows Virtual PC application.</span></span>

<span data-ttu-id="484d6-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="484d6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="484d6-111">語法</span><span class="sxs-lookup"><span data-stu-id="484d6-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualPCName
);
```



## <a name="property-value"></a><span data-ttu-id="484d6-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="484d6-112">Property value</span></span>

<span data-ttu-id="484d6-113">Windows Virtual PC 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="484d6-113">The name of the Windows Virtual PC application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="484d6-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="484d6-114">Error codes</span></span>



| <span data-ttu-id="484d6-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="484d6-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="484d6-116">意義</span><span class="sxs-lookup"><span data-stu-id="484d6-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="484d6-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="484d6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="484d6-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="484d6-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="484d6-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="484d6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="484d6-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="484d6-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="484d6-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="484d6-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="484d6-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="484d6-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="484d6-123"><dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="484d6-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="484d6-124">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="484d6-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="484d6-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="484d6-125">Requirements</span></span>



| <span data-ttu-id="484d6-126">需求</span><span class="sxs-lookup"><span data-stu-id="484d6-126">Requirement</span></span> | <span data-ttu-id="484d6-127">值</span><span class="sxs-lookup"><span data-stu-id="484d6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="484d6-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="484d6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="484d6-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="484d6-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="484d6-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="484d6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="484d6-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="484d6-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="484d6-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="484d6-132">End of client support</span></span><br/>    | <span data-ttu-id="484d6-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="484d6-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="484d6-134">產品</span><span class="sxs-lookup"><span data-stu-id="484d6-134">Product</span></span><br/>                  | <span data-ttu-id="484d6-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="484d6-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="484d6-136">標頭</span><span class="sxs-lookup"><span data-stu-id="484d6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="484d6-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="484d6-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="484d6-138">IID</span><span class="sxs-lookup"><span data-stu-id="484d6-138">IID</span></span><br/>                      | <span data-ttu-id="484d6-139">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="484d6-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="484d6-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="484d6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="484d6-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="484d6-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

