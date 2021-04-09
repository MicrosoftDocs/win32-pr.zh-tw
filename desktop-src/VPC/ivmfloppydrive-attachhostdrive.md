---
title: 'IVMFloppyDrive AttachHostDrive 方法 (VPCCOMInterfaces .h) '
description: 將主機上的實體磁片磁碟機附加至虛擬機器中的磁片磁碟機。
ms.assetid: 9be84e06-e38a-419a-be50-dddd0cc6d2dd
keywords:
- AttachHostDrive 方法 Virtual PC
- AttachHostDrive 方法 Virtual PC，IVMFloppyDrive 介面
- IVMFloppyDrive 介面 Virtual PC，AttachHostDrive 方法
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a21785e3e1e4ec77146f048ab4cce018de9d8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025231"
---
# <a name="ivmfloppydriveattachhostdrive-method"></a><span data-ttu-id="5355d-106">IVMFloppyDrive：： AttachHostDrive 方法</span><span class="sxs-lookup"><span data-stu-id="5355d-106">IVMFloppyDrive::AttachHostDrive method</span></span>

<span data-ttu-id="5355d-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="5355d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5355d-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="5355d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5355d-109">將主機上的實體磁片磁碟機附加至虛擬機器中的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="5355d-109">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5355d-110">語法</span><span class="sxs-lookup"><span data-stu-id="5355d-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="5355d-111">參數</span><span class="sxs-lookup"><span data-stu-id="5355d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5355d-112">*r* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5355d-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5355d-113">要連接之主機電腦上的實體磁片磁碟機磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="5355d-113">The drive letter of the physical floppy drive on the host machine to is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5355d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5355d-114">Return value</span></span>

<span data-ttu-id="5355d-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5355d-115">This method can return one of these values.</span></span>



| <span data-ttu-id="5355d-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="5355d-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="5355d-117">Description</span><span class="sxs-lookup"><span data-stu-id="5355d-117">Description</span></span>                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5355d-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5355d-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5355d-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="5355d-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="5355d-120"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="5355d-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="5355d-121">*R* 參數為 **Null**、不是有效的磁片磁碟機，或指定的路徑是空的。</span><span class="sxs-lookup"><span data-stu-id="5355d-121">The *driveLetter* parameter is **NULL**, is not a valid floppy drive, or the given path is empty.</span></span><br/> |
| <dl> <span data-ttu-id="5355d-122"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="5355d-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="5355d-123">此虛擬機器的設定無效或找不到。</span><span class="sxs-lookup"><span data-stu-id="5355d-123">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                       |
| <dl> <span data-ttu-id="5355d-124"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5355d-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="5355d-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5355d-125">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="5355d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5355d-126">Requirements</span></span>



| <span data-ttu-id="5355d-127">需求</span><span class="sxs-lookup"><span data-stu-id="5355d-127">Requirement</span></span> | <span data-ttu-id="5355d-128">值</span><span class="sxs-lookup"><span data-stu-id="5355d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5355d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5355d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5355d-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5355d-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5355d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5355d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5355d-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="5355d-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5355d-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5355d-133">End of client support</span></span><br/>    | <span data-ttu-id="5355d-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5355d-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5355d-135">產品</span><span class="sxs-lookup"><span data-stu-id="5355d-135">Product</span></span><br/>                  | <span data-ttu-id="5355d-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5355d-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5355d-137">標頭</span><span class="sxs-lookup"><span data-stu-id="5355d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5355d-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="5355d-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5355d-139">IID</span><span class="sxs-lookup"><span data-stu-id="5355d-139">IID</span></span><br/>                      | <span data-ttu-id="5355d-140">IID \_ IVMFloppyDrive 定義為661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="5355d-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="5355d-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5355d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5355d-142">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="5355d-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

