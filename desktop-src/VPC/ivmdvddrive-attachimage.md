---
title: 'IVMDVDDrive AttachImage 方法 (VPCCOMInterfaces .h) '
description: 將 ISO 映像附加至 VM 內的 DVD 光碟機。
ms.assetid: 08947898-ca3f-41b6-97a3-52dc6977fc6d
keywords:
- AttachImage 方法 Virtual PC
- AttachImage 方法 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，AttachImage 方法
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58204545e21bd7dbf48d21acbc232b9fc5d1e3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385150"
---
# <a name="ivmdvddriveattachimage-method"></a><span data-ttu-id="f0c5a-106">IVMDVDDrive：： AttachImage 方法</span><span class="sxs-lookup"><span data-stu-id="f0c5a-106">IVMDVDDrive::AttachImage method</span></span>

<span data-ttu-id="f0c5a-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="f0c5a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f0c5a-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="f0c5a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f0c5a-109">將 ISO 映像連接至虛擬機器 (VM) 內的 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="f0c5a-109">Attaches an ISO image to the DVD drive within the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c5a-110">語法</span><span class="sxs-lookup"><span data-stu-id="f0c5a-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR imagePath
);
```



## <a name="parameters"></a><span data-ttu-id="f0c5a-111">參數</span><span class="sxs-lookup"><span data-stu-id="f0c5a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c5a-112">*imagePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0c5a-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c5a-113">要附加之 ISO 映像的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f0c5a-113">The full path to the ISO image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c5a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0c5a-114">Return value</span></span>

<span data-ttu-id="f0c5a-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f0c5a-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f0c5a-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="f0c5a-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="f0c5a-117">Description</span><span class="sxs-lookup"><span data-stu-id="f0c5a-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0c5a-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f0c5a-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="f0c5a-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="f0c5a-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="f0c5a-120"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="f0c5a-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="f0c5a-121">*ImagePath* 參數是目錄。</span><span class="sxs-lookup"><span data-stu-id="f0c5a-121">The *imagePath* parameter is a directory.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="f0c5a-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f0c5a-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="f0c5a-123">*ImagePath* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f0c5a-123">The *imagePath* parameter is **NULL**.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="f0c5a-124"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="f0c5a-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="f0c5a-125">找不到 VM。</span><span class="sxs-lookup"><span data-stu-id="f0c5a-125">The VM could not be found.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="f0c5a-126"><dt>**VM \_\_ \_ \_ 使用中的 E 磁片磁碟機**</dt> <dt>0xA0040727</dt></span><span class="sxs-lookup"><span data-stu-id="f0c5a-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="f0c5a-127">主機 DVD 光碟機或 ISO 映像已附加至此磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f0c5a-127">A host DVD drive or ISO image is already attached to this drive.</span></span><br/>                                  |
| <dl> <span data-ttu-id="f0c5a-128"><dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="f0c5a-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="f0c5a-129">此磁片磁碟機的匯流排位置無效，或磁片磁碟機似乎不是有效的 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="f0c5a-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/> |
| <dl> <span data-ttu-id="f0c5a-130"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f0c5a-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="f0c5a-131">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f0c5a-131">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="f0c5a-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0c5a-132">Requirements</span></span>



| <span data-ttu-id="f0c5a-133">需求</span><span class="sxs-lookup"><span data-stu-id="f0c5a-133">Requirement</span></span> | <span data-ttu-id="f0c5a-134">值</span><span class="sxs-lookup"><span data-stu-id="f0c5a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c5a-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0c5a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c5a-136">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0c5a-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0c5a-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0c5a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c5a-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="f0c5a-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f0c5a-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f0c5a-139">End of client support</span></span><br/>    | <span data-ttu-id="f0c5a-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f0c5a-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f0c5a-141">產品</span><span class="sxs-lookup"><span data-stu-id="f0c5a-141">Product</span></span><br/>                  | <span data-ttu-id="f0c5a-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f0c5a-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f0c5a-143">標頭</span><span class="sxs-lookup"><span data-stu-id="f0c5a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0c5a-144"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0c5a-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f0c5a-145">IID</span><span class="sxs-lookup"><span data-stu-id="f0c5a-145">IID</span></span><br/>                      | <span data-ttu-id="f0c5a-146">IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="f0c5a-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f0c5a-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0c5a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c5a-148">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="f0c5a-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

