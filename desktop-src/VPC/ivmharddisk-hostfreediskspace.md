---
title: 'IVMHardDisk HostFreeDiskSpace 屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬硬碟主機上的剩餘可用磁碟空間量。
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- HostFreeDiskSpace 屬性 Virtual PC
- HostFreeDiskSpace 屬性 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，HostFreeDiskSpace 屬性
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105810"
---
# <a name="ivmharddiskhostfreediskspace-property"></a><span data-ttu-id="10e9a-106">IVMHardDisk：： HostFreeDiskSpace 屬性</span><span class="sxs-lookup"><span data-stu-id="10e9a-106">IVMHardDisk::HostFreeDiskSpace property</span></span>

<span data-ttu-id="10e9a-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="10e9a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="10e9a-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="10e9a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="10e9a-109">抓取虛擬硬碟主機上的剩餘可用磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="10e9a-109">Retrieves the amount of remaining disk space available on the host for the virtual hard disk.</span></span>

<span data-ttu-id="10e9a-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="10e9a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="10e9a-111">語法</span><span class="sxs-lookup"><span data-stu-id="10e9a-111">Syntax</span></span>


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a><span data-ttu-id="10e9a-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="10e9a-112">Property value</span></span>

<span data-ttu-id="10e9a-113">主機電腦上目前硬碟影像檔案的剩餘可用磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="10e9a-113">The amount of remaining disk space available on the host computer for the current hard disk image file.</span></span> <span data-ttu-id="10e9a-114">此值為 VT  DECIMAL 類型的變數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="10e9a-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="10e9a-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="10e9a-115">Error codes</span></span>



| <span data-ttu-id="10e9a-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="10e9a-116">Name/value</span></span>                                                                                                                                                                            | <span data-ttu-id="10e9a-117">意義</span><span class="sxs-lookup"><span data-stu-id="10e9a-117">Meaning</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="10e9a-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="10e9a-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                               | <span data-ttu-id="10e9a-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="10e9a-119">The operation was successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="10e9a-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="10e9a-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                 | <span data-ttu-id="10e9a-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="10e9a-121">The parameter is **NULL**.</span></span><br/>                                   |
| <dl> <span data-ttu-id="10e9a-122"><dt>HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤) </dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="10e9a-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl> | <span data-ttu-id="10e9a-123">目前虛擬硬碟檔案的路徑無效。</span><span class="sxs-lookup"><span data-stu-id="10e9a-123">The path to the current virtual hard disk file is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="10e9a-124"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="10e9a-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                         | <span data-ttu-id="10e9a-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="10e9a-125">An unexpected error has occurred.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="10e9a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="10e9a-126">Requirements</span></span>



| <span data-ttu-id="10e9a-127">需求</span><span class="sxs-lookup"><span data-stu-id="10e9a-127">Requirement</span></span> | <span data-ttu-id="10e9a-128">值</span><span class="sxs-lookup"><span data-stu-id="10e9a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="10e9a-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10e9a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="10e9a-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10e9a-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="10e9a-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10e9a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="10e9a-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="10e9a-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="10e9a-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="10e9a-133">End of client support</span></span><br/>    | <span data-ttu-id="10e9a-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="10e9a-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="10e9a-135">產品</span><span class="sxs-lookup"><span data-stu-id="10e9a-135">Product</span></span><br/>                  | <span data-ttu-id="10e9a-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="10e9a-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="10e9a-137">標頭</span><span class="sxs-lookup"><span data-stu-id="10e9a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="10e9a-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="10e9a-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="10e9a-139">IID</span><span class="sxs-lookup"><span data-stu-id="10e9a-139">IID</span></span><br/>                      | <span data-ttu-id="10e9a-140">IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="10e9a-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="10e9a-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10e9a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10e9a-142">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="10e9a-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

