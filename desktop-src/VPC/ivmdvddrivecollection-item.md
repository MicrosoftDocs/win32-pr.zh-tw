---
title: 'IVMDVDDriveCollection 專案屬性 (VPCCOMInterfaces .h) '
description: 抓取對應至指定之索引的 CD 或 DVD 光碟機物件。
ms.assetid: ecc94eea-9ddc-46c8-87e2-e67aca83eecc
keywords:
- 專案屬性 Virtual PC
- 專案屬性 Virtual PC，IVMDVDDriveCollection 介面
- IVMDVDDriveCollection 介面 Virtual PC，Item 屬性
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Item
- IVMDVDDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cc631ab6d4de3ab65071bf2b8692236f3ae03ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025056"
---
# <a name="ivmdvddrivecollectionitem-property"></a><span data-ttu-id="f7163-106">IVMDVDDriveCollection：： Item 屬性</span><span class="sxs-lookup"><span data-stu-id="f7163-106">IVMDVDDriveCollection::Item property</span></span>

<span data-ttu-id="f7163-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="f7163-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f7163-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="f7163-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f7163-109">抓取對應至指定之索引的 CD 或 DVD 光碟機物件。</span><span class="sxs-lookup"><span data-stu-id="f7163-109">Retrieves the CD or DVD drive object that corresponds to the specified index.</span></span>

<span data-ttu-id="f7163-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="f7163-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7163-111">語法</span><span class="sxs-lookup"><span data-stu-id="f7163-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long        index,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="property-value"></a><span data-ttu-id="f7163-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="f7163-112">Property value</span></span>

<span data-ttu-id="f7163-113">[**IVMDVDDrive**](ivmdvddrive.md)物件。</span><span class="sxs-lookup"><span data-stu-id="f7163-113">The [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f7163-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f7163-114">Error codes</span></span>



| <span data-ttu-id="f7163-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="f7163-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f7163-116">意義</span><span class="sxs-lookup"><span data-stu-id="f7163-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7163-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f7163-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f7163-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="f7163-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="f7163-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f7163-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f7163-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f7163-120">The parameter is **NULL**.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="f7163-121"><dt>E \_FAIL</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="f7163-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="f7163-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f7163-122">An unexpected error has occurred.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="f7163-123"><dt>會 \_E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="f7163-123"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="f7163-124">要求專案的索引未對應到此集合中的專案。</span><span class="sxs-lookup"><span data-stu-id="f7163-124">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="f7163-125"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="f7163-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f7163-126">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="f7163-126">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="f7163-127"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f7163-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f7163-128">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f7163-128">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="f7163-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7163-129">Requirements</span></span>



| <span data-ttu-id="f7163-130">需求</span><span class="sxs-lookup"><span data-stu-id="f7163-130">Requirement</span></span> | <span data-ttu-id="f7163-131">值</span><span class="sxs-lookup"><span data-stu-id="f7163-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7163-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7163-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f7163-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7163-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7163-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7163-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f7163-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="f7163-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f7163-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f7163-136">End of client support</span></span><br/>    | <span data-ttu-id="f7163-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f7163-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f7163-138">產品</span><span class="sxs-lookup"><span data-stu-id="f7163-138">Product</span></span><br/>                  | <span data-ttu-id="f7163-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f7163-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f7163-140">標頭</span><span class="sxs-lookup"><span data-stu-id="f7163-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7163-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7163-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f7163-142">IID</span><span class="sxs-lookup"><span data-stu-id="f7163-142">IID</span></span><br/>                      | <span data-ttu-id="f7163-143">IID \_ IVMDVDDriveCollection 定義為 bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="f7163-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="f7163-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7163-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7163-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="f7163-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="f7163-146">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="f7163-146">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

