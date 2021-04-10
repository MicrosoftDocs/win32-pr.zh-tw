---
title: 'IVMDVDDriveCollection _NewEnum 屬性 (VPCCOMInterfaces) '
description: 抓取 CD/DVD 集合的列舉值。
ms.assetid: e911628b-2a92-41e5-9271-556a297d747d
keywords:
- _NewEnum 屬性 Virtual PC
- _NewEnum 屬性 Virtual PC，IVMDVDDriveCollection 介面
- IVMDVDDriveCollection 介面 Virtual PC，_NewEnum 屬性
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection._NewEnum
- IVMDVDDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dfd0de3aaf6b25808d1afa591b0c2099599e6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934328"
---
# <a name="ivmdvddrivecollection_newenum-property"></a><span data-ttu-id="d0fe2-106">IVMDVDDriveCollection：： \_ NewEnum 屬性</span><span class="sxs-lookup"><span data-stu-id="d0fe2-106">IVMDVDDriveCollection::\_NewEnum property</span></span>

<span data-ttu-id="d0fe2-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="d0fe2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d0fe2-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="d0fe2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d0fe2-109">抓取 CD/DVD 集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="d0fe2-109">Retrieves an enumerator for the CD/DVD collection.</span></span>

<span data-ttu-id="d0fe2-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d0fe2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0fe2-111">語法</span><span class="sxs-lookup"><span data-stu-id="d0fe2-111">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="d0fe2-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="d0fe2-112">Property value</span></span>

<span data-ttu-id="d0fe2-113">[IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)列舉值。</span><span class="sxs-lookup"><span data-stu-id="d0fe2-113">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d0fe2-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d0fe2-114">Error codes</span></span>



| <span data-ttu-id="d0fe2-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="d0fe2-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d0fe2-116">意義</span><span class="sxs-lookup"><span data-stu-id="d0fe2-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d0fe2-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d0fe2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d0fe2-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="d0fe2-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d0fe2-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d0fe2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d0fe2-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d0fe2-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d0fe2-121"><dt>E \_FAIL</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="d0fe2-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="d0fe2-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0fe2-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="d0fe2-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d0fe2-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d0fe2-124">發生意外錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0fe2-124">An unexpected error occurred.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="d0fe2-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0fe2-125">Requirements</span></span>



| <span data-ttu-id="d0fe2-126">需求</span><span class="sxs-lookup"><span data-stu-id="d0fe2-126">Requirement</span></span> | <span data-ttu-id="d0fe2-127">值</span><span class="sxs-lookup"><span data-stu-id="d0fe2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0fe2-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0fe2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d0fe2-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0fe2-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d0fe2-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0fe2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d0fe2-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="d0fe2-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d0fe2-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d0fe2-132">End of client support</span></span><br/>    | <span data-ttu-id="d0fe2-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d0fe2-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d0fe2-134">產品</span><span class="sxs-lookup"><span data-stu-id="d0fe2-134">Product</span></span><br/>                  | <span data-ttu-id="d0fe2-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d0fe2-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d0fe2-136">標頭</span><span class="sxs-lookup"><span data-stu-id="d0fe2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0fe2-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0fe2-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d0fe2-138">IID</span><span class="sxs-lookup"><span data-stu-id="d0fe2-138">IID</span></span><br/>                      | <span data-ttu-id="d0fe2-139">IID \_ IVMDVDDriveCollection 定義為 bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="d0fe2-139">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="d0fe2-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0fe2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0fe2-141">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="d0fe2-141">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

