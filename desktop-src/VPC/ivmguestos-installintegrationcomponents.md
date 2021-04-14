---
title: 'IVMGuestOS InstallIntegrationComponents 方法 (VPCCOMInterfaces .h) '
description: 找出最新的整合元件，並將其安裝在客體作業系統中。
ms.assetid: 06f302b3-ec2b-471a-8e2e-095ed6ecbd3d
keywords:
- InstallIntegrationComponents 方法 Virtual PC
- InstallIntegrationComponents 方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，InstallIntegrationComponents 方法
topic_type:
- apiref
api_name:
- IVMGuestOS.InstallIntegrationComponents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879ded1464ebd310e1d1da4e3a952dc086600350
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383946"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a><span data-ttu-id="9df19-106">IVMGuestOS：： InstallIntegrationComponents 方法</span><span class="sxs-lookup"><span data-stu-id="9df19-106">IVMGuestOS::InstallIntegrationComponents method</span></span>

<span data-ttu-id="9df19-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="9df19-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9df19-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="9df19-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9df19-109">找出最新的整合元件，並將其安裝在客體作業系統中。</span><span class="sxs-lookup"><span data-stu-id="9df19-109">Locates and installs the latest Integration Components into the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="9df19-110">語法</span><span class="sxs-lookup"><span data-stu-id="9df19-110">Syntax</span></span>


```C++
HRESULT InstallIntegrationComponents();
```



## <a name="parameters"></a><span data-ttu-id="9df19-111">參數</span><span class="sxs-lookup"><span data-stu-id="9df19-111">Parameters</span></span>

<span data-ttu-id="9df19-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9df19-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9df19-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9df19-113">Return value</span></span>

<span data-ttu-id="9df19-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9df19-114">This method can return one of these values.</span></span>



| <span data-ttu-id="9df19-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="9df19-115">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="9df19-116">Description</span><span class="sxs-lookup"><span data-stu-id="9df19-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9df19-117"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9df19-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="9df19-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="9df19-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="9df19-119"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="9df19-119"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                       | <span data-ttu-id="9df19-120">虛擬機器必須正在執行，才能進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="9df19-120">The virtual machine must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="9df19-121"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="9df19-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="9df19-122">找不到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9df19-122">The virtual machine could not be found.</span></span><br/>                                     |
| <dl> <span data-ttu-id="9df19-123"><dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="9df19-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="9df19-124">虛擬機器沒有空的 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="9df19-124">The virtual machine does not have an empty DVD drive.</span></span><br/>                       |
| <dl> <span data-ttu-id="9df19-125"><dt>**VM \_E \_ 媒體 \_ 卸載 \_ 失敗**</dt> <dt>0xA0040508</dt></span><span class="sxs-lookup"><span data-stu-id="9df19-125"><dt>**VM\_E\_MEDIA\_UNMOUNT\_FAIL**</dt> <dt>0xA0040508</dt></span></span> </dl>                   | <span data-ttu-id="9df19-126">嘗試從虛擬機器 DVD 磁片磁碟機卸載媒體失敗。</span><span class="sxs-lookup"><span data-stu-id="9df19-126">The attempt to unmount the media from the virtual machine DVD drive failed.</span></span><br/> |
| <dl> <span data-ttu-id="9df19-127"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9df19-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="9df19-128">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9df19-128">An unexpected error has occurred.</span></span><br/>                                           |
| <dl> <span data-ttu-id="9df19-129"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="9df19-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="9df19-130">系統找不到整合元件的 ISO 檔案。</span><span class="sxs-lookup"><span data-stu-id="9df19-130">The system cannot find the ISO file for the Integration Components.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="9df19-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="9df19-131">Requirements</span></span>



| <span data-ttu-id="9df19-132">需求</span><span class="sxs-lookup"><span data-stu-id="9df19-132">Requirement</span></span> | <span data-ttu-id="9df19-133">值</span><span class="sxs-lookup"><span data-stu-id="9df19-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9df19-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9df19-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9df19-135">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9df19-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9df19-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9df19-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9df19-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="9df19-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9df19-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9df19-138">End of client support</span></span><br/>    | <span data-ttu-id="9df19-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9df19-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9df19-140">產品</span><span class="sxs-lookup"><span data-stu-id="9df19-140">Product</span></span><br/>                  | <span data-ttu-id="9df19-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9df19-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9df19-142">標頭</span><span class="sxs-lookup"><span data-stu-id="9df19-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="9df19-143"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="9df19-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9df19-144">IID</span><span class="sxs-lookup"><span data-stu-id="9df19-144">IID</span></span><br/>                      | <span data-ttu-id="9df19-145">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="9df19-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="9df19-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9df19-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9df19-147">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="9df19-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

