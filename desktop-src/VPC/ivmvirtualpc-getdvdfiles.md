---
title: 'IVMVirtualPC GetDVDFiles 方法 (VPCCOMInterfaces .h) '
description: 捕獲已知 DVD 檔案的陣列。
ms.assetid: 9fe2191f-c5c0-464d-a190-29b2aba69682
keywords:
- GetDVDFiles 方法 Virtual PC
- GetDVDFiles 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，GetDVDFiles 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetDVDFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a91d7f0d65d1f62feb21d41bd9b27bf6ce112ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966524"
---
# <a name="ivmvirtualpcgetdvdfiles-method"></a><span data-ttu-id="e66a9-106">IVMVirtualPC：： GetDVDFiles 方法</span><span class="sxs-lookup"><span data-stu-id="e66a9-106">IVMVirtualPC::GetDVDFiles method</span></span>

<span data-ttu-id="e66a9-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="e66a9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e66a9-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="e66a9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e66a9-109">捕獲已知 DVD 檔案的陣列。</span><span class="sxs-lookup"><span data-stu-id="e66a9-109">Retrieves an array of known DVD files.</span></span>

## <a name="syntax"></a><span data-ttu-id="e66a9-110">語法</span><span class="sxs-lookup"><span data-stu-id="e66a9-110">Syntax</span></span>


```C++
HRESULT GetDVDFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outDVDFileList
);
```



## <a name="parameters"></a><span data-ttu-id="e66a9-111">參數</span><span class="sxs-lookup"><span data-stu-id="e66a9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e66a9-112">*inAdditionalSearchPaths* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e66a9-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e66a9-113">將會搜尋這些路徑，以及在 [**IVMVirtualPC：： SearchPaths**](ivmvirtualpc-searchpaths.md) 屬性中設定的路徑。</span><span class="sxs-lookup"><span data-stu-id="e66a9-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="e66a9-114">*outDVDFileList* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="e66a9-114">*outDVDFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e66a9-115">在指定搜尋路徑中找到的虛擬 DVD 檔案陣列。</span><span class="sxs-lookup"><span data-stu-id="e66a9-115">An array of virtual DVD files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e66a9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e66a9-116">Return value</span></span>

<span data-ttu-id="e66a9-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e66a9-117">This method can return one of these values.</span></span>



| <span data-ttu-id="e66a9-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="e66a9-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="e66a9-119">Description</span><span class="sxs-lookup"><span data-stu-id="e66a9-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e66a9-120"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e66a9-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="e66a9-121">作業成功。</span><span class="sxs-lookup"><span data-stu-id="e66a9-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e66a9-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e66a9-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="e66a9-123">*OutDVDFileList* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e66a9-123">The *outDVDFileList* parameter is **NULL**.</span></span><br/>                                          |
| <dl> <span data-ttu-id="e66a9-124"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e66a9-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="e66a9-125">*InAdditionalSearchPaths* 參數不是字串的陣列。</span><span class="sxs-lookup"><span data-stu-id="e66a9-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="e66a9-126"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e66a9-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="e66a9-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e66a9-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="e66a9-128"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="e66a9-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="e66a9-129">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="e66a9-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e66a9-130">備註</span><span class="sxs-lookup"><span data-stu-id="e66a9-130">Remarks</span></span>

<span data-ttu-id="e66a9-131">用來取出檔案陣列的搜尋路徑將包含先前由 [**IVMVirtualPC：： SearchPaths**](ivmvirtualpc-searchpaths.md) 所設定的檔案，以及 *inAdditionalSearchPaths* 參數所指定的路徑，以及整合元件模組的安裝程式位置。</span><span class="sxs-lookup"><span data-stu-id="e66a9-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter and the installer location for the integration components module.</span></span>

## <a name="requirements"></a><span data-ttu-id="e66a9-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="e66a9-132">Requirements</span></span>



| <span data-ttu-id="e66a9-133">需求</span><span class="sxs-lookup"><span data-stu-id="e66a9-133">Requirement</span></span> | <span data-ttu-id="e66a9-134">值</span><span class="sxs-lookup"><span data-stu-id="e66a9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e66a9-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e66a9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e66a9-136">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e66a9-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e66a9-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e66a9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e66a9-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="e66a9-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e66a9-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e66a9-139">End of client support</span></span><br/>    | <span data-ttu-id="e66a9-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e66a9-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e66a9-141">產品</span><span class="sxs-lookup"><span data-stu-id="e66a9-141">Product</span></span><br/>                  | <span data-ttu-id="e66a9-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e66a9-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e66a9-143">標頭</span><span class="sxs-lookup"><span data-stu-id="e66a9-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e66a9-144"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="e66a9-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e66a9-145">IID</span><span class="sxs-lookup"><span data-stu-id="e66a9-145">IID</span></span><br/>                      | <span data-ttu-id="e66a9-146">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="e66a9-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e66a9-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e66a9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e66a9-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="e66a9-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

