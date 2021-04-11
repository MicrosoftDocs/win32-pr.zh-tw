---
description: 取得由 IStream COM 介面管理的 HGLOBAL 記憶體區塊的位元組指標。
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: 'ISCardTypeConv：： GetAtIStreamMemory 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bdd828921f18c3d06edd2d41da189260a4ed4394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689695"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a><span data-ttu-id="bd25a-103">ISCardTypeConv：： GetAtIStreamMemory 方法</span><span class="sxs-lookup"><span data-stu-id="bd25a-103">ISCardTypeConv::GetAtIStreamMemory method</span></span>

<span data-ttu-id="bd25a-104">\[**GetAtIStreamMemory** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="bd25a-104">\[The **GetAtIStreamMemory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bd25a-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="bd25a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bd25a-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="bd25a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bd25a-107">**GetAtIStreamMemory** 方法會取得 **IStream** COM 介面所管理之 HGLOBAL 記憶體區塊的位元組指標。</span><span class="sxs-lookup"><span data-stu-id="bd25a-107">The **GetAtIStreamMemory** method acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span>

<span data-ttu-id="bd25a-108">這是取得 **IStream** 下記憶體的方法，不需要取得記憶體區塊的 sizeof 值（以位元組為單位），並使用 **IStream** 介面將位元組讀入暫存位元組陣列中。</span><span class="sxs-lookup"><span data-stu-id="bd25a-108">This is a way to get at the memory under the **IStream** without having to get the sizeof value for the memory block in bytes and read the bytes into a temporary byte array using the **IStream** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd25a-109">語法</span><span class="sxs-lookup"><span data-stu-id="bd25a-109">Syntax</span></span>


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a><span data-ttu-id="bd25a-110">參數</span><span class="sxs-lookup"><span data-stu-id="bd25a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd25a-111">*pStrm* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd25a-111">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd25a-112">可管理 HGLOBAL 記憶體區塊的 **IStream** COM 介面指標。</span><span class="sxs-lookup"><span data-stu-id="bd25a-112">A pointer to the **IStream** COM interface that manages the HGLOBAL memory block.</span></span>

</dd> <dt>

<span data-ttu-id="bd25a-113">*ppMem* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bd25a-113">*ppMem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd25a-114">如果成功，則為 HGLOBAL 記憶體區塊第一個位元組的指標;否則，如果作業失敗，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="bd25a-114">A pointer to the first byte of the HGLOBAL memory block if successful; else, **NULL** if operation fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd25a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd25a-115">Return value</span></span>

<span data-ttu-id="bd25a-116">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="bd25a-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="bd25a-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bd25a-117">Return code</span></span>                                                                                   | <span data-ttu-id="bd25a-118">Description</span><span class="sxs-lookup"><span data-stu-id="bd25a-118">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd25a-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bd25a-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bd25a-120">已成功配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="bd25a-120">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="bd25a-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bd25a-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bd25a-122">傳遞至函式的一或多個參數發生問題。</span><span class="sxs-lookup"><span data-stu-id="bd25a-122">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="bd25a-123"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="bd25a-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bd25a-124">指標類型的參數不正確。</span><span class="sxs-lookup"><span data-stu-id="bd25a-124">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="bd25a-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bd25a-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bd25a-126">可用記憶體不足，無法滿足要求。</span><span class="sxs-lookup"><span data-stu-id="bd25a-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="bd25a-127">備註</span><span class="sxs-lookup"><span data-stu-id="bd25a-127">Remarks</span></span>

<span data-ttu-id="bd25a-128">每個取得的 *ppMem* 指標都會遞增 **IStream** 參考計數。</span><span class="sxs-lookup"><span data-stu-id="bd25a-128">The **IStream** reference count will be incremented for each *ppMem* pointer acquired.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd25a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd25a-129">Requirements</span></span>



| <span data-ttu-id="bd25a-130">需求</span><span class="sxs-lookup"><span data-stu-id="bd25a-130">Requirement</span></span> | <span data-ttu-id="bd25a-131">值</span><span class="sxs-lookup"><span data-stu-id="bd25a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd25a-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd25a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bd25a-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd25a-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bd25a-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd25a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bd25a-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd25a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd25a-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="bd25a-136">End of client support</span></span><br/>    | <span data-ttu-id="bd25a-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bd25a-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bd25a-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="bd25a-138">End of server support</span></span><br/>    | <span data-ttu-id="bd25a-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bd25a-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bd25a-140">標頭</span><span class="sxs-lookup"><span data-stu-id="bd25a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd25a-141"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="bd25a-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd25a-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bd25a-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd25a-143"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bd25a-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bd25a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="bd25a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd25a-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd25a-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bd25a-146">IID</span><span class="sxs-lookup"><span data-stu-id="bd25a-146">IID</span></span><br/>                      | <span data-ttu-id="bd25a-147">IID \_ ISCardTypeConv 定義為53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="bd25a-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="bd25a-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd25a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd25a-149">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="bd25a-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="bd25a-150">智慧卡傳回值</span><span class="sxs-lookup"><span data-stu-id="bd25a-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
