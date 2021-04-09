---
description: 釋放指向 IStream COM 介面所管理之 HGLOBAL 記憶體區塊的位元組指標。
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: 'ISCardTypeConv：： FreeIStreamMemoryPtr 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 12912b8130ed6e1ccaa995f88069b59e96f57c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693224"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a><span data-ttu-id="26099-103">ISCardTypeConv：： FreeIStreamMemoryPtr 方法</span><span class="sxs-lookup"><span data-stu-id="26099-103">ISCardTypeConv::FreeIStreamMemoryPtr method</span></span>

<span data-ttu-id="26099-104">\[**FreeIStreamMemoryPtr** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="26099-104">\[The **FreeIStreamMemoryPtr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="26099-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="26099-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="26099-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="26099-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="26099-107">**FreeIStreamMemoryPtr** 方法會釋放指向 **IStream** COM 介面所管理之 HGLOBAL 記憶體區塊的位元組指標。</span><span class="sxs-lookup"><span data-stu-id="26099-107">The **FreeIStreamMemoryPtr** method frees the byte pointer pointing to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="26099-108">語法</span><span class="sxs-lookup"><span data-stu-id="26099-108">Syntax</span></span>


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a><span data-ttu-id="26099-109">參數</span><span class="sxs-lookup"><span data-stu-id="26099-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26099-110">*pStrm* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26099-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26099-111">可管理 *pMem* 所指向之記憶體區塊的 **IStream** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="26099-111">Pointer to the **IStream** interface that manages the memory block pointed to by *pMem*.</span></span>

</dd> <dt>

<span data-ttu-id="26099-112">*pMem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26099-112">*pMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26099-113">由 **IStream** 介面管理之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="26099-113">Pointer to the memory block managed by the **IStream** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26099-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="26099-114">Return value</span></span>

<span data-ttu-id="26099-115">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="26099-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="26099-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="26099-116">Return code</span></span>                                                                                   | <span data-ttu-id="26099-117">Description</span><span class="sxs-lookup"><span data-stu-id="26099-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="26099-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="26099-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="26099-119">已成功配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="26099-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="26099-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="26099-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="26099-121">傳遞至函式的一或多個參數發生問題。</span><span class="sxs-lookup"><span data-stu-id="26099-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="26099-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="26099-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="26099-123">指標類型的參數不正確。</span><span class="sxs-lookup"><span data-stu-id="26099-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="26099-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="26099-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="26099-125">可用記憶體不足，無法滿足要求。</span><span class="sxs-lookup"><span data-stu-id="26099-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="26099-126">備註</span><span class="sxs-lookup"><span data-stu-id="26099-126">Remarks</span></span>

<span data-ttu-id="26099-127">這個函式會完整且完全釋放指向 **IStream** 介面所管理之 HGLOBAL 記憶體區塊的位元組指標。</span><span class="sxs-lookup"><span data-stu-id="26099-127">This function completely and cleanly releases the byte pointer pointing to the HGLOBAL memory block managed by the **IStream** interface.</span></span> <span data-ttu-id="26099-128">呼叫 [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)時，會取得位元組指標。</span><span class="sxs-lookup"><span data-stu-id="26099-128">The byte pointer is acquired by a call to [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26099-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="26099-129">Requirements</span></span>



| <span data-ttu-id="26099-130">需求</span><span class="sxs-lookup"><span data-stu-id="26099-130">Requirement</span></span> | <span data-ttu-id="26099-131">值</span><span class="sxs-lookup"><span data-stu-id="26099-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26099-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26099-132">Minimum supported client</span></span><br/> | <span data-ttu-id="26099-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26099-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="26099-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26099-134">Minimum supported server</span></span><br/> | <span data-ttu-id="26099-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26099-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26099-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="26099-136">End of client support</span></span><br/>    | <span data-ttu-id="26099-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="26099-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="26099-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="26099-138">End of server support</span></span><br/>    | <span data-ttu-id="26099-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="26099-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="26099-140">標頭</span><span class="sxs-lookup"><span data-stu-id="26099-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="26099-141"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="26099-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="26099-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="26099-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="26099-143"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="26099-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="26099-144">DLL</span><span class="sxs-lookup"><span data-stu-id="26099-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26099-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26099-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="26099-146">IID</span><span class="sxs-lookup"><span data-stu-id="26099-146">IID</span></span><br/>                      | <span data-ttu-id="26099-147">IID \_ ISCardTypeConv 定義為53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="26099-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="26099-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26099-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26099-149">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="26099-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="26099-150">智慧卡傳回值</span><span class="sxs-lookup"><span data-stu-id="26099-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="26099-151">**GetAtIStreamMemory**</span><span class="sxs-lookup"><span data-stu-id="26099-151">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
