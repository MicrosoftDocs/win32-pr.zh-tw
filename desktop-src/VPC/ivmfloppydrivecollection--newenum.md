---
title: 'IVMFloppyDriveCollection _NewEnum 屬性 (VPCCOMInterfaces) '
description: '擷取集合的列舉值。 |IVMFloppyDriveCollection _NewEnum 屬性 (VPCCOMInterfaces) '
ms.assetid: 06de9560-cba9-4c64-907e-83e77781cafc
keywords:
- _NewEnum 屬性 Virtual PC
- _NewEnum 屬性 Virtual PC，IVMFloppyDriveCollection 介面
- IVMFloppyDriveCollection 介面 Virtual PC，_NewEnum 屬性
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection._NewEnum
- IVMFloppyDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db9960ca627b66442e583c6e6bc8fdc89d8d878
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986467"
---
# <a name="ivmfloppydrivecollection_newenum-property"></a><span data-ttu-id="260bf-107">IVMFloppyDriveCollection：： \_ NewEnum 屬性</span><span class="sxs-lookup"><span data-stu-id="260bf-107">IVMFloppyDriveCollection::\_NewEnum property</span></span>

<span data-ttu-id="260bf-108">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="260bf-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="260bf-109">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="260bf-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="260bf-110">擷取集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="260bf-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="260bf-111">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="260bf-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="260bf-112">語法</span><span class="sxs-lookup"><span data-stu-id="260bf-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="260bf-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="260bf-113">Property value</span></span>

<span data-ttu-id="260bf-114">[IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)列舉值。</span><span class="sxs-lookup"><span data-stu-id="260bf-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="260bf-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="260bf-115">Error codes</span></span>



| <span data-ttu-id="260bf-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="260bf-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="260bf-117">意義</span><span class="sxs-lookup"><span data-stu-id="260bf-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="260bf-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="260bf-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="260bf-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="260bf-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="260bf-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="260bf-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="260bf-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="260bf-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="260bf-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="260bf-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="260bf-123">發生意外錯誤。</span><span class="sxs-lookup"><span data-stu-id="260bf-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="260bf-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="260bf-124">Requirements</span></span>



| <span data-ttu-id="260bf-125">需求</span><span class="sxs-lookup"><span data-stu-id="260bf-125">Requirement</span></span> | <span data-ttu-id="260bf-126">值</span><span class="sxs-lookup"><span data-stu-id="260bf-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="260bf-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="260bf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="260bf-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="260bf-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="260bf-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="260bf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="260bf-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="260bf-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="260bf-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="260bf-131">End of client support</span></span><br/>    | <span data-ttu-id="260bf-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="260bf-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="260bf-133">產品</span><span class="sxs-lookup"><span data-stu-id="260bf-133">Product</span></span><br/>                  | <span data-ttu-id="260bf-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="260bf-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="260bf-135">標頭</span><span class="sxs-lookup"><span data-stu-id="260bf-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="260bf-136"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="260bf-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="260bf-137">IID</span><span class="sxs-lookup"><span data-stu-id="260bf-137">IID</span></span><br/>                      | <span data-ttu-id="260bf-138">IID \_ IVMFloppyDriveCollection 定義為8ba70a25-f698-4ee5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="260bf-138">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="260bf-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="260bf-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="260bf-140">**IVMFloppyDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="260bf-140">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

