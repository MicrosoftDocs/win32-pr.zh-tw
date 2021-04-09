---
title: 'IVMFloppyDriveCollection 專案屬性 (VPCCOMInterfaces .h) '
description: 對應至指定之索引的軟碟物件。
ms.assetid: 068a1f1c-ae84-4689-b68a-ce25b68fc06b
keywords:
- 專案屬性 Virtual PC
- 專案屬性 Virtual PC，IVMFloppyDriveCollection 介面
- IVMFloppyDriveCollection 介面 Virtual PC，Item 屬性
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Item
- IVMFloppyDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315eaea13699d78a75457f39c6c915b30fa2fa9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106062"
---
# <a name="ivmfloppydrivecollectionitem-property"></a><span data-ttu-id="ec89f-106">IVMFloppyDriveCollection：： Item 屬性</span><span class="sxs-lookup"><span data-stu-id="ec89f-106">IVMFloppyDriveCollection::Item property</span></span>

<span data-ttu-id="ec89f-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="ec89f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ec89f-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="ec89f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ec89f-109">抓取對應至指定之索引的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="ec89f-109">Retrieves the floppy object that corresponds to the specified index.</span></span>

<span data-ttu-id="ec89f-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ec89f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec89f-111">語法</span><span class="sxs-lookup"><span data-stu-id="ec89f-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long           index,
  [out, retval] IVMFloppyDrive **floppyDrive
);
```



## <a name="property-value"></a><span data-ttu-id="ec89f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="ec89f-112">Property value</span></span>

<span data-ttu-id="ec89f-113">[**IVMFloppyDrive**](ivmfloppydrive.md)物件。</span><span class="sxs-lookup"><span data-stu-id="ec89f-113">The [**IVMFloppyDrive**](ivmfloppydrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ec89f-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ec89f-114">Error codes</span></span>



| <span data-ttu-id="ec89f-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="ec89f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="ec89f-116">意義</span><span class="sxs-lookup"><span data-stu-id="ec89f-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec89f-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ec89f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ec89f-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="ec89f-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="ec89f-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ec89f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ec89f-120">*FloppyDrive* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ec89f-120">The *floppyDrive* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="ec89f-121"><dt>會 \_E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="ec89f-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="ec89f-122">要求專案的索引未對應到此集合中的專案。</span><span class="sxs-lookup"><span data-stu-id="ec89f-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="ec89f-123"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="ec89f-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="ec89f-124">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="ec89f-124">The configuration is unknown.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="ec89f-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ec89f-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ec89f-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ec89f-126">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="ec89f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec89f-127">Requirements</span></span>



| <span data-ttu-id="ec89f-128">需求</span><span class="sxs-lookup"><span data-stu-id="ec89f-128">Requirement</span></span> | <span data-ttu-id="ec89f-129">值</span><span class="sxs-lookup"><span data-stu-id="ec89f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec89f-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec89f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ec89f-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec89f-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ec89f-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec89f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ec89f-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="ec89f-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ec89f-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ec89f-134">End of client support</span></span><br/>    | <span data-ttu-id="ec89f-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ec89f-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ec89f-136">產品</span><span class="sxs-lookup"><span data-stu-id="ec89f-136">Product</span></span><br/>                  | <span data-ttu-id="ec89f-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ec89f-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ec89f-138">標頭</span><span class="sxs-lookup"><span data-stu-id="ec89f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec89f-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec89f-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ec89f-140">IID</span><span class="sxs-lookup"><span data-stu-id="ec89f-140">IID</span></span><br/>                      | <span data-ttu-id="ec89f-141">IID \_ IVMFloppyDriveCollection 定義為8ba70a25-f698-4ee5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="ec89f-141">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="ec89f-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec89f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec89f-143">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="ec89f-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="ec89f-144">**IVMFloppyDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="ec89f-144">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

