---
title: 'IVMVirtualPC Version 屬性 (VPCCOMInterfaces. h) '
description: 抓取此 Windows Virtual PC 實例的版本。
ms.assetid: efcd5e71-8752-45a2-8138-4bc214762f39
keywords:
- Version 屬性 Virtual PC
- Version 屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，Version 屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.Version
- IVMVirtualPC.get_Version
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0dc84fd714c50c0a0adb3084603aeea2419d3ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466977"
---
# <a name="ivmvirtualpcversion-property"></a><span data-ttu-id="001e5-106">IVMVirtualPC：： Version 屬性</span><span class="sxs-lookup"><span data-stu-id="001e5-106">IVMVirtualPC::Version property</span></span>

<span data-ttu-id="001e5-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="001e5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="001e5-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="001e5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="001e5-109">抓取此 Windows Virtual PC 實例的版本。</span><span class="sxs-lookup"><span data-stu-id="001e5-109">Retrieves the version of this instance of Windows Virtual PC.</span></span>

<span data-ttu-id="001e5-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="001e5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="001e5-111">語法</span><span class="sxs-lookup"><span data-stu-id="001e5-111">Syntax</span></span>


```C++
HRESULT get_Version(
  [out, retval] BSTR *version
);
```



## <a name="property-value"></a><span data-ttu-id="001e5-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="001e5-112">Property value</span></span>

<span data-ttu-id="001e5-113">版本。</span><span class="sxs-lookup"><span data-stu-id="001e5-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="001e5-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="001e5-114">Error codes</span></span>



| <span data-ttu-id="001e5-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="001e5-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="001e5-116">意義</span><span class="sxs-lookup"><span data-stu-id="001e5-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="001e5-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="001e5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="001e5-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="001e5-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="001e5-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="001e5-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="001e5-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="001e5-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="001e5-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="001e5-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="001e5-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="001e5-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="001e5-123"><dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="001e5-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="001e5-124">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="001e5-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="001e5-125">備註</span><span class="sxs-lookup"><span data-stu-id="001e5-125">Remarks</span></span>

<span data-ttu-id="001e5-126">Windows Virtual PC 版本資訊會以下列格式傳回字串值： "*v*。*s*。*bbb*。「 *t*」，其中 *v* 是主要版本號碼， *s* 是次要版本號碼， *bbb* 是組建編號， *t* 是組建類型 (0 = 發行組建) ，而 *ee* 是 server edition (SE = Standard edition，ee = Enterprise edition) 。</span><span class="sxs-lookup"><span data-stu-id="001e5-126">The Windows Virtual PC version information is returned as a string value with the following format: "*v*.*s*.*bbb*.*tee*", where *v* is the major version number, *s* is the minor version number, *bbb* is the build number, *t* is the build type (0 = release build), and *ee* is the server edition (SE = Standard Edition, EE = Enterprise Edition).</span></span>

## <a name="requirements"></a><span data-ttu-id="001e5-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="001e5-127">Requirements</span></span>



| <span data-ttu-id="001e5-128">需求</span><span class="sxs-lookup"><span data-stu-id="001e5-128">Requirement</span></span> | <span data-ttu-id="001e5-129">值</span><span class="sxs-lookup"><span data-stu-id="001e5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="001e5-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="001e5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="001e5-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="001e5-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="001e5-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="001e5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="001e5-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="001e5-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="001e5-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="001e5-134">End of client support</span></span><br/>    | <span data-ttu-id="001e5-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="001e5-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="001e5-136">產品</span><span class="sxs-lookup"><span data-stu-id="001e5-136">Product</span></span><br/>                  | <span data-ttu-id="001e5-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="001e5-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="001e5-138">標頭</span><span class="sxs-lookup"><span data-stu-id="001e5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="001e5-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="001e5-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="001e5-140">IID</span><span class="sxs-lookup"><span data-stu-id="001e5-140">IID</span></span><br/>                      | <span data-ttu-id="001e5-141">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="001e5-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="001e5-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="001e5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="001e5-143">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="001e5-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

