---
description: 將位元組 (IStream 物件) 的通用緩衝區轉換為一般的 C/c + + 位元組陣列。
ms.assetid: f5b14096-d848-4de9-a5c3-bb60af9044a2
title: 'ISCardTypeConv：： ConvertByteBufferToByteArray 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7eed6758373aebf08863669b5b81909fca1c0840
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194204"
---
# <a name="iscardtypeconvconvertbytebuffertobytearray-method"></a><span data-ttu-id="f2be7-103">ISCardTypeConv：： ConvertByteBufferToByteArray 方法</span><span class="sxs-lookup"><span data-stu-id="f2be7-103">ISCardTypeConv::ConvertByteBufferToByteArray method</span></span>

<span data-ttu-id="f2be7-104">\[**ConvertByteBufferToByteArray** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="f2be7-104">\[The **ConvertByteBufferToByteArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f2be7-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="f2be7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f2be7-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="f2be7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f2be7-107">**ConvertByteBufferToByteArray** 方法會將位元組 (**IStream** 物件) 的通用緩衝區轉換為一般的 c/c + + 位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="f2be7-107">The **ConvertByteBufferToByteArray** method converts a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2be7-108">語法</span><span class="sxs-lookup"><span data-stu-id="f2be7-108">Syntax</span></span>


```C++
HRESULT ConvertByteBufferToByteArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPBYTEARRAY  *ppArray
);
```



## <a name="parameters"></a><span data-ttu-id="f2be7-109">參數</span><span class="sxs-lookup"><span data-stu-id="f2be7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2be7-110">*pbyBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2be7-110">*pbyBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2be7-111">要轉換之 **IStream** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="f2be7-111">Pointer to the **IStream** object to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="f2be7-112">*ppArray* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f2be7-112">*ppArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2be7-113">要傳回的位元組陣列指標。</span><span class="sxs-lookup"><span data-stu-id="f2be7-113">Pointer to the array of bytes to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2be7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2be7-114">Return value</span></span>

<span data-ttu-id="f2be7-115">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="f2be7-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="f2be7-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f2be7-116">Return code</span></span>                                                                                   | <span data-ttu-id="f2be7-117">Description</span><span class="sxs-lookup"><span data-stu-id="f2be7-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2be7-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f2be7-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f2be7-119">已成功配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="f2be7-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f2be7-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f2be7-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f2be7-121">傳遞至函式的一或多個參數發生問題。</span><span class="sxs-lookup"><span data-stu-id="f2be7-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="f2be7-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="f2be7-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f2be7-123">指標類型的參數不正確。</span><span class="sxs-lookup"><span data-stu-id="f2be7-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="f2be7-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f2be7-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f2be7-125">可用記憶體不足，無法滿足要求。</span><span class="sxs-lookup"><span data-stu-id="f2be7-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="f2be7-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2be7-126">Requirements</span></span>



| <span data-ttu-id="f2be7-127">需求</span><span class="sxs-lookup"><span data-stu-id="f2be7-127">Requirement</span></span> | <span data-ttu-id="f2be7-128">值</span><span class="sxs-lookup"><span data-stu-id="f2be7-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2be7-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2be7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f2be7-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2be7-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f2be7-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2be7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f2be7-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2be7-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2be7-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f2be7-133">End of client support</span></span><br/>    | <span data-ttu-id="f2be7-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f2be7-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f2be7-135">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f2be7-135">End of server support</span></span><br/>    | <span data-ttu-id="f2be7-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2be7-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f2be7-137">標頭</span><span class="sxs-lookup"><span data-stu-id="f2be7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2be7-138"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="f2be7-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2be7-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f2be7-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2be7-140"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f2be7-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f2be7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f2be7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2be7-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2be7-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2be7-143">IID</span><span class="sxs-lookup"><span data-stu-id="f2be7-143">IID</span></span><br/>                      | <span data-ttu-id="f2be7-144">IID \_ ISCardTypeConv 定義為53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f2be7-144">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f2be7-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2be7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2be7-146">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="f2be7-146">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="f2be7-147">智慧卡傳回值</span><span class="sxs-lookup"><span data-stu-id="f2be7-147">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
