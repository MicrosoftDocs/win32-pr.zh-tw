---
title: 'IVMDVDDrive 附件屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器中連接至 DVD 光碟機的媒體類型。
ms.assetid: 7ae1714d-e5e9-4f6a-85a6-c0b3c4d21820
keywords:
- 附加屬性虛擬電腦
- 附加屬性 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，附件屬性
topic_type:
- apiref
api_name:
- IVMDVDDrive.Attachment
- IVMDVDDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5c7801e11534249da899797b73b632a7eda307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843952"
---
# <a name="ivmdvddriveattachment-property"></a><span data-ttu-id="ee98d-106">IVMDVDDrive：：附件屬性</span><span class="sxs-lookup"><span data-stu-id="ee98d-106">IVMDVDDrive::Attachment property</span></span>

<span data-ttu-id="ee98d-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="ee98d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ee98d-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="ee98d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ee98d-109">抓取虛擬機器中連接至 DVD 光碟機的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="ee98d-109">Retrieves the type of media attached to the DVD drive within the virtual machine.</span></span>

<span data-ttu-id="ee98d-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ee98d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee98d-111">語法</span><span class="sxs-lookup"><span data-stu-id="ee98d-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMDVDDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="ee98d-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="ee98d-112">Property value</span></span>

<span data-ttu-id="ee98d-113">附加的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="ee98d-113">The attached media type.</span></span> <span data-ttu-id="ee98d-114">如需值的清單，請參閱 [**VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md)。</span><span class="sxs-lookup"><span data-stu-id="ee98d-114">For a list of values, see [**VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="ee98d-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ee98d-115">Error codes</span></span>



| <span data-ttu-id="ee98d-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="ee98d-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="ee98d-117">意義</span><span class="sxs-lookup"><span data-stu-id="ee98d-117">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="ee98d-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ee98d-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="ee98d-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="ee98d-119">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="ee98d-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ee98d-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="ee98d-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ee98d-121">The parameter is **NULL**.</span></span><br/>                  |
| <dl> <span data-ttu-id="ee98d-122"><dt>E \_FAIL</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="ee98d-122"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="ee98d-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ee98d-123">An unexpected error has occurred.</span></span><br/>           |
| <dl> <span data-ttu-id="ee98d-124"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="ee98d-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="ee98d-125">找不到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ee98d-125">The virtual machine could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="ee98d-126"><dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="ee98d-126"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="ee98d-127">此磁片磁碟機的匯流排位置無效。</span><span class="sxs-lookup"><span data-stu-id="ee98d-127">The bus location for this drive is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="ee98d-128"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ee98d-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="ee98d-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ee98d-129">An unexpected error has occurred.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="ee98d-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee98d-130">Requirements</span></span>



| <span data-ttu-id="ee98d-131">需求</span><span class="sxs-lookup"><span data-stu-id="ee98d-131">Requirement</span></span> | <span data-ttu-id="ee98d-132">值</span><span class="sxs-lookup"><span data-stu-id="ee98d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee98d-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee98d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ee98d-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee98d-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ee98d-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee98d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ee98d-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="ee98d-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ee98d-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ee98d-137">End of client support</span></span><br/>    | <span data-ttu-id="ee98d-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ee98d-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ee98d-139">產品</span><span class="sxs-lookup"><span data-stu-id="ee98d-139">Product</span></span><br/>                  | <span data-ttu-id="ee98d-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ee98d-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ee98d-141">標頭</span><span class="sxs-lookup"><span data-stu-id="ee98d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee98d-142"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee98d-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ee98d-143">IID</span><span class="sxs-lookup"><span data-stu-id="ee98d-143">IID</span></span><br/>                      | <span data-ttu-id="ee98d-144">IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="ee98d-144">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="ee98d-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee98d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee98d-146">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="ee98d-146">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

