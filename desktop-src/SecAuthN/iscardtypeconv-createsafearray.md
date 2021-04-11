---
description: 建立不帶正負號字元的自動化 SAFEARRAY， (位元組) 。
ms.assetid: 67cc8cd1-95be-4498-ac25-6c418089af27
title: 'ISCardTypeConv：： CreateSafeArray 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bc27a3f50f0740eca178787fd021f76c9b6729e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111980"
---
# <a name="iscardtypeconvcreatesafearray-method"></a><span data-ttu-id="9820d-103">ISCardTypeConv：： CreateSafeArray 方法</span><span class="sxs-lookup"><span data-stu-id="9820d-103">ISCardTypeConv::CreateSafeArray method</span></span>

<span data-ttu-id="9820d-104">\[**CreateSafeArray** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="9820d-104">\[The **CreateSafeArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9820d-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="9820d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9820d-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="9820d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9820d-107">**CreateSafeArray** 方法會建立不帶正負號字元的自動化 SAFEARRAY (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="9820d-107">The **CreateSafeArray** method creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span>

## <a name="syntax"></a><span data-ttu-id="9820d-108">語法</span><span class="sxs-lookup"><span data-stu-id="9820d-108">Syntax</span></span>


```C++
HRESULT CreateSafeArray(
  [in]  UINT        nAllocSize,
  [out] LPSAFEARRAY *ppArray
);
```



## <a name="parameters"></a><span data-ttu-id="9820d-109">參數</span><span class="sxs-lookup"><span data-stu-id="9820d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9820d-110">*nAllocSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9820d-110">*nAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9820d-111">要為數組配置的記憶體大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9820d-111">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="9820d-112">*ppArray* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9820d-112">*ppArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9820d-113">要傳回之 SAFEARRAY 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="9820d-113">Pointer to the SAFEARRAY object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9820d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9820d-114">Return value</span></span>

<span data-ttu-id="9820d-115">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="9820d-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="9820d-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9820d-116">Return code</span></span>                                                                                   | <span data-ttu-id="9820d-117">Description</span><span class="sxs-lookup"><span data-stu-id="9820d-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9820d-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9820d-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9820d-119">已成功配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="9820d-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="9820d-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9820d-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9820d-121">傳遞至函式的一或多個參數發生問題。</span><span class="sxs-lookup"><span data-stu-id="9820d-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="9820d-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9820d-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9820d-123">可用記憶體不足，無法滿足要求。</span><span class="sxs-lookup"><span data-stu-id="9820d-123">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="9820d-124">備註</span><span class="sxs-lookup"><span data-stu-id="9820d-124">Remarks</span></span>

<span data-ttu-id="9820d-125">若要建立一般 C/c + + 位元組陣列，請呼叫 [**CreateByteArray**](iscardtypeconv-createbytearray.md)。</span><span class="sxs-lookup"><span data-stu-id="9820d-125">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="9820d-126">若要建立對應至 **IStream** ([**IByteBuffer**](ibytebuffer.md)) 物件的通用位元組緩衝區，請呼叫 [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="9820d-126">To create a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object, call [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9820d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="9820d-127">Requirements</span></span>



| <span data-ttu-id="9820d-128">需求</span><span class="sxs-lookup"><span data-stu-id="9820d-128">Requirement</span></span> | <span data-ttu-id="9820d-129">值</span><span class="sxs-lookup"><span data-stu-id="9820d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9820d-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9820d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9820d-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9820d-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9820d-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9820d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9820d-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9820d-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9820d-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9820d-134">End of client support</span></span><br/>    | <span data-ttu-id="9820d-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9820d-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9820d-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9820d-136">End of server support</span></span><br/>    | <span data-ttu-id="9820d-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9820d-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9820d-138">標頭</span><span class="sxs-lookup"><span data-stu-id="9820d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9820d-139"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="9820d-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="9820d-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9820d-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="9820d-141"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9820d-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9820d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9820d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9820d-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9820d-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9820d-144">IID</span><span class="sxs-lookup"><span data-stu-id="9820d-144">IID</span></span><br/>                      | <span data-ttu-id="9820d-145">IID \_ ISCardTypeConv 定義為53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="9820d-145">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9820d-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9820d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9820d-147">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="9820d-147">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="9820d-148">智慧卡傳回值</span><span class="sxs-lookup"><span data-stu-id="9820d-148">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="9820d-149">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="9820d-149">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="9820d-150">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="9820d-150">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)
</dt> </dl>

 

 
