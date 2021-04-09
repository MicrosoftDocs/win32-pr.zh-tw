---
title: 'IVMFloppyDrive ImageFile 屬性 (VPCCOMInterfaces .h) '
description: 抓取連接軟碟磁碟機之影像檔案的完整路徑。
ms.assetid: fc87e438-e5d4-494d-8ac2-27a4312ee81d
keywords:
- 虛擬 PC 的 ImageFile 屬性
- ImageFile 屬性 Virtual PC，IVMFloppyDrive 介面
- IVMFloppyDrive 介面 Virtual PC，ImageFile 屬性
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ImageFile
- IVMFloppyDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa18c4a1da3137613e0106f828f59805e5615384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025308"
---
# <a name="ivmfloppydriveimagefile-property"></a><span data-ttu-id="43920-106">IVMFloppyDrive：： ImageFile 屬性</span><span class="sxs-lookup"><span data-stu-id="43920-106">IVMFloppyDrive::ImageFile property</span></span>

<span data-ttu-id="43920-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="43920-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="43920-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="43920-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="43920-109">抓取連接軟碟磁碟機之影像檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="43920-109">Retrieves the full path of the image file to which the floppy drive is attached.</span></span>

<span data-ttu-id="43920-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="43920-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="43920-111">語法</span><span class="sxs-lookup"><span data-stu-id="43920-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imageFile
);
```



## <a name="property-value"></a><span data-ttu-id="43920-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="43920-112">Property value</span></span>

<span data-ttu-id="43920-113">影像檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="43920-113">The full path of the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="43920-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="43920-114">Error codes</span></span>



| <span data-ttu-id="43920-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="43920-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="43920-116">意義</span><span class="sxs-lookup"><span data-stu-id="43920-116">Meaning</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43920-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="43920-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="43920-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="43920-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="43920-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="43920-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="43920-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="43920-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="43920-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="43920-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="43920-122">此虛擬機器的設定無效或找不到。</span><span class="sxs-lookup"><span data-stu-id="43920-122">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="43920-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="43920-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="43920-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="43920-124">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="requirements"></a><span data-ttu-id="43920-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="43920-125">Requirements</span></span>



| <span data-ttu-id="43920-126">需求</span><span class="sxs-lookup"><span data-stu-id="43920-126">Requirement</span></span> | <span data-ttu-id="43920-127">值</span><span class="sxs-lookup"><span data-stu-id="43920-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="43920-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43920-128">Minimum supported client</span></span><br/> | <span data-ttu-id="43920-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43920-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43920-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43920-130">Minimum supported server</span></span><br/> | <span data-ttu-id="43920-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="43920-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="43920-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="43920-132">End of client support</span></span><br/>    | <span data-ttu-id="43920-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="43920-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="43920-134">產品</span><span class="sxs-lookup"><span data-stu-id="43920-134">Product</span></span><br/>                  | <span data-ttu-id="43920-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="43920-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="43920-136">標頭</span><span class="sxs-lookup"><span data-stu-id="43920-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="43920-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="43920-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="43920-138">IID</span><span class="sxs-lookup"><span data-stu-id="43920-138">IID</span></span><br/>                      | <span data-ttu-id="43920-139">IID \_ IVMFloppyDrive 定義為661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="43920-139">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="43920-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43920-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43920-141">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="43920-141">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

