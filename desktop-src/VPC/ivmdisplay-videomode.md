---
title: 'IVMDisplay VideoMode 屬性 (VPCCOMInterfaces .h) '
description: 抓取目前的影片模式。
ms.assetid: e5a090c2-f7e6-4b85-8729-64d2ff68fcf3
keywords:
- VideoMode 屬性 Virtual PC
- VideoMode 屬性 Virtual PC，IVMDisplay 介面
- IVMDisplay 介面 Virtual PC，VideoMode 屬性
topic_type:
- apiref
api_name:
- IVMDisplay.VideoMode
- IVMDisplay.get_VideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164a658766cb8973a7c1ac403756ee888abab1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934329"
---
# <a name="ivmdisplayvideomode-property"></a><span data-ttu-id="9d445-106">IVMDisplay：： VideoMode 屬性</span><span class="sxs-lookup"><span data-stu-id="9d445-106">IVMDisplay::VideoMode property</span></span>

<span data-ttu-id="9d445-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="9d445-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9d445-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="9d445-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9d445-109">抓取目前的影片模式。</span><span class="sxs-lookup"><span data-stu-id="9d445-109">Retrieves the current video mode.</span></span>

<span data-ttu-id="9d445-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9d445-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d445-111">語法</span><span class="sxs-lookup"><span data-stu-id="9d445-111">Syntax</span></span>


```C++
HRESULT get_VideoMode(
  [out, retval] VMDisplayVideoMode *videoMode
);
```



## <a name="property-value"></a><span data-ttu-id="9d445-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="9d445-112">Property value</span></span>

<span data-ttu-id="9d445-113">客體作業系統目前的影片模式。</span><span class="sxs-lookup"><span data-stu-id="9d445-113">The current video mode of the guest operating system.</span></span> <span data-ttu-id="9d445-114">如需值的清單，請參閱 [**VMDisplayVideoMode**](vmdisplayvideomode.md)。</span><span class="sxs-lookup"><span data-stu-id="9d445-114">For a list of values, see [**VMDisplayVideoMode**](vmdisplayvideomode.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="9d445-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9d445-115">Error codes</span></span>



| <span data-ttu-id="9d445-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="9d445-116">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="9d445-117">意義</span><span class="sxs-lookup"><span data-stu-id="9d445-117">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d445-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9d445-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="9d445-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="9d445-119">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="9d445-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9d445-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="9d445-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9d445-121">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9d445-122"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="9d445-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="9d445-123">虛擬機器必須正在執行，才能進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="9d445-123">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="9d445-124"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="9d445-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="9d445-125">虛擬機器無效或目前未執行。</span><span class="sxs-lookup"><span data-stu-id="9d445-125">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="9d445-126"><dt>VM \_E \_ NO \_ DISPLAY</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="9d445-126"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="9d445-127">找不到虛擬機器的有效顯示。</span><span class="sxs-lookup"><span data-stu-id="9d445-127">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="9d445-128"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9d445-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="9d445-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9d445-129">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="9d445-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d445-130">Requirements</span></span>



| <span data-ttu-id="9d445-131">需求</span><span class="sxs-lookup"><span data-stu-id="9d445-131">Requirement</span></span> | <span data-ttu-id="9d445-132">值</span><span class="sxs-lookup"><span data-stu-id="9d445-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d445-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d445-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9d445-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d445-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d445-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d445-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9d445-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="9d445-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9d445-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9d445-137">End of client support</span></span><br/>    | <span data-ttu-id="9d445-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9d445-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9d445-139">產品</span><span class="sxs-lookup"><span data-stu-id="9d445-139">Product</span></span><br/>                  | <span data-ttu-id="9d445-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9d445-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9d445-141">標頭</span><span class="sxs-lookup"><span data-stu-id="9d445-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d445-142"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d445-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9d445-143">IID</span><span class="sxs-lookup"><span data-stu-id="9d445-143">IID</span></span><br/>                      | <span data-ttu-id="9d445-144">IID \_ IVMDisplay 定義為960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="9d445-144">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="9d445-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d445-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d445-146">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="9d445-146">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

