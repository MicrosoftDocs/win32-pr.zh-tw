---
title: 'IVMDVDDrive AttachHostDrive 方法 (VPCCOMInterfaces .h) '
description: 將主機磁片磁碟機連接到虛擬機器中的 DVD 光碟機。
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- AttachHostDrive 方法 Virtual PC
- AttachHostDrive 方法 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，AttachHostDrive 方法
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012afcdc0b88aa5b77f1d85cc5becff1e70853f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966339"
---
# <a name="ivmdvddriveattachhostdrive-method"></a><span data-ttu-id="3ec2b-106">IVMDVDDrive：： AttachHostDrive 方法</span><span class="sxs-lookup"><span data-stu-id="3ec2b-106">IVMDVDDrive::AttachHostDrive method</span></span>

<span data-ttu-id="3ec2b-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="3ec2b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3ec2b-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="3ec2b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3ec2b-109">將主機磁片磁碟機連接到虛擬機器中的 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="3ec2b-109">Attaches a host drive to the DVD drive within the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec2b-110">語法</span><span class="sxs-lookup"><span data-stu-id="3ec2b-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="3ec2b-111">參數</span><span class="sxs-lookup"><span data-stu-id="3ec2b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ec2b-112">*r* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ec2b-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec2b-113">要附加之主機磁片磁碟機的字母。</span><span class="sxs-lookup"><span data-stu-id="3ec2b-113">The letter of the host drive that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ec2b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ec2b-114">Return value</span></span>

<span data-ttu-id="3ec2b-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3ec2b-115">This method can return one of these values.</span></span>



| <span data-ttu-id="3ec2b-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="3ec2b-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="3ec2b-117">Description</span><span class="sxs-lookup"><span data-stu-id="3ec2b-117">Description</span></span>                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ec2b-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3ec2b-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="3ec2b-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="3ec2b-119">The operation was successful.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="3ec2b-120"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3ec2b-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="3ec2b-121">未指定任何磁碟機號，或指定的磁碟機號無效。</span><span class="sxs-lookup"><span data-stu-id="3ec2b-121">No drive letter was specified, or the specified drive letter is invalid.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="3ec2b-122"><dt>**E \_FAIL**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="3ec2b-122"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="3ec2b-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3ec2b-123">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="3ec2b-124"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="3ec2b-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="3ec2b-125">找不到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3ec2b-125">The virtual machine could not be found.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="3ec2b-126"><dt>**VM \_\_ \_ \_ 使用中的 E 磁片磁碟機**</dt> <dt>0xA0040727</dt></span><span class="sxs-lookup"><span data-stu-id="3ec2b-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="3ec2b-127">主機 DVD 光碟機或 ISO 映像已連結到虛擬機器中的這個磁片磁碟機，或指定的主機磁片磁碟機已在另一部虛擬機器中使用。</span><span class="sxs-lookup"><span data-stu-id="3ec2b-127">A host DVD drive or ISO image is already attached to this drive within the virtual machine, or the specified host drive is already in use within another virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="3ec2b-128"><dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="3ec2b-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="3ec2b-129">此磁片磁碟機的匯流排位置無效，或磁片磁碟機似乎不是有效的 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="3ec2b-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="3ec2b-130"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3ec2b-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="3ec2b-131">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3ec2b-131">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="3ec2b-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ec2b-132">Requirements</span></span>



| <span data-ttu-id="3ec2b-133">需求</span><span class="sxs-lookup"><span data-stu-id="3ec2b-133">Requirement</span></span> | <span data-ttu-id="3ec2b-134">值</span><span class="sxs-lookup"><span data-stu-id="3ec2b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec2b-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ec2b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec2b-136">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ec2b-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ec2b-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ec2b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec2b-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="3ec2b-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3ec2b-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3ec2b-139">End of client support</span></span><br/>    | <span data-ttu-id="3ec2b-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3ec2b-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3ec2b-141">產品</span><span class="sxs-lookup"><span data-stu-id="3ec2b-141">Product</span></span><br/>                  | <span data-ttu-id="3ec2b-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3ec2b-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3ec2b-143">標頭</span><span class="sxs-lookup"><span data-stu-id="3ec2b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ec2b-144"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ec2b-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3ec2b-145">IID</span><span class="sxs-lookup"><span data-stu-id="3ec2b-145">IID</span></span><br/>                      | <span data-ttu-id="3ec2b-146">IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="3ec2b-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3ec2b-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ec2b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec2b-148">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="3ec2b-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

