---
title: 'IVMDVDDrive HostDriveLetter 屬性 (VPCCOMInterfaces .h) '
description: 為此裝置設定之主機磁片磁碟機的字母。
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- HostDriveLetter 屬性 Virtual PC
- HostDriveLetter 屬性 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，HostDriveLetter 屬性
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60d2599b8fb73e727100111dc37d29a9d13c5d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685806"
---
# <a name="ivmdvddrivehostdriveletter-property"></a><span data-ttu-id="5afe7-106">IVMDVDDrive：： HostDriveLetter 屬性</span><span class="sxs-lookup"><span data-stu-id="5afe7-106">IVMDVDDrive::HostDriveLetter property</span></span>

<span data-ttu-id="5afe7-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="5afe7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5afe7-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="5afe7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5afe7-109">抓取此裝置的主機磁片磁碟機的字母。</span><span class="sxs-lookup"><span data-stu-id="5afe7-109">Retrieves the letter of the host drive set for this device.</span></span>

<span data-ttu-id="5afe7-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5afe7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5afe7-111">語法</span><span class="sxs-lookup"><span data-stu-id="5afe7-111">Syntax</span></span>


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a><span data-ttu-id="5afe7-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="5afe7-112">Property value</span></span>

<span data-ttu-id="5afe7-113">磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="5afe7-113">The drive letter.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5afe7-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5afe7-114">Error codes</span></span>



| <span data-ttu-id="5afe7-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="5afe7-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="5afe7-116">意義</span><span class="sxs-lookup"><span data-stu-id="5afe7-116">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="5afe7-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5afe7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="5afe7-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="5afe7-118">The operation was successful.</span></span><br/>                             |
| <dl> <span data-ttu-id="5afe7-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="5afe7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="5afe7-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5afe7-120">The parameter is **NULL**.</span></span><br/>                                |
| <dl> <span data-ttu-id="5afe7-121"><dt>E \_FAIL</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="5afe7-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="5afe7-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5afe7-122">An unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="5afe7-123"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="5afe7-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="5afe7-124">找不到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5afe7-124">The virtual machine could not be found.</span></span><br/>                   |
| <dl> <span data-ttu-id="5afe7-125"><dt>VM \_E \_ 媒體有 \_ 錯誤的 \_ 類型</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="5afe7-125"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="5afe7-126">由此 DVD 光碟機所捕捉的媒體不是主機磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="5afe7-126">The media captured by this DVD drive is not a host drive.</span></span><br/> |
| <dl> <span data-ttu-id="5afe7-127"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5afe7-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="5afe7-128">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5afe7-128">An unexpected error has occurred.</span></span><br/>                         |



## <a name="requirements"></a><span data-ttu-id="5afe7-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5afe7-129">Requirements</span></span>



| <span data-ttu-id="5afe7-130">需求</span><span class="sxs-lookup"><span data-stu-id="5afe7-130">Requirement</span></span> | <span data-ttu-id="5afe7-131">值</span><span class="sxs-lookup"><span data-stu-id="5afe7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5afe7-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5afe7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5afe7-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5afe7-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5afe7-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5afe7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5afe7-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="5afe7-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5afe7-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5afe7-136">End of client support</span></span><br/>    | <span data-ttu-id="5afe7-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5afe7-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5afe7-138">產品</span><span class="sxs-lookup"><span data-stu-id="5afe7-138">Product</span></span><br/>                  | <span data-ttu-id="5afe7-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5afe7-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5afe7-140">標頭</span><span class="sxs-lookup"><span data-stu-id="5afe7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5afe7-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="5afe7-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5afe7-142">IID</span><span class="sxs-lookup"><span data-stu-id="5afe7-142">IID</span></span><br/>                      | <span data-ttu-id="5afe7-143">IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="5afe7-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="5afe7-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5afe7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5afe7-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="5afe7-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

