---
title: 'IVMGuestOS GetOsVersionInfo 方法 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器中執行之客體作業系統的版本資訊。
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- GetOsVersionInfo 方法 Virtual PC
- GetOsVersionInfo 方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，GetOsVersionInfo 方法
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec0c0c2516a8ef16a3d9d9c6c4178abb31bd52f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965324"
---
# <a name="ivmguestosgetosversioninfo-method"></a><span data-ttu-id="15b46-106">IVMGuestOS：： GetOsVersionInfo 方法</span><span class="sxs-lookup"><span data-stu-id="15b46-106">IVMGuestOS::GetOsVersionInfo method</span></span>

<span data-ttu-id="15b46-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="15b46-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="15b46-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="15b46-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="15b46-109">抓取虛擬機器中執行之客體作業系統 (VM) 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="15b46-109">Retrieves version information for the guest operating system running in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="15b46-110">語法</span><span class="sxs-lookup"><span data-stu-id="15b46-110">Syntax</span></span>


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="15b46-111">參數</span><span class="sxs-lookup"><span data-stu-id="15b46-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15b46-112">*guestOsVersionInfo* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="15b46-112">*guestOsVersionInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="15b46-113">[**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="15b46-113">A pointer to a [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15b46-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="15b46-114">Return value</span></span>

<span data-ttu-id="15b46-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="15b46-115">This method can return one of these values.</span></span>



| <span data-ttu-id="15b46-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="15b46-116">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="15b46-117">Description</span><span class="sxs-lookup"><span data-stu-id="15b46-117">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="15b46-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="15b46-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="15b46-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="15b46-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="15b46-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="15b46-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="15b46-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="15b46-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="15b46-122"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="15b46-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="15b46-123">沒有足夠的記憶體可完成此要求。</span><span class="sxs-lookup"><span data-stu-id="15b46-123">There is not enough memory available to complete this request.</span></span><br/> |
| <dl> <span data-ttu-id="15b46-124"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="15b46-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="15b46-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="15b46-125">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="15b46-126"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="15b46-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="15b46-127">VM 未執行。</span><span class="sxs-lookup"><span data-stu-id="15b46-127">The VM is not running.</span></span><br/>                                         |
| <dl> <span data-ttu-id="15b46-128"><dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="15b46-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="15b46-129">此 VM 中未安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="15b46-129">Integration components are not installed in this VM.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="15b46-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="15b46-130">Requirements</span></span>



| <span data-ttu-id="15b46-131">需求</span><span class="sxs-lookup"><span data-stu-id="15b46-131">Requirement</span></span> | <span data-ttu-id="15b46-132">值</span><span class="sxs-lookup"><span data-stu-id="15b46-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="15b46-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15b46-133">Minimum supported client</span></span><br/> | <span data-ttu-id="15b46-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15b46-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15b46-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15b46-135">Minimum supported server</span></span><br/> | <span data-ttu-id="15b46-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="15b46-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="15b46-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="15b46-137">End of client support</span></span><br/>    | <span data-ttu-id="15b46-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="15b46-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="15b46-139">產品</span><span class="sxs-lookup"><span data-stu-id="15b46-139">Product</span></span><br/>                  | <span data-ttu-id="15b46-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="15b46-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="15b46-141">標頭</span><span class="sxs-lookup"><span data-stu-id="15b46-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="15b46-142"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="15b46-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="15b46-143">IID</span><span class="sxs-lookup"><span data-stu-id="15b46-143">IID</span></span><br/>                      | <span data-ttu-id="15b46-144">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="15b46-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="15b46-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15b46-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15b46-146">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="15b46-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

