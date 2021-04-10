---
title: 'IVMFloppyDriveCollection Count 屬性 (VPCCOMInterfaces .h) '
description: 此集合中的磁片磁碟機數目。
ms.assetid: d430e5ae-9782-4f88-a5a4-744e79545c7a
keywords:
- Count 屬性 Virtual PC
- Count 屬性 Virtual PC，IVMFloppyDriveCollection 介面
- IVMFloppyDriveCollection 介面 Virtual PC、Count 屬性
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Count
- IVMFloppyDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21b00c13795a633c664cea2c4476d58b346f9108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025457"
---
# <a name="ivmfloppydrivecollectioncount-property"></a><span data-ttu-id="52599-106">IVMFloppyDriveCollection：： Count 屬性</span><span class="sxs-lookup"><span data-stu-id="52599-106">IVMFloppyDriveCollection::Count property</span></span>

<span data-ttu-id="52599-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="52599-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="52599-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="52599-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="52599-109">捕獲此集合中的磁片磁碟機數目。</span><span class="sxs-lookup"><span data-stu-id="52599-109">Retrieves the number of floppy drives in this collection.</span></span>

<span data-ttu-id="52599-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="52599-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52599-111">語法</span><span class="sxs-lookup"><span data-stu-id="52599-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="52599-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="52599-112">Property value</span></span>

<span data-ttu-id="52599-113">磁片磁碟機的數目。</span><span class="sxs-lookup"><span data-stu-id="52599-113">The number of floppy media drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="52599-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="52599-114">Error codes</span></span>



| <span data-ttu-id="52599-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="52599-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="52599-116">意義</span><span class="sxs-lookup"><span data-stu-id="52599-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="52599-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52599-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="52599-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="52599-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="52599-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="52599-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="52599-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="52599-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="52599-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="52599-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="52599-122">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="52599-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="52599-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="52599-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="52599-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="52599-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="52599-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="52599-125">Requirements</span></span>



| <span data-ttu-id="52599-126">需求</span><span class="sxs-lookup"><span data-stu-id="52599-126">Requirement</span></span> | <span data-ttu-id="52599-127">值</span><span class="sxs-lookup"><span data-stu-id="52599-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="52599-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52599-128">Minimum supported client</span></span><br/> | <span data-ttu-id="52599-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52599-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52599-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52599-130">Minimum supported server</span></span><br/> | <span data-ttu-id="52599-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="52599-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="52599-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="52599-132">End of client support</span></span><br/>    | <span data-ttu-id="52599-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52599-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="52599-134">產品</span><span class="sxs-lookup"><span data-stu-id="52599-134">Product</span></span><br/>                  | <span data-ttu-id="52599-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="52599-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="52599-136">標頭</span><span class="sxs-lookup"><span data-stu-id="52599-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="52599-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="52599-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="52599-138">IID</span><span class="sxs-lookup"><span data-stu-id="52599-138">IID</span></span><br/>                      | <span data-ttu-id="52599-139">IID \_ IVMFloppyDriveCollection 定義為8ba70a25-f698-4ee5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="52599-139">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="52599-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52599-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52599-141">**IVMFloppyDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="52599-141">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

