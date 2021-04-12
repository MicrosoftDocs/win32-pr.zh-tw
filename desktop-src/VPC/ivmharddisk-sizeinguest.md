---
title: 'IVMHardDisk SizeInGuest 屬性 (VPCCOMInterfaces .h) '
description: 抓取客體作業系統中虛擬硬碟的大小。
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- SizeInGuest 屬性 Virtual PC
- SizeInGuest 屬性 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，SizeInGuest 屬性
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace142bf7c0dc612de47c8b2cb043ce24d6e9e9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104916"
---
# <a name="ivmharddisksizeinguest-property"></a><span data-ttu-id="82b43-106">IVMHardDisk：： SizeInGuest 屬性</span><span class="sxs-lookup"><span data-stu-id="82b43-106">IVMHardDisk::SizeInGuest property</span></span>

<span data-ttu-id="82b43-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="82b43-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="82b43-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="82b43-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="82b43-109">抓取客體作業系統中虛擬硬碟的大小。</span><span class="sxs-lookup"><span data-stu-id="82b43-109">Retrieves the size of the virtual hard disk in the guest operating system.</span></span>

<span data-ttu-id="82b43-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="82b43-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="82b43-111">語法</span><span class="sxs-lookup"><span data-stu-id="82b43-111">Syntax</span></span>


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="82b43-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="82b43-112">Property value</span></span>

<span data-ttu-id="82b43-113">硬碟影像的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="82b43-113">The size, in bytes, of the hard disk image.</span></span> <span data-ttu-id="82b43-114">此值為 VT  DECIMAL 類型的變數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="82b43-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="82b43-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="82b43-115">Error codes</span></span>



| <span data-ttu-id="82b43-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="82b43-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="82b43-117">意義</span><span class="sxs-lookup"><span data-stu-id="82b43-117">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82b43-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="82b43-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="82b43-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="82b43-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="82b43-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="82b43-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="82b43-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="82b43-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="82b43-122"><dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="82b43-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="82b43-123">找不到目前的虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="82b43-123">The current virtual hard disk file could not be found.</span></span><br/>                         |
| <dl> <span data-ttu-id="82b43-124"><dt>VM \_E \_ HD \_ 映射 \_ 開啟 \_ 失敗</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="82b43-124"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="82b43-125">嘗試開啟目前的硬碟影像檔案時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="82b43-125">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="82b43-126"><dt>VM \_電子 \_ HD \_ 影像 \_ 存取</dt> <dt>0xA0040681</dt></span><span class="sxs-lookup"><span data-stu-id="82b43-126"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="82b43-127">嘗試存取目前的硬碟影像檔案時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="82b43-127">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="82b43-128"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="82b43-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="82b43-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="82b43-129">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="82b43-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="82b43-130">Requirements</span></span>



| <span data-ttu-id="82b43-131">需求</span><span class="sxs-lookup"><span data-stu-id="82b43-131">Requirement</span></span> | <span data-ttu-id="82b43-132">值</span><span class="sxs-lookup"><span data-stu-id="82b43-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b43-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82b43-133">Minimum supported client</span></span><br/> | <span data-ttu-id="82b43-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82b43-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82b43-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82b43-135">Minimum supported server</span></span><br/> | <span data-ttu-id="82b43-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="82b43-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="82b43-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="82b43-137">End of client support</span></span><br/>    | <span data-ttu-id="82b43-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="82b43-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="82b43-139">產品</span><span class="sxs-lookup"><span data-stu-id="82b43-139">Product</span></span><br/>                  | <span data-ttu-id="82b43-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="82b43-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="82b43-141">標頭</span><span class="sxs-lookup"><span data-stu-id="82b43-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="82b43-142"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="82b43-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="82b43-143">IID</span><span class="sxs-lookup"><span data-stu-id="82b43-143">IID</span></span><br/>                      | <span data-ttu-id="82b43-144">IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="82b43-144">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="82b43-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82b43-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b43-146">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="82b43-146">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

