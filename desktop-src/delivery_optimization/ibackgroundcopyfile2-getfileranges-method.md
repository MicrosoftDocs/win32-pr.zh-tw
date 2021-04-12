---
title: 'IBackgroundCopyFile2 GetFileRanges 方法 (>deliveryoptimization .h) '
description: 抓取您要從遠端檔案下載的範圍。
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- GetFileRanges 方法
- GetFileRanges 方法，IBackgroundCopyFile2 介面
- IBackgroundCopyFile2 介面，GetFileRanges 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37352176ca460587343bed0a154ee992c12c2fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384513"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a><span data-ttu-id="7ced3-106">IBackgroundCopyFile2：： GetFileRanges 方法</span><span class="sxs-lookup"><span data-stu-id="7ced3-106">IBackgroundCopyFile2::GetFileRanges method</span></span>

<span data-ttu-id="7ced3-107">抓取您要從遠端檔案下載的範圍。</span><span class="sxs-lookup"><span data-stu-id="7ced3-107">Retrieves the ranges that you want to download from the remote file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ced3-108">語法</span><span class="sxs-lookup"><span data-stu-id="7ced3-108">Syntax</span></span>


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a><span data-ttu-id="7ced3-109">參數</span><span class="sxs-lookup"><span data-stu-id="7ced3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ced3-110">*RangeCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="7ced3-110">*RangeCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ced3-111">*範圍* 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="7ced3-111">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="7ced3-112">*範圍* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7ced3-112">*Ranges* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ced3-113">[**BG_FILE_RANGE**](bg-file-range.md)結構的陣列，指定要下載的範圍。</span><span class="sxs-lookup"><span data-stu-id="7ced3-113">Array of [**BG_FILE_RANGE**](bg-file-range.md) structures that specify the ranges to download.</span></span> <span data-ttu-id="7ced3-114">完成時，請呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 函式來釋放 *範圍*。</span><span class="sxs-lookup"><span data-stu-id="7ced3-114">When done, call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *Ranges*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ced3-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ced3-115">Return value</span></span>

<span data-ttu-id="7ced3-116">這個方法會傳回下列傳回值以及其他值。</span><span class="sxs-lookup"><span data-stu-id="7ced3-116">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="7ced3-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7ced3-117">Return code</span></span>                                                                              | <span data-ttu-id="7ced3-118">Description</span><span class="sxs-lookup"><span data-stu-id="7ced3-118">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ced3-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="7ced3-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="7ced3-120">Success</span><span class="sxs-lookup"><span data-stu-id="7ced3-120">Success</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="7ced3-121"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="7ced3-121"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="7ced3-122">未指定範圍，或作業為上傳或上傳回復作業。</span><span class="sxs-lookup"><span data-stu-id="7ced3-122">No ranges were specified or the job is an upload or upload-reply job.</span></span> <span data-ttu-id="7ced3-123">*RangeCount* 設定為零，而 *範圍* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7ced3-123">*RangeCount* is set to zero and *Ranges* is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7ced3-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ced3-124">Requirements</span></span>



| <span data-ttu-id="7ced3-125">需求</span><span class="sxs-lookup"><span data-stu-id="7ced3-125">Requirement</span></span> | <span data-ttu-id="7ced3-126">值</span><span class="sxs-lookup"><span data-stu-id="7ced3-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ced3-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ced3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7ced3-128">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ced3-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7ced3-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ced3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7ced3-130">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ced3-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7ced3-131">標頭</span><span class="sxs-lookup"><span data-stu-id="7ced3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ced3-132"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ced3-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ced3-133">Idl</span><span class="sxs-lookup"><span data-stu-id="7ced3-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ced3-134"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ced3-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="7ced3-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="7ced3-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ced3-136"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ced3-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="7ced3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7ced3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ced3-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ced3-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="7ced3-139">IID</span><span class="sxs-lookup"><span data-stu-id="7ced3-139">IID</span></span><br/>                      | <span data-ttu-id="7ced3-140">IID_IBackgroundCopyFile2 定義為83e81b93-0873-474d-8a8c-f2018b1a939c</span><span class="sxs-lookup"><span data-stu-id="7ced3-140">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="7ced3-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ced3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ced3-142">**BG_FILE_RANGE**</span><span class="sxs-lookup"><span data-stu-id="7ced3-142">**BG_FILE_RANGE**</span></span>](bg-file-range.md)
</dt> <dt>

[<span data-ttu-id="7ced3-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="7ced3-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

