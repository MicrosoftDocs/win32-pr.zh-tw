---
title: 'IVMFloppyDrive AttachImage 方法 (VPCCOMInterfaces .h) '
description: 將主機上的軟碟媒體映射連接到虛擬機器的磁片磁碟機。
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- AttachImage 方法 Virtual PC
- AttachImage 方法 Virtual PC，IVMFloppyDrive 介面
- IVMFloppyDrive 介面 Virtual PC，AttachImage 方法
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8821a6d9bdae979f45477d1fe2ba666eb6da10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934227"
---
# <a name="ivmfloppydriveattachimage-method"></a><span data-ttu-id="43ef5-106">IVMFloppyDrive：： AttachImage 方法</span><span class="sxs-lookup"><span data-stu-id="43ef5-106">IVMFloppyDrive::AttachImage method</span></span>

<span data-ttu-id="43ef5-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="43ef5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="43ef5-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="43ef5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="43ef5-109">將主機上的軟碟媒體映射連接到虛擬機器的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="43ef5-109">Attaches a floppy media image on the host to the floppy drive of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ef5-110">語法</span><span class="sxs-lookup"><span data-stu-id="43ef5-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a><span data-ttu-id="43ef5-111">參數</span><span class="sxs-lookup"><span data-stu-id="43ef5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43ef5-112">*mediaImagePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43ef5-112">*mediaImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ef5-113">要附加之軟碟媒體映射的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="43ef5-113">The full path to the floppy media image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43ef5-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="43ef5-114">Return value</span></span>

<span data-ttu-id="43ef5-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="43ef5-115">This method can return one of these values.</span></span>



| <span data-ttu-id="43ef5-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="43ef5-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="43ef5-117">Description</span><span class="sxs-lookup"><span data-stu-id="43ef5-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43ef5-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="43ef5-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="43ef5-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="43ef5-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="43ef5-120"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="43ef5-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="43ef5-121">*MediaImagePath* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="43ef5-121">The *mediaImagePath* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="43ef5-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="43ef5-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="43ef5-123">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="43ef5-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="43ef5-124"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="43ef5-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="43ef5-125">沒有足夠的記憶體可完成此要求。</span><span class="sxs-lookup"><span data-stu-id="43ef5-125">There is not enough memory available to complete this request.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="43ef5-126"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="43ef5-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="43ef5-127">*MediaImagePath* 參數所指定的路徑太長。</span><span class="sxs-lookup"><span data-stu-id="43ef5-127">The path specified by the *mediaImagePath* parameter is too long.</span></span> <span data-ttu-id="43ef5-128">路徑必須小於 **最大 \_ 路徑** (260) 個字元。</span><span class="sxs-lookup"><span data-stu-id="43ef5-128">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="43ef5-129"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="43ef5-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="43ef5-130">*MediaImagePath* 參數包含不正確字元 (" \* ？ <>/ \| "： ") 之一。</span><span class="sxs-lookup"><span data-stu-id="43ef5-130">The *mediaImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="43ef5-131"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="43ef5-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="43ef5-132">*MediaImagePath* 參數會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="43ef5-132">The *mediaImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="43ef5-133">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="43ef5-133">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="43ef5-134"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="43ef5-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="43ef5-135">此虛擬機器的設定無效或找不到。</span><span class="sxs-lookup"><span data-stu-id="43ef5-135">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="43ef5-136"><dt>**VM \_E \_ 映射 \_ 捕捉 \_ 失敗**</dt> <dt>0xA00400650</dt></span><span class="sxs-lookup"><span data-stu-id="43ef5-136"><dt>**VM\_E\_IMAGE\_CAPTURE\_FAIL**</dt> <dt>0xA00400650</dt></span></span> </dl>                  | <span data-ttu-id="43ef5-137">無法捕獲指定的影像檔案。</span><span class="sxs-lookup"><span data-stu-id="43ef5-137">The image file specified could not be captured.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="43ef5-138"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="43ef5-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="43ef5-139">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="43ef5-139">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="43ef5-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="43ef5-140">Requirements</span></span>



| <span data-ttu-id="43ef5-141">需求</span><span class="sxs-lookup"><span data-stu-id="43ef5-141">Requirement</span></span> | <span data-ttu-id="43ef5-142">值</span><span class="sxs-lookup"><span data-stu-id="43ef5-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="43ef5-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43ef5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="43ef5-144">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43ef5-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43ef5-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43ef5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="43ef5-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="43ef5-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="43ef5-147">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="43ef5-147">End of client support</span></span><br/>    | <span data-ttu-id="43ef5-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="43ef5-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="43ef5-149">產品</span><span class="sxs-lookup"><span data-stu-id="43ef5-149">Product</span></span><br/>                  | <span data-ttu-id="43ef5-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="43ef5-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="43ef5-151">標頭</span><span class="sxs-lookup"><span data-stu-id="43ef5-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="43ef5-152"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="43ef5-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="43ef5-153">IID</span><span class="sxs-lookup"><span data-stu-id="43ef5-153">IID</span></span><br/>                      | <span data-ttu-id="43ef5-154">IID \_ IVMFloppyDrive 定義為661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="43ef5-154">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="43ef5-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43ef5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ef5-156">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="43ef5-156">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

