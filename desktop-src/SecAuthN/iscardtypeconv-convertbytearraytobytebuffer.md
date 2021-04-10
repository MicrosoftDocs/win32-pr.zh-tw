---
description: 將典型的 C/c + + 位元組陣列轉換成 (IStream 物件) 的通用位元組緩衝區。
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: 'ISCardTypeConv：： ConvertByteArrayToByteBuffer 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 406e7aecb7e86802ad67c07669ca199b158ad954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851723"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a><span data-ttu-id="1b185-103">ISCardTypeConv：： ConvertByteArrayToByteBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="1b185-103">ISCardTypeConv::ConvertByteArrayToByteBuffer method</span></span>

<span data-ttu-id="1b185-104">\[**ConvertByteArrayToByteBuffer** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="1b185-104">\[The **ConvertByteArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1b185-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="1b185-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1b185-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="1b185-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1b185-107">**ConvertByteArrayToByteBuffer** 方法會將典型的 C/c + + 位元組陣列轉換成 (**IStream** 物件) 的通用位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1b185-107">The **ConvertByteArrayToByteBuffer** method converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="1b185-108">所建立的位元組緩衝區是透過記憶體區塊對應的資料流程。</span><span class="sxs-lookup"><span data-stu-id="1b185-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="1b185-109">若要存取或管理緩衝區，請使用 **IStream** 介面所提供的方法。</span><span class="sxs-lookup"><span data-stu-id="1b185-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="1b185-110">這個陣列實作為的獨特功能，就是當您呼叫 **IStream：： Release** 方法時，將會為您釋放基礎記憶體。</span><span class="sxs-lookup"><span data-stu-id="1b185-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b185-111">語法</span><span class="sxs-lookup"><span data-stu-id="1b185-111">Syntax</span></span>


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="1b185-112">參數</span><span class="sxs-lookup"><span data-stu-id="1b185-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b185-113">*pbyArray* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b185-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b185-114">要轉換的位元組陣列指標。</span><span class="sxs-lookup"><span data-stu-id="1b185-114">Pointer to the array of bytes to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="1b185-115">*dwArraySize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b185-115">*dwArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b185-116">要轉換之位元組陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="1b185-116">Size of the byte array to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="1b185-117">*ppbyBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1b185-117">*ppbyBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b185-118">要傳回的 **IStream** 物件指標。</span><span class="sxs-lookup"><span data-stu-id="1b185-118">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b185-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b185-119">Return value</span></span>

<span data-ttu-id="1b185-120">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="1b185-120">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="1b185-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1b185-121">Return code</span></span>                                                                                   | <span data-ttu-id="1b185-122">Description</span><span class="sxs-lookup"><span data-stu-id="1b185-122">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1b185-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1b185-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1b185-124">已成功配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="1b185-124">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="1b185-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1b185-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1b185-126">傳遞至函式的一或多個參數發生問題。</span><span class="sxs-lookup"><span data-stu-id="1b185-126">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="1b185-127"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="1b185-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1b185-128">指標類型的參數不正確。</span><span class="sxs-lookup"><span data-stu-id="1b185-128">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="1b185-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1b185-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1b185-130">可用記憶體不足，無法滿足要求。</span><span class="sxs-lookup"><span data-stu-id="1b185-130">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="1b185-131">備註</span><span class="sxs-lookup"><span data-stu-id="1b185-131">Remarks</span></span>

<span data-ttu-id="1b185-132">配置的記憶體是可移動的。</span><span class="sxs-lookup"><span data-stu-id="1b185-132">Memory allocated is movable.</span></span> <span data-ttu-id="1b185-133">使用 **IStream：： Release** 方法釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="1b185-133">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b185-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b185-134">Requirements</span></span>



| <span data-ttu-id="1b185-135">需求</span><span class="sxs-lookup"><span data-stu-id="1b185-135">Requirement</span></span> | <span data-ttu-id="1b185-136">值</span><span class="sxs-lookup"><span data-stu-id="1b185-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b185-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b185-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1b185-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b185-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1b185-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b185-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1b185-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b185-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1b185-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1b185-141">End of client support</span></span><br/>    | <span data-ttu-id="1b185-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1b185-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1b185-143">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1b185-143">End of server support</span></span><br/>    | <span data-ttu-id="1b185-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b185-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1b185-145">標頭</span><span class="sxs-lookup"><span data-stu-id="1b185-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b185-146"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="1b185-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b185-147">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1b185-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="1b185-148"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1b185-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1b185-149">DLL</span><span class="sxs-lookup"><span data-stu-id="1b185-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b185-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b185-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1b185-151">IID</span><span class="sxs-lookup"><span data-stu-id="1b185-151">IID</span></span><br/>                      | <span data-ttu-id="1b185-152">IID \_ ISCardTypeConv 定義為53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1b185-152">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1b185-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b185-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b185-154">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="1b185-154">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="1b185-155">智慧卡傳回值</span><span class="sxs-lookup"><span data-stu-id="1b185-155">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
