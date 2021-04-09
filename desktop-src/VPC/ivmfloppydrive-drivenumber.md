---
title: 'IVMFloppyDrive DriveNumber 屬性 (VPCCOMInterfaces .h) '
description: 抓取連接磁片磁碟機之控制器的以零為基底的索引。
ms.assetid: 79a40cad-d280-4c67-9214-0532569e47e4
keywords:
- DriveNumber 屬性 Virtual PC
- DriveNumber 屬性 Virtual PC，IVMFloppyDrive 介面
- IVMFloppyDrive 介面 Virtual PC，DriveNumber 屬性
topic_type:
- apiref
api_name:
- IVMFloppyDrive.DriveNumber
- IVMFloppyDrive.get_DriveNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2f2aeacaf3067515e9e44c58422cd4c9f31fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843724"
---
# <a name="ivmfloppydrivedrivenumber-property"></a><span data-ttu-id="96f83-106">IVMFloppyDrive：:D riveNumber 屬性</span><span class="sxs-lookup"><span data-stu-id="96f83-106">IVMFloppyDrive::DriveNumber property</span></span>

<span data-ttu-id="96f83-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="96f83-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="96f83-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="96f83-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="96f83-109">抓取連接磁片磁碟機之控制器的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="96f83-109">Retrieves the zero-based index of the controller to which the floppy drive is attached.</span></span>

<span data-ttu-id="96f83-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="96f83-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="96f83-111">語法</span><span class="sxs-lookup"><span data-stu-id="96f83-111">Syntax</span></span>


```C++
HRESULT get_DriveNumber(
  [out, retval] long *driveNumber
);
```



## <a name="property-value"></a><span data-ttu-id="96f83-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="96f83-112">Property value</span></span>

<span data-ttu-id="96f83-113">控制器的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="96f83-113">The zero-based index of the controller.</span></span>

## <a name="error-codes"></a><span data-ttu-id="96f83-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="96f83-114">Error codes</span></span>



| <span data-ttu-id="96f83-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="96f83-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="96f83-116">意義</span><span class="sxs-lookup"><span data-stu-id="96f83-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="96f83-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="96f83-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="96f83-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="96f83-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="96f83-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="96f83-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="96f83-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="96f83-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="96f83-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="96f83-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="96f83-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="96f83-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="96f83-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="96f83-123">Requirements</span></span>



| <span data-ttu-id="96f83-124">需求</span><span class="sxs-lookup"><span data-stu-id="96f83-124">Requirement</span></span> | <span data-ttu-id="96f83-125">值</span><span class="sxs-lookup"><span data-stu-id="96f83-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96f83-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96f83-126">Minimum supported client</span></span><br/> | <span data-ttu-id="96f83-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96f83-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96f83-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96f83-128">Minimum supported server</span></span><br/> | <span data-ttu-id="96f83-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="96f83-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="96f83-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="96f83-130">End of client support</span></span><br/>    | <span data-ttu-id="96f83-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="96f83-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="96f83-132">產品</span><span class="sxs-lookup"><span data-stu-id="96f83-132">Product</span></span><br/>                  | <span data-ttu-id="96f83-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="96f83-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="96f83-134">標頭</span><span class="sxs-lookup"><span data-stu-id="96f83-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="96f83-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="96f83-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="96f83-136">IID</span><span class="sxs-lookup"><span data-stu-id="96f83-136">IID</span></span><br/>                      | <span data-ttu-id="96f83-137">IID \_ IVMFloppyDrive 定義為661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="96f83-137">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="96f83-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96f83-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96f83-139">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="96f83-139">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

