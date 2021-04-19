---
title: 'IVMTask Error 屬性 (VPCCOMInterfaces) '
description: 抓取此工作所記錄的錯誤。
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Error 屬性 Virtual PC
- Error 屬性 Virtual PC，IVMTask 介面
- IVMTask 介面 Virtual PC，Error 屬性
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965730"
---
# <a name="ivmtaskerror-property"></a><span data-ttu-id="324b8-106">IVMTask：： Error 屬性</span><span class="sxs-lookup"><span data-stu-id="324b8-106">IVMTask::Error property</span></span>

<span data-ttu-id="324b8-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="324b8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="324b8-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="324b8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="324b8-109">抓取此工作所記錄的錯誤。</span><span class="sxs-lookup"><span data-stu-id="324b8-109">Retrieves the error recorded for this task.</span></span>

<span data-ttu-id="324b8-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="324b8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="324b8-111">語法</span><span class="sxs-lookup"><span data-stu-id="324b8-111">Syntax</span></span>


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a><span data-ttu-id="324b8-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="324b8-112">Property value</span></span>

<span data-ttu-id="324b8-113">記錄的錯誤。</span><span class="sxs-lookup"><span data-stu-id="324b8-113">The recorded error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="324b8-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="324b8-114">Error codes</span></span>

<span data-ttu-id="324b8-115">由其他介面傳回的 [**IVMTask**](ivmtask.md) 實例可能會傳回額外的值。</span><span class="sxs-lookup"><span data-stu-id="324b8-115">Instances of [**IVMTask**](ivmtask.md) returned by other interfaces may return additional values.</span></span> <span data-ttu-id="324b8-116">如需詳細資訊，請參閱傳回 **IVMTask** 實例之方法的檔。</span><span class="sxs-lookup"><span data-stu-id="324b8-116">For details, see the documentation of the methods that return a **IVMTask** instance.</span></span>



| <span data-ttu-id="324b8-117">名稱/值</span><span class="sxs-lookup"><span data-stu-id="324b8-117">Name/value</span></span>                                                                                                                                                                        | <span data-ttu-id="324b8-118">意義</span><span class="sxs-lookup"><span data-stu-id="324b8-118">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="324b8-119"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="324b8-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                           | <span data-ttu-id="324b8-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="324b8-120">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="324b8-121"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="324b8-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                             | <span data-ttu-id="324b8-122">參數值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="324b8-122">The parameter value is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="324b8-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="324b8-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                     | <span data-ttu-id="324b8-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="324b8-124">An unexpected error has occurred.</span></span><br/>                          |
| <dl> <span data-ttu-id="324b8-125"><dt>VM \_E \_ VMVIRTUALPC \_ 較舊的 \_ 版本</dt> <dt>0xA0040952</dt></span><span class="sxs-lookup"><span data-stu-id="324b8-125"><dt>VM\_E\_VMVIRTUALPC\_OLDER\_VERSION</dt> <dt>0xA0040952</dt></span></span> </dl>     | <span data-ttu-id="324b8-126">Virtual PC 2007 和 Windows Virtual PC 皆已安裝。</span><span class="sxs-lookup"><span data-stu-id="324b8-126">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <dl> <span data-ttu-id="324b8-127"><dt>VM \_\_其他 \_ 虛擬化 \_ 軟體</dt> <dt>0xA0040953</dt></span><span class="sxs-lookup"><span data-stu-id="324b8-127"><dt>VM\_E\_OTHER\_VIRTUALIZATION\_SOFTWARE</dt> <dt>0xA0040953</dt></span></span> </dl> | <span data-ttu-id="324b8-128">已安裝其他虛擬化軟體。</span><span class="sxs-lookup"><span data-stu-id="324b8-128">Other virtualization software is installed.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="324b8-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="324b8-129">Requirements</span></span>



| <span data-ttu-id="324b8-130">需求</span><span class="sxs-lookup"><span data-stu-id="324b8-130">Requirement</span></span> | <span data-ttu-id="324b8-131">值</span><span class="sxs-lookup"><span data-stu-id="324b8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="324b8-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="324b8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="324b8-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="324b8-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="324b8-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="324b8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="324b8-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="324b8-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="324b8-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="324b8-136">End of client support</span></span><br/>    | <span data-ttu-id="324b8-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="324b8-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="324b8-138">產品</span><span class="sxs-lookup"><span data-stu-id="324b8-138">Product</span></span><br/>                  | <span data-ttu-id="324b8-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="324b8-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="324b8-140">標頭</span><span class="sxs-lookup"><span data-stu-id="324b8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="324b8-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="324b8-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="324b8-142">IID</span><span class="sxs-lookup"><span data-stu-id="324b8-142">IID</span></span><br/>                      | <span data-ttu-id="324b8-143">IID \_ IVMTask 定義為 ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="324b8-143">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="324b8-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="324b8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="324b8-145">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="324b8-145">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

