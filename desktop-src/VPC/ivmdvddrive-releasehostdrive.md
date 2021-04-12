---
title: 'IVMDVDDrive ReleaseHostDrive 方法 (VPCCOMInterfaces .h) '
description: 從 DVD 光碟機釋放已捕捉的主機磁片磁碟機。
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- ReleaseHostDrive 方法 Virtual PC
- ReleaseHostDrive 方法 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，ReleaseHostDrive 方法
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ed2c551ba619855743266b9b506a0c579f92a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384438"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a><span data-ttu-id="bc210-106">IVMDVDDrive：： ReleaseHostDrive 方法</span><span class="sxs-lookup"><span data-stu-id="bc210-106">IVMDVDDrive::ReleaseHostDrive method</span></span>

<span data-ttu-id="bc210-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="bc210-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bc210-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="bc210-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bc210-109">從 DVD 光碟機釋放已捕捉的主機磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bc210-109">Releases a captured host drive from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc210-110">語法</span><span class="sxs-lookup"><span data-stu-id="bc210-110">Syntax</span></span>


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a><span data-ttu-id="bc210-111">參數</span><span class="sxs-lookup"><span data-stu-id="bc210-111">Parameters</span></span>

<span data-ttu-id="bc210-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bc210-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc210-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc210-113">Return value</span></span>

<span data-ttu-id="bc210-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bc210-114">This method can return one of these values.</span></span>



| <span data-ttu-id="bc210-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="bc210-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="bc210-116">Description</span><span class="sxs-lookup"><span data-stu-id="bc210-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bc210-117"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bc210-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="bc210-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="bc210-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="bc210-119"><dt>**E \_FAIL**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="bc210-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="bc210-120">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bc210-120">An unexpected error has occurred.</span></span><br/>                                  |
| <dl> <span data-ttu-id="bc210-121"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="bc210-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="bc210-122">找不到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bc210-122">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="bc210-123"><dt>**VM \_E \_ 媒體有 \_ 錯誤的 \_ 類型**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="bc210-123"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="bc210-124">目前所捕獲的媒體不是主機磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bc210-124">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="bc210-125"><dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="bc210-125"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="bc210-126">因為匯流排位置無效，所以無法初始化磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bc210-126">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="bc210-127"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bc210-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="bc210-128">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bc210-128">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="bc210-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc210-129">Requirements</span></span>



| <span data-ttu-id="bc210-130">需求</span><span class="sxs-lookup"><span data-stu-id="bc210-130">Requirement</span></span> | <span data-ttu-id="bc210-131">值</span><span class="sxs-lookup"><span data-stu-id="bc210-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc210-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc210-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bc210-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc210-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bc210-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc210-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bc210-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="bc210-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bc210-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="bc210-136">End of client support</span></span><br/>    | <span data-ttu-id="bc210-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bc210-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bc210-138">產品</span><span class="sxs-lookup"><span data-stu-id="bc210-138">Product</span></span><br/>                  | <span data-ttu-id="bc210-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bc210-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bc210-140">標頭</span><span class="sxs-lookup"><span data-stu-id="bc210-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc210-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="bc210-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bc210-142">IID</span><span class="sxs-lookup"><span data-stu-id="bc210-142">IID</span></span><br/>                      | <span data-ttu-id="bc210-143">IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="bc210-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="bc210-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc210-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc210-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="bc210-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

