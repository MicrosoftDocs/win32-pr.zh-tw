---
description: 建立對應至 IStream (IByteBuffer) 物件的通用位元組緩衝區。
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: 'ISCardTypeConv：： CreateByteBuffer 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ab69c8061d2e2740e652e29b2fe6407574fe7076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026811"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a><span data-ttu-id="4a716-103">ISCardTypeConv：： CreateByteBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="4a716-103">ISCardTypeConv::CreateByteBuffer method</span></span>

<span data-ttu-id="4a716-104">\[**CreateByteBuffer** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="4a716-104">\[The **CreateByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4a716-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="4a716-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4a716-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="4a716-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4a716-107">**CreateByteBuffer** 方法會建立對應至 **IStream** ([**IByteBuffer**](ibytebuffer.md)) 物件中的通用位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4a716-107">The **CreateByteBuffer** method creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span>

<span data-ttu-id="4a716-108">所建立的位元組緩衝區是透過記憶體區塊對應的資料流程。</span><span class="sxs-lookup"><span data-stu-id="4a716-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="4a716-109">若要存取或管理緩衝區，請使用 **IStream** 介面所提供的方法。</span><span class="sxs-lookup"><span data-stu-id="4a716-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="4a716-110">這個陣列實作為的獨特功能，就是當您呼叫 **IStream：： Release** 方法時，將會為您釋放基礎記憶體。</span><span class="sxs-lookup"><span data-stu-id="4a716-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a716-111">語法</span><span class="sxs-lookup"><span data-stu-id="4a716-111">Syntax</span></span>


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="4a716-112">參數</span><span class="sxs-lookup"><span data-stu-id="4a716-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a716-113">*dwAllocSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a716-113">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a716-114">要為數組配置的記憶體大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4a716-114">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="4a716-115">*ppbyBuff* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4a716-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a716-116">要傳回的 IStream 物件指標。</span><span class="sxs-lookup"><span data-stu-id="4a716-116">Pointer to the IStream object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a716-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a716-117">Return value</span></span>

<span data-ttu-id="4a716-118">可能的傳回值如下：</span><span class="sxs-lookup"><span data-stu-id="4a716-118">The possible return values are the following:</span></span>



| <span data-ttu-id="4a716-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4a716-119">Return code</span></span>                                                                                   | <span data-ttu-id="4a716-120">Description</span><span class="sxs-lookup"><span data-stu-id="4a716-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a716-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4a716-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4a716-122">已成功配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="4a716-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4a716-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4a716-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4a716-124">傳遞至函式的一或多個參數發生問題。</span><span class="sxs-lookup"><span data-stu-id="4a716-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="4a716-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4a716-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4a716-126">可用記憶體不足，無法滿足要求。</span><span class="sxs-lookup"><span data-stu-id="4a716-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="4a716-127">備註</span><span class="sxs-lookup"><span data-stu-id="4a716-127">Remarks</span></span>

<span data-ttu-id="4a716-128">配置的記憶體是可移動的。</span><span class="sxs-lookup"><span data-stu-id="4a716-128">Memory allocated is movable.</span></span> <span data-ttu-id="4a716-129">使用 **IStream：： Release** 方法釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="4a716-129">Use the **IStream::Release** method to free the memory.</span></span>

<span data-ttu-id="4a716-130">若要建立一般 C/c + + 位元組陣列，請呼叫 [**CreateByteArray**](iscardtypeconv-createbytearray.md)。</span><span class="sxs-lookup"><span data-stu-id="4a716-130">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="4a716-131">若要建立不帶正負號字元的自動化 SAFEARRAY (bytes) ，請呼叫 [**CreateSafeArray**](iscardtypeconv-createsafearray.md)。</span><span class="sxs-lookup"><span data-stu-id="4a716-131">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a716-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a716-132">Requirements</span></span>



| <span data-ttu-id="4a716-133">需求</span><span class="sxs-lookup"><span data-stu-id="4a716-133">Requirement</span></span> | <span data-ttu-id="4a716-134">值</span><span class="sxs-lookup"><span data-stu-id="4a716-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a716-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a716-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4a716-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a716-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4a716-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a716-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4a716-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a716-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4a716-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4a716-139">End of client support</span></span><br/>    | <span data-ttu-id="4a716-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a716-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4a716-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="4a716-141">End of server support</span></span><br/>    | <span data-ttu-id="4a716-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4a716-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4a716-143">標頭</span><span class="sxs-lookup"><span data-stu-id="4a716-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a716-144"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a716-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a716-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4a716-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="4a716-146"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4a716-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4a716-147">DLL</span><span class="sxs-lookup"><span data-stu-id="4a716-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a716-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a716-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4a716-149">IID</span><span class="sxs-lookup"><span data-stu-id="4a716-149">IID</span></span><br/>                      | <span data-ttu-id="4a716-150">IID \_ ISCardTypeConv 定義為53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4a716-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4a716-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a716-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a716-152">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="4a716-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="4a716-153">智慧卡傳回值</span><span class="sxs-lookup"><span data-stu-id="4a716-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="4a716-154">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="4a716-154">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="4a716-155">**CreateSafeArray**</span><span class="sxs-lookup"><span data-stu-id="4a716-155">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
