---
title: 'IVMDisplay Graphicswindow.canresize 屬性 (VPCCOMInterfaces .h) '
description: 判斷來賓是否允許解析變更。
ms.assetid: 97f2aad9-aa27-4db2-ac5d-fa9645f0e674
keywords:
- Graphicswindow.canresize 屬性 Virtual PC
- Graphicswindow.canresize 屬性 Virtual PC，IVMDisplay 介面
- IVMDisplay 介面 Virtual PC，Graphicswindow.canresize 屬性
topic_type:
- apiref
api_name:
- IVMDisplay.CanResize
- IVMDisplay.get_CanResize
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca865189b1fd155e0edf85bac9a36d94ffe5d656
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686412"
---
# <a name="ivmdisplaycanresize-property"></a><span data-ttu-id="2dac3-106">IVMDisplay：： Graphicswindow.canresize 屬性</span><span class="sxs-lookup"><span data-stu-id="2dac3-106">IVMDisplay::CanResize property</span></span>

<span data-ttu-id="2dac3-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="2dac3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2dac3-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="2dac3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2dac3-109">判斷來賓是否允許解析變更。</span><span class="sxs-lookup"><span data-stu-id="2dac3-109">Determines whether the Guest allows resolution changes.</span></span>

<span data-ttu-id="2dac3-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2dac3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dac3-111">語法</span><span class="sxs-lookup"><span data-stu-id="2dac3-111">Syntax</span></span>


```C++
HRESULT get_CanResize(
  [out, retval] VARIANT_BOOL *canResize
);
```



## <a name="property-value"></a><span data-ttu-id="2dac3-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="2dac3-112">Property value</span></span>

<span data-ttu-id="2dac3-113">**變異 \_** 如果來賓允許解析變更，則為 TRUE，否則為 **VARIANT \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="2dac3-113">**VARIANT\_TRUE** if the Guest allows resolution changes and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2dac3-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2dac3-114">Error codes</span></span>



| <span data-ttu-id="2dac3-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="2dac3-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="2dac3-116">意義</span><span class="sxs-lookup"><span data-stu-id="2dac3-116">Meaning</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2dac3-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2dac3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="2dac3-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="2dac3-118">The operation was successful.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="2dac3-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2dac3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="2dac3-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2dac3-120">The parameter is **NULL**.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="2dac3-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="2dac3-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="2dac3-122">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="2dac3-122">The configuration is unknown.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="2dac3-123"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="2dac3-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="2dac3-124">虛擬機器必須正在執行，才能進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="2dac3-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="2dac3-125"><dt>VM \_E \_ NO \_ DISPLAY</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="2dac3-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="2dac3-126">找不到虛擬機器的影片裝置。</span><span class="sxs-lookup"><span data-stu-id="2dac3-126">There was no video device found for the virtual machine.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="2dac3-127"><dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="2dac3-127"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="2dac3-128">無法使用 [整合元件] 功能;可能是未安裝整合元件，或已停用此功能。</span><span class="sxs-lookup"><span data-stu-id="2dac3-128">The integration components feature is not available; either the integration components are not installed or the feature has been disabled.</span></span><br/> |
| <dl> <span data-ttu-id="2dac3-129"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2dac3-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="2dac3-130">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2dac3-130">An unexpected error has occurred.</span></span><br/>                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="2dac3-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="2dac3-131">Requirements</span></span>



| <span data-ttu-id="2dac3-132">需求</span><span class="sxs-lookup"><span data-stu-id="2dac3-132">Requirement</span></span> | <span data-ttu-id="2dac3-133">值</span><span class="sxs-lookup"><span data-stu-id="2dac3-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dac3-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2dac3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2dac3-135">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2dac3-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2dac3-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2dac3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2dac3-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="2dac3-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2dac3-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2dac3-138">End of client support</span></span><br/>    | <span data-ttu-id="2dac3-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2dac3-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2dac3-140">產品</span><span class="sxs-lookup"><span data-stu-id="2dac3-140">Product</span></span><br/>                  | <span data-ttu-id="2dac3-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2dac3-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2dac3-142">標頭</span><span class="sxs-lookup"><span data-stu-id="2dac3-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dac3-143"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="2dac3-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2dac3-144">IID</span><span class="sxs-lookup"><span data-stu-id="2dac3-144">IID</span></span><br/>                      | <span data-ttu-id="2dac3-145">IID \_ IVMDisplay 定義為960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="2dac3-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="2dac3-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2dac3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dac3-147">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="2dac3-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

