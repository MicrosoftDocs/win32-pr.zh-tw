---
title: 'IVMFloppyDrive ReleaseImage 方法 (VPCCOMInterfaces .h) '
description: 從軟碟磁碟機釋放主機上的軟碟媒體映射。
ms.assetid: 12fc6dc4-8450-4122-b0f0-ed11cc10134c
keywords:
- ReleaseImage 方法 Virtual PC
- ReleaseImage 方法 Virtual PC，IVMFloppyDrive 介面
- IVMFloppyDrive 介面 Virtual PC，ReleaseImage 方法
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece899bbb615fc2d54a3cbdc86193e743168ef23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685474"
---
# <a name="ivmfloppydrivereleaseimage-method"></a><span data-ttu-id="b66ff-106">IVMFloppyDrive：： ReleaseImage 方法</span><span class="sxs-lookup"><span data-stu-id="b66ff-106">IVMFloppyDrive::ReleaseImage method</span></span>

<span data-ttu-id="b66ff-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="b66ff-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b66ff-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="b66ff-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b66ff-109">從軟碟磁碟機釋放主機上的軟碟媒體映射。</span><span class="sxs-lookup"><span data-stu-id="b66ff-109">Releases a floppy media image on the host from the floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="b66ff-110">語法</span><span class="sxs-lookup"><span data-stu-id="b66ff-110">Syntax</span></span>


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a><span data-ttu-id="b66ff-111">參數</span><span class="sxs-lookup"><span data-stu-id="b66ff-111">Parameters</span></span>

<span data-ttu-id="b66ff-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b66ff-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b66ff-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b66ff-113">Return value</span></span>

<span data-ttu-id="b66ff-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b66ff-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b66ff-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="b66ff-115">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="b66ff-116">Description</span><span class="sxs-lookup"><span data-stu-id="b66ff-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b66ff-117"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b66ff-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="b66ff-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="b66ff-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b66ff-119"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="b66ff-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>          | <span data-ttu-id="b66ff-120">此虛擬機器的設定無效或找不到。</span><span class="sxs-lookup"><span data-stu-id="b66ff-120">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="b66ff-121"><dt>**VM \_E \_ 媒體有 \_ 錯誤的 \_ 類型**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="b66ff-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl>  | <span data-ttu-id="b66ff-122">連接到這個磁片磁碟機的媒體不是磁碟片映射。</span><span class="sxs-lookup"><span data-stu-id="b66ff-122">The media attached to this floppy drive is not a floppy disk image.</span></span><br/>         |
| <dl> <span data-ttu-id="b66ff-123"><dt>**VM \_E \_ 未 \_ \_ 捕獲媒體**</dt> <dt>0xA00400652</dt></span><span class="sxs-lookup"><span data-stu-id="b66ff-123"><dt>**VM\_E\_NO\_MEDIA\_CAPTURED**</dt> <dt>0xA00400652</dt></span></span> </dl> | <span data-ttu-id="b66ff-124">沒有媒體連接到這個磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b66ff-124">There is no media attached to this floppy drive.</span></span><br/>                            |
| <dl> <span data-ttu-id="b66ff-125"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b66ff-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="b66ff-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b66ff-126">An unexpected error has occurred.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="b66ff-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="b66ff-127">Requirements</span></span>



| <span data-ttu-id="b66ff-128">需求</span><span class="sxs-lookup"><span data-stu-id="b66ff-128">Requirement</span></span> | <span data-ttu-id="b66ff-129">值</span><span class="sxs-lookup"><span data-stu-id="b66ff-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b66ff-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b66ff-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b66ff-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b66ff-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b66ff-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b66ff-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b66ff-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="b66ff-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b66ff-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b66ff-134">End of client support</span></span><br/>    | <span data-ttu-id="b66ff-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b66ff-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b66ff-136">產品</span><span class="sxs-lookup"><span data-stu-id="b66ff-136">Product</span></span><br/>                  | <span data-ttu-id="b66ff-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b66ff-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b66ff-138">標頭</span><span class="sxs-lookup"><span data-stu-id="b66ff-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b66ff-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="b66ff-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b66ff-140">IID</span><span class="sxs-lookup"><span data-stu-id="b66ff-140">IID</span></span><br/>                      | <span data-ttu-id="b66ff-141">IID \_ IVMFloppyDrive 定義為661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="b66ff-141">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b66ff-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b66ff-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b66ff-143">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="b66ff-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

