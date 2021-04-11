---
title: 'IVMDVDDrive ImageFile 屬性 (VPCCOMInterfaces .h) '
description: 抓取此裝置之影像檔案的完整路徑。
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- 虛擬 PC 的 ImageFile 屬性
- ImageFile 屬性 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，ImageFile 屬性
topic_type:
- apiref
api_name:
- IVMDVDDrive.ImageFile
- IVMDVDDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c71ed5328e41a72c9896147c6dcd824b2bd2ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844204"
---
# <a name="ivmdvddriveimagefile-property"></a><span data-ttu-id="a4129-106">IVMDVDDrive：： ImageFile 屬性</span><span class="sxs-lookup"><span data-stu-id="a4129-106">IVMDVDDrive::ImageFile property</span></span>

<span data-ttu-id="a4129-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="a4129-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a4129-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="a4129-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a4129-109">抓取此裝置之影像檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a4129-109">Retrieves the full path of the image file set for this device.</span></span>

<span data-ttu-id="a4129-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="a4129-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4129-111">語法</span><span class="sxs-lookup"><span data-stu-id="a4129-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a><span data-ttu-id="a4129-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="a4129-112">Property value</span></span>

<span data-ttu-id="a4129-113">影像檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a4129-113">The full path to the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a4129-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a4129-114">Error codes</span></span>



| <span data-ttu-id="a4129-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="a4129-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="a4129-116">意義</span><span class="sxs-lookup"><span data-stu-id="a4129-116">Meaning</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a4129-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a4129-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="a4129-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="a4129-118">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="a4129-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a4129-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="a4129-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a4129-120">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="a4129-121"><dt>E \_FAIL</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="a4129-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="a4129-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a4129-122">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="a4129-123"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="a4129-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="a4129-124">找不到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a4129-124">The virtual machine could not be found.</span></span><br/>                        |
| <dl> <span data-ttu-id="a4129-125"><dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="a4129-125"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="a4129-126">此磁片磁碟機的匯流排位置無效。</span><span class="sxs-lookup"><span data-stu-id="a4129-126">The bus location for this drive is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="a4129-127"><dt>VM \_E \_ 媒體有 \_ 錯誤的 \_ 類型</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="a4129-127"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="a4129-128">由此 DVD 光碟機所捕捉的媒體不是 ISO 影像檔案。</span><span class="sxs-lookup"><span data-stu-id="a4129-128">The media captured by this DVD drive is not an ISO image file.</span></span><br/> |
| <dl> <span data-ttu-id="a4129-129"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a4129-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="a4129-130">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a4129-130">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="a4129-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4129-131">Requirements</span></span>



| <span data-ttu-id="a4129-132">需求</span><span class="sxs-lookup"><span data-stu-id="a4129-132">Requirement</span></span> | <span data-ttu-id="a4129-133">值</span><span class="sxs-lookup"><span data-stu-id="a4129-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4129-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4129-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a4129-135">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4129-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4129-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4129-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a4129-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="a4129-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a4129-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a4129-138">End of client support</span></span><br/>    | <span data-ttu-id="a4129-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a4129-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a4129-140">產品</span><span class="sxs-lookup"><span data-stu-id="a4129-140">Product</span></span><br/>                  | <span data-ttu-id="a4129-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a4129-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a4129-142">標頭</span><span class="sxs-lookup"><span data-stu-id="a4129-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4129-143"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="a4129-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a4129-144">IID</span><span class="sxs-lookup"><span data-stu-id="a4129-144">IID</span></span><br/>                      | <span data-ttu-id="a4129-145">IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="a4129-145">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="a4129-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4129-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4129-147">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="a4129-147">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

