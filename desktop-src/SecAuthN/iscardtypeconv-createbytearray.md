---
description: 建立一般的 C/c + + 位元組陣列。
ms.assetid: 915e8cca-2a0f-409e-a6df-54fa73bdc305
title: 'ISCardTypeConv：： CreateByteArray 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae253af1b24433987baf66364519a3761f7e0365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115612"
---
# <a name="iscardtypeconvcreatebytearray-method"></a><span data-ttu-id="2aaf1-103">ISCardTypeConv：： CreateByteArray 方法</span><span class="sxs-lookup"><span data-stu-id="2aaf1-103">ISCardTypeConv::CreateByteArray method</span></span>

<span data-ttu-id="2aaf1-104">\[**CreateByteArray** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="2aaf1-104">\[The **CreateByteArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2aaf1-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="2aaf1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2aaf1-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="2aaf1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2aaf1-107">**CreateByteArray** 方法會建立一般的 c/c + + 位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="2aaf1-107">The **CreateByteArray** method creates a typical C/C++ byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aaf1-108">語法</span><span class="sxs-lookup"><span data-stu-id="2aaf1-108">Syntax</span></span>


```C++
HRESULT CreateByteArray(
  [in]  DWORD  dwAllocSize,
  [out] LPBYTE *ppbyArray
);
```



## <a name="parameters"></a><span data-ttu-id="2aaf1-109">參數</span><span class="sxs-lookup"><span data-stu-id="2aaf1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aaf1-110">*dwAllocSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2aaf1-110">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aaf1-111">要為數組配置的記憶體) 大小 (以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="2aaf1-111">Size (in bytes) of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="2aaf1-112">*ppbyArray* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2aaf1-112">*ppbyArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aaf1-113">要傳回的位元組陣列指標。</span><span class="sxs-lookup"><span data-stu-id="2aaf1-113">Pointer to the byte array to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aaf1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2aaf1-114">Return value</span></span>

<span data-ttu-id="2aaf1-115">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="2aaf1-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="2aaf1-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2aaf1-116">Return code</span></span>                                                                                   | <span data-ttu-id="2aaf1-117">Description</span><span class="sxs-lookup"><span data-stu-id="2aaf1-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2aaf1-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2aaf1-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2aaf1-119">已成功配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="2aaf1-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="2aaf1-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2aaf1-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2aaf1-121">傳遞至函式的一或多個參數發生問題。</span><span class="sxs-lookup"><span data-stu-id="2aaf1-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="2aaf1-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2aaf1-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2aaf1-123">可用記憶體不足，無法滿足要求。</span><span class="sxs-lookup"><span data-stu-id="2aaf1-123">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="2aaf1-124">備註</span><span class="sxs-lookup"><span data-stu-id="2aaf1-124">Remarks</span></span>

<span data-ttu-id="2aaf1-125">若要建立對應至 **IStream** ([**IByteBuffer**](ibytebuffer.md)) 物件的通用位元組緩衝區，請呼叫 [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="2aaf1-125">To create a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object, call [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span></span>

<span data-ttu-id="2aaf1-126">若要建立不帶正負號字元的自動化 SAFEARRAY (bytes) ，請呼叫 [**CreateSafeArray**](iscardtypeconv-createsafearray.md)。</span><span class="sxs-lookup"><span data-stu-id="2aaf1-126">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2aaf1-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2aaf1-127">Requirements</span></span>



| <span data-ttu-id="2aaf1-128">需求</span><span class="sxs-lookup"><span data-stu-id="2aaf1-128">Requirement</span></span> | <span data-ttu-id="2aaf1-129">值</span><span class="sxs-lookup"><span data-stu-id="2aaf1-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2aaf1-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2aaf1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2aaf1-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2aaf1-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2aaf1-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2aaf1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2aaf1-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2aaf1-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2aaf1-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2aaf1-134">End of client support</span></span><br/>    | <span data-ttu-id="2aaf1-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2aaf1-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2aaf1-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2aaf1-136">End of server support</span></span><br/>    | <span data-ttu-id="2aaf1-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2aaf1-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2aaf1-138">標頭</span><span class="sxs-lookup"><span data-stu-id="2aaf1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2aaf1-139"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="2aaf1-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="2aaf1-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2aaf1-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="2aaf1-141"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2aaf1-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2aaf1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2aaf1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2aaf1-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2aaf1-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2aaf1-144">IID</span><span class="sxs-lookup"><span data-stu-id="2aaf1-144">IID</span></span><br/>                      | <span data-ttu-id="2aaf1-145">IID \_ ISCardTypeConv 定義為53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2aaf1-145">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2aaf1-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2aaf1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aaf1-147">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="2aaf1-147">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="2aaf1-148">智慧卡傳回值</span><span class="sxs-lookup"><span data-stu-id="2aaf1-148">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="2aaf1-149">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="2aaf1-149">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)
</dt> <dt>

[<span data-ttu-id="2aaf1-150">**CreateSafeArray**</span><span class="sxs-lookup"><span data-stu-id="2aaf1-150">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
