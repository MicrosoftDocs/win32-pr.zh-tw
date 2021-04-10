---
description: 將定義為 SAFEARRAY 的位元組陣列轉換成 (IStream 物件) 的通用位元組緩衝區。
ms.assetid: faa07bb5-cfdb-4181-b86a-f82a9c6b251a
title: 'ISCardTypeConv：： ConvertSafeArrayToByteBuffer 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertSafeArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aa6503f474d96e3c25da3f2780ac43976b6507a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943371"
---
# <a name="iscardtypeconvconvertsafearraytobytebuffer-method"></a><span data-ttu-id="51969-103">ISCardTypeConv：： ConvertSafeArrayToByteBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="51969-103">ISCardTypeConv::ConvertSafeArrayToByteBuffer method</span></span>

<span data-ttu-id="51969-104">\[**ConvertSafeArrayToByteBuffer** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="51969-104">\[The **ConvertSafeArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="51969-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="51969-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="51969-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="51969-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="51969-107">**ConvertSafeArrayToByteBuffer** 方法會將定義為 SAFEARRAY 的位元組陣列轉換成 (**IStream** 物件) 的通用位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="51969-107">The **ConvertSafeArrayToByteBuffer** method converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="51969-108">所建立的位元組緩衝區是透過記憶體區塊對應的資料流程。</span><span class="sxs-lookup"><span data-stu-id="51969-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="51969-109">若要存取或管理緩衝區，請使用 **IStream** 介面所提供的方法。</span><span class="sxs-lookup"><span data-stu-id="51969-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="51969-110">這個陣列實作為的獨特功能，就是當您呼叫 **IStream：： Release** 方法時，將會為您釋放基礎記憶體。</span><span class="sxs-lookup"><span data-stu-id="51969-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="51969-111">語法</span><span class="sxs-lookup"><span data-stu-id="51969-111">Syntax</span></span>


```C++
HRESULT ConvertSafeArrayToByteBuffer(
  [in]  LPSAFEARRAY  pbyArray,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="51969-112">參數</span><span class="sxs-lookup"><span data-stu-id="51969-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51969-113">*pbyArray* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51969-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51969-114">要轉換之 SAFEARRAY 的指標。</span><span class="sxs-lookup"><span data-stu-id="51969-114">Pointer to the SAFEARRAY to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="51969-115">*ppbyBuff* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="51969-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51969-116">要傳回的 **IStream** 物件指標。</span><span class="sxs-lookup"><span data-stu-id="51969-116">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51969-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="51969-117">Return value</span></span>

<span data-ttu-id="51969-118">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="51969-118">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="51969-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="51969-119">Return code</span></span>                                                                                   | <span data-ttu-id="51969-120">Description</span><span class="sxs-lookup"><span data-stu-id="51969-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="51969-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="51969-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="51969-122">已成功配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="51969-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="51969-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="51969-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="51969-124">傳遞至函式的一或多個參數發生問題。</span><span class="sxs-lookup"><span data-stu-id="51969-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="51969-125"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="51969-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="51969-126">指標類型的參數不正確。</span><span class="sxs-lookup"><span data-stu-id="51969-126">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="51969-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="51969-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="51969-128">可用記憶體不足，無法滿足要求。</span><span class="sxs-lookup"><span data-stu-id="51969-128">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="51969-129">備註</span><span class="sxs-lookup"><span data-stu-id="51969-129">Remarks</span></span>

<span data-ttu-id="51969-130">配置的記憶體是可移動的。</span><span class="sxs-lookup"><span data-stu-id="51969-130">Memory allocated is moveable.</span></span> <span data-ttu-id="51969-131">使用 **IStream：： Release** 方法釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="51969-131">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="51969-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="51969-132">Requirements</span></span>



| <span data-ttu-id="51969-133">需求</span><span class="sxs-lookup"><span data-stu-id="51969-133">Requirement</span></span> | <span data-ttu-id="51969-134">值</span><span class="sxs-lookup"><span data-stu-id="51969-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51969-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51969-135">Minimum supported client</span></span><br/> | <span data-ttu-id="51969-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51969-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="51969-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51969-137">Minimum supported server</span></span><br/> | <span data-ttu-id="51969-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51969-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="51969-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="51969-139">End of client support</span></span><br/>    | <span data-ttu-id="51969-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="51969-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="51969-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="51969-141">End of server support</span></span><br/>    | <span data-ttu-id="51969-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="51969-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="51969-143">標頭</span><span class="sxs-lookup"><span data-stu-id="51969-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="51969-144"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="51969-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="51969-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="51969-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="51969-146"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="51969-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="51969-147">DLL</span><span class="sxs-lookup"><span data-stu-id="51969-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51969-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51969-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="51969-149">IID</span><span class="sxs-lookup"><span data-stu-id="51969-149">IID</span></span><br/>                      | <span data-ttu-id="51969-150">IID \_ ISCardTypeConv 定義為53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="51969-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="51969-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51969-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51969-152">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="51969-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="51969-153">智慧卡傳回值</span><span class="sxs-lookup"><span data-stu-id="51969-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
