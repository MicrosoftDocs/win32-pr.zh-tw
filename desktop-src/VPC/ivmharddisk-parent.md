---
title: 'IVMHardDisk 父屬性 (VPCCOMInterfaces) '
description: 差異虛擬硬碟的父系。
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- 父屬性虛擬電腦
- 父屬性 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，Parent 屬性
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933883"
---
# <a name="ivmharddiskparent-property"></a><span data-ttu-id="99dab-106">IVMHardDisk：:P 不用屬性</span><span class="sxs-lookup"><span data-stu-id="99dab-106">IVMHardDisk::Parent property</span></span>

<span data-ttu-id="99dab-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="99dab-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="99dab-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="99dab-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="99dab-109">抓取並設定差異虛擬硬碟的父系。</span><span class="sxs-lookup"><span data-stu-id="99dab-109">Retrieves and sets the parent of the differencing virtual hard disk.</span></span>

<span data-ttu-id="99dab-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="99dab-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="99dab-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="99dab-111">Syntax</span></span>


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a><span data-ttu-id="99dab-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="99dab-112">Property value</span></span>

<span data-ttu-id="99dab-113">設定與父硬碟影像相關聯的 [**IVMHardDisk**](ivmharddisk.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="99dab-113">Sets the [**IVMHardDisk**](ivmharddisk.md) object associated with the parent hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="99dab-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="99dab-114">Error codes</span></span>



| <span data-ttu-id="99dab-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="99dab-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="99dab-116">意義</span><span class="sxs-lookup"><span data-stu-id="99dab-116">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="99dab-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="99dab-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="99dab-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="99dab-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="99dab-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="99dab-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="99dab-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="99dab-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="99dab-121"><dt>S \_FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="99dab-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="99dab-122">這不是差異硬碟，因此沒有父系。</span><span class="sxs-lookup"><span data-stu-id="99dab-122">This is not a differencing hard disk, so it has no parent.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="99dab-123"><dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="99dab-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="99dab-124">系統找不到父虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="99dab-124">The system could not find the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="99dab-125"><dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑) </dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="99dab-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="99dab-126">系統找不到父虛擬硬碟檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="99dab-126">The system could not find the path to the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="99dab-127"><dt>VM \_E \_ HD \_ 映射 \_ 開啟 \_ 失敗</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="99dab-127"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="99dab-128">嘗試開啟目前的硬碟影像檔案時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="99dab-128">An error occurred while attempting to open the current hard disk image file.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="99dab-129"><dt>VM \_電子 \_ HD \_ 影像 \_ 存取</dt> <dt>0xA0040681</dt></span><span class="sxs-lookup"><span data-stu-id="99dab-129"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="99dab-130">嘗試存取目前的硬碟影像檔案時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="99dab-130">An error occurred while attempting to access the current hard disk image file.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="99dab-131"><dt>VM \_E \_ 父系 \_ 子系 \_ 識別碼 \_ 不符</dt> <dt>0xA0040685</dt></span><span class="sxs-lookup"><span data-stu-id="99dab-131"><dt>VM\_E\_PARENT\_CHILD\_ID\_MISMATCH</dt> <dt>0xA0040685</dt></span></span> </dl>            | <span data-ttu-id="99dab-132">*父* 參數所找出的虛擬硬碟映射與子磁片映射的識別碼不同。</span><span class="sxs-lookup"><span data-stu-id="99dab-132">The virtual hard disk image located by the *parent* parameter does not have the same ID as the child disk image.</span></span> <span data-ttu-id="99dab-133">請確定 *父* 參數所找到的父虛擬硬碟映射，與用來建立差異虛擬硬碟映射的映射相同。</span><span class="sxs-lookup"><span data-stu-id="99dab-133">Make sure the parent virtual hard disk image located by the *parent* parameter is the same image used to create the differencing virtual hard disk image.</span></span><br/> |
| <dl> <span data-ttu-id="99dab-134"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="99dab-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="99dab-135">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="99dab-135">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="99dab-136">備註</span><span class="sxs-lookup"><span data-stu-id="99dab-136">Remarks</span></span>

<span data-ttu-id="99dab-137">這個屬性只適用于差異硬碟映射。</span><span class="sxs-lookup"><span data-stu-id="99dab-137">This property is only valid with differencing hard disk images.</span></span>

## <a name="requirements"></a><span data-ttu-id="99dab-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="99dab-138">Requirements</span></span>



| <span data-ttu-id="99dab-139">需求</span><span class="sxs-lookup"><span data-stu-id="99dab-139">Requirement</span></span> | <span data-ttu-id="99dab-140">值</span><span class="sxs-lookup"><span data-stu-id="99dab-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="99dab-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99dab-141">Minimum supported client</span></span><br/> | <span data-ttu-id="99dab-142">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99dab-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="99dab-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99dab-143">Minimum supported server</span></span><br/> | <span data-ttu-id="99dab-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="99dab-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="99dab-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="99dab-145">End of client support</span></span><br/>    | <span data-ttu-id="99dab-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="99dab-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="99dab-147">產品</span><span class="sxs-lookup"><span data-stu-id="99dab-147">Product</span></span><br/>                  | <span data-ttu-id="99dab-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="99dab-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="99dab-149">標頭</span><span class="sxs-lookup"><span data-stu-id="99dab-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="99dab-150"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="99dab-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="99dab-151">IID</span><span class="sxs-lookup"><span data-stu-id="99dab-151">IID</span></span><br/>                      | <span data-ttu-id="99dab-152">IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="99dab-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="99dab-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99dab-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99dab-154">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="99dab-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

