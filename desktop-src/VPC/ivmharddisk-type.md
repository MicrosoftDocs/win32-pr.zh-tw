---
title: 'IVMHardDisk Type 屬性 (VPCCOMInterfaces .h) '
description: 虛擬硬碟的類型。
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- 類型虛擬電腦
- Type property Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，Type 屬性
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3757d74de5fc99972be3c7d267b15c56da6bee16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025054"
---
# <a name="ivmharddisktype-property"></a><span data-ttu-id="762cf-106">IVMHardDisk：： Type 屬性</span><span class="sxs-lookup"><span data-stu-id="762cf-106">IVMHardDisk::Type property</span></span>

<span data-ttu-id="762cf-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="762cf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="762cf-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="762cf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="762cf-109">捕獲虛擬硬碟的類型。</span><span class="sxs-lookup"><span data-stu-id="762cf-109">Retrieves the type of the virtual hard disk.</span></span>

<span data-ttu-id="762cf-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="762cf-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="762cf-111">語法</span><span class="sxs-lookup"><span data-stu-id="762cf-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a><span data-ttu-id="762cf-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="762cf-112">Property value</span></span>

<span data-ttu-id="762cf-113">目前硬碟映射的類型。</span><span class="sxs-lookup"><span data-stu-id="762cf-113">The type of the current hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="762cf-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="762cf-114">Error codes</span></span>



| <span data-ttu-id="762cf-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="762cf-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="762cf-116">意義</span><span class="sxs-lookup"><span data-stu-id="762cf-116">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="762cf-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="762cf-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="762cf-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="762cf-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="762cf-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="762cf-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="762cf-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="762cf-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="762cf-121"><dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="762cf-121"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="762cf-122">找不到目前的硬碟影像檔案。</span><span class="sxs-lookup"><span data-stu-id="762cf-122">The current hard disk image file could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="762cf-123"><dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="762cf-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="762cf-124">目前硬碟映射的類型無效。</span><span class="sxs-lookup"><span data-stu-id="762cf-124">The type of the current hard disk image is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="762cf-125"><dt>VM \_E \_ HD \_ 映射 \_ 開啟 \_ 失敗</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="762cf-125"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="762cf-126">嘗試開啟目前的硬碟影像檔案時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="762cf-126">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="762cf-127"><dt>VM \_電子 \_ HD \_ 影像 \_ 存取</dt> <dt>0xA0040681</dt></span><span class="sxs-lookup"><span data-stu-id="762cf-127"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="762cf-128">嘗試存取目前的硬碟影像檔案時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="762cf-128">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="762cf-129"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="762cf-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="762cf-130">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="762cf-130">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="762cf-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="762cf-131">Requirements</span></span>



| <span data-ttu-id="762cf-132">需求</span><span class="sxs-lookup"><span data-stu-id="762cf-132">Requirement</span></span> | <span data-ttu-id="762cf-133">值</span><span class="sxs-lookup"><span data-stu-id="762cf-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="762cf-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="762cf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="762cf-135">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="762cf-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="762cf-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="762cf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="762cf-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="762cf-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="762cf-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="762cf-138">End of client support</span></span><br/>    | <span data-ttu-id="762cf-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="762cf-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="762cf-140">產品</span><span class="sxs-lookup"><span data-stu-id="762cf-140">Product</span></span><br/>                  | <span data-ttu-id="762cf-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="762cf-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="762cf-142">標頭</span><span class="sxs-lookup"><span data-stu-id="762cf-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="762cf-143"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="762cf-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="762cf-144">IID</span><span class="sxs-lookup"><span data-stu-id="762cf-144">IID</span></span><br/>                      | <span data-ttu-id="762cf-145">IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="762cf-145">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="762cf-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="762cf-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="762cf-147">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="762cf-147">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

