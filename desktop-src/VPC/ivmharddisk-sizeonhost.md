---
title: 'IVMHardDisk SizeOnHost 屬性 (VPCCOMInterfaces .h) '
description: 主機電腦上虛擬硬碟檔案的大小。
ms.assetid: f787ec4b-7b4f-4d35-b07c-4844424d91cf
keywords:
- SizeOnHost 屬性 Virtual PC
- SizeOnHost 屬性 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，SizeOnHost 屬性
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeOnHost
- IVMHardDisk.get_SizeOnHost
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a000a70e1713b28f8fb8eea3590a53fb46ff0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025307"
---
# <a name="ivmharddisksizeonhost-property"></a><span data-ttu-id="2ea04-106">IVMHardDisk：： SizeOnHost 屬性</span><span class="sxs-lookup"><span data-stu-id="2ea04-106">IVMHardDisk::SizeOnHost property</span></span>

<span data-ttu-id="2ea04-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="2ea04-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2ea04-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="2ea04-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2ea04-109">抓取主機電腦上虛擬硬碟檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="2ea04-109">Retrieves the size of the virtual hard disk file on the host computer.</span></span>

<span data-ttu-id="2ea04-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2ea04-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ea04-111">語法</span><span class="sxs-lookup"><span data-stu-id="2ea04-111">Syntax</span></span>


```C++
HRESULT get_SizeOnHost(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="2ea04-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="2ea04-112">Property value</span></span>

<span data-ttu-id="2ea04-113">硬碟影像檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2ea04-113">The size, in bytes, of the hard disk image file.</span></span> <span data-ttu-id="2ea04-114">此值為 **VT \_ DECIMAL** 類型的 **變數**。</span><span class="sxs-lookup"><span data-stu-id="2ea04-114">This value is a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2ea04-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2ea04-115">Error codes</span></span>



| <span data-ttu-id="2ea04-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="2ea04-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="2ea04-117">意義</span><span class="sxs-lookup"><span data-stu-id="2ea04-117">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="2ea04-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2ea04-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="2ea04-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="2ea04-119">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="2ea04-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2ea04-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="2ea04-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2ea04-121">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="2ea04-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2ea04-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="2ea04-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2ea04-123">An unexpected error has occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="2ea04-124"><dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="2ea04-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="2ea04-125">找不到硬碟影像檔案。</span><span class="sxs-lookup"><span data-stu-id="2ea04-125">The hard disk image file was not found.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2ea04-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ea04-126">Requirements</span></span>



| <span data-ttu-id="2ea04-127">需求</span><span class="sxs-lookup"><span data-stu-id="2ea04-127">Requirement</span></span> | <span data-ttu-id="2ea04-128">值</span><span class="sxs-lookup"><span data-stu-id="2ea04-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ea04-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ea04-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2ea04-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ea04-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2ea04-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ea04-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2ea04-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="2ea04-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2ea04-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2ea04-133">End of client support</span></span><br/>    | <span data-ttu-id="2ea04-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2ea04-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2ea04-135">產品</span><span class="sxs-lookup"><span data-stu-id="2ea04-135">Product</span></span><br/>                  | <span data-ttu-id="2ea04-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2ea04-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2ea04-137">標頭</span><span class="sxs-lookup"><span data-stu-id="2ea04-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ea04-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ea04-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2ea04-139">IID</span><span class="sxs-lookup"><span data-stu-id="2ea04-139">IID</span></span><br/>                      | <span data-ttu-id="2ea04-140">IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="2ea04-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="2ea04-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ea04-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ea04-142">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="2ea04-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

