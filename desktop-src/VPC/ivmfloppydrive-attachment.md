---
title: 'IVMFloppyDrive 附件屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器中連接至軟碟磁碟機的媒體類型。
ms.assetid: 0b7e43ac-de56-4c4b-82e6-75877aea06f2
keywords:
- 附加屬性虛擬電腦
- 附加屬性 Virtual PC，IVMFloppyDrive 介面
- IVMFloppyDrive 介面 Virtual PC，附件屬性
topic_type:
- apiref
api_name:
- IVMFloppyDrive.Attachment
- IVMFloppyDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44814148baf27672f30b8e3c5015d841aaaba4b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965303"
---
# <a name="ivmfloppydriveattachment-property"></a><span data-ttu-id="fd50c-106">IVMFloppyDrive：：附件屬性</span><span class="sxs-lookup"><span data-stu-id="fd50c-106">IVMFloppyDrive::Attachment property</span></span>

<span data-ttu-id="fd50c-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="fd50c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd50c-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="fd50c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd50c-109">抓取虛擬機器 (VM) 中連接至磁片磁碟機的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="fd50c-109">Retrieves the type of media attached to the floppy drive in the virtual machine (VM).</span></span>

<span data-ttu-id="fd50c-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="fd50c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd50c-111">語法</span><span class="sxs-lookup"><span data-stu-id="fd50c-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMFloppyDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="fd50c-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="fd50c-112">Property value</span></span>

<span data-ttu-id="fd50c-113">媒體的類型。</span><span class="sxs-lookup"><span data-stu-id="fd50c-113">The type of media.</span></span> <span data-ttu-id="fd50c-114">如需值的清單，請參閱 [**VMFloppyDriveAttachmentType**](vmfloppydriveattachmenttype.md)。</span><span class="sxs-lookup"><span data-stu-id="fd50c-114">For a list of values, see [**VMFloppyDriveAttachmentType**](vmfloppydriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="fd50c-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="fd50c-115">Error codes</span></span>



| <span data-ttu-id="fd50c-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="fd50c-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="fd50c-117">意義</span><span class="sxs-lookup"><span data-stu-id="fd50c-117">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd50c-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fd50c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="fd50c-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="fd50c-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="fd50c-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fd50c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="fd50c-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fd50c-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="fd50c-122"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="fd50c-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="fd50c-123">此 VM 的設定無效或找不到。</span><span class="sxs-lookup"><span data-stu-id="fd50c-123">The configuration for this VM is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="fd50c-124"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fd50c-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="fd50c-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="fd50c-125">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="fd50c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd50c-126">Requirements</span></span>



| <span data-ttu-id="fd50c-127">需求</span><span class="sxs-lookup"><span data-stu-id="fd50c-127">Requirement</span></span> | <span data-ttu-id="fd50c-128">值</span><span class="sxs-lookup"><span data-stu-id="fd50c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd50c-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd50c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fd50c-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd50c-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd50c-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd50c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fd50c-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="fd50c-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd50c-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="fd50c-133">End of client support</span></span><br/>    | <span data-ttu-id="fd50c-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd50c-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd50c-135">產品</span><span class="sxs-lookup"><span data-stu-id="fd50c-135">Product</span></span><br/>                  | <span data-ttu-id="fd50c-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd50c-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd50c-137">標頭</span><span class="sxs-lookup"><span data-stu-id="fd50c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd50c-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd50c-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fd50c-139">IID</span><span class="sxs-lookup"><span data-stu-id="fd50c-139">IID</span></span><br/>                      | <span data-ttu-id="fd50c-140">IID \_ IVMFloppyDrive 定義為661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="fd50c-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="fd50c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd50c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd50c-142">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="fd50c-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

