---
description: 決定 IStream COM 介面的大小（以位元組為單位）。
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'ISCardTypeConv：： SizeOfIStream 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 603a01dc6cb4727d59a7fb82c3270c08a495f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984209"
---
# <a name="iscardtypeconvsizeofistream-method"></a><span data-ttu-id="ade81-103">ISCardTypeConv：： SizeOfIStream 方法</span><span class="sxs-lookup"><span data-stu-id="ade81-103">ISCardTypeConv::SizeOfIStream method</span></span>

<span data-ttu-id="ade81-104">\[**SizeOfIStream** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ade81-104">\[The **SizeOfIStream** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ade81-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="ade81-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ade81-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="ade81-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ade81-107">**SizeOfIStream** 方法會決定 **IStream** COM 介面的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ade81-107">The **SizeOfIStream** method determines the size, in bytes, of the **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ade81-108">語法</span><span class="sxs-lookup"><span data-stu-id="ade81-108">Syntax</span></span>


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a><span data-ttu-id="ade81-109">參數</span><span class="sxs-lookup"><span data-stu-id="ade81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ade81-110">*pStrm* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ade81-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ade81-111">**IStream** COM 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ade81-111">A pointer to the **IStream** COM interface.</span></span>

</dd> <dt>

<span data-ttu-id="ade81-112">*puliSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ade81-112">*puliSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ade81-113">不帶正負號的大整數指標，可保存 **IStream** COM 介面的整個64位 sizeof 值。</span><span class="sxs-lookup"><span data-stu-id="ade81-113">A pointer to the unsigned large integer that can hold the entire 64-bit sizeof value of the **IStream** COM interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ade81-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ade81-114">Return value</span></span>

<span data-ttu-id="ade81-115">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="ade81-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ade81-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ade81-116">Return code</span></span>                                                                                  | <span data-ttu-id="ade81-117">Description</span><span class="sxs-lookup"><span data-stu-id="ade81-117">Description</span></span>                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ade81-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ade81-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ade81-119">函數 succeeded 和 *\* PuliSize* 是 IStream COM 介面的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ade81-119">The function succeeded and *\*puliSize* is the size, in bytes, of the IStream COM interface.</span></span><br/> |
| <dl> <span data-ttu-id="ade81-120"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="ade81-120"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="ade81-121">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="ade81-121">Unspecified failure occurred.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="ade81-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ade81-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ade81-123">*PuliSize* 參數不正確。</span><span class="sxs-lookup"><span data-stu-id="ade81-123">The *puliSize* parameter is incorrect.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="ade81-124"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="ade81-124"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="ade81-125">*PStrm* 參數不正確。</span><span class="sxs-lookup"><span data-stu-id="ade81-125">The *pStrm* parameter is incorrect.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="ade81-126"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="ade81-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="ade81-127">發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ade81-127">Unexpected error occurred.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="ade81-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="ade81-128">Requirements</span></span>



| <span data-ttu-id="ade81-129">需求</span><span class="sxs-lookup"><span data-stu-id="ade81-129">Requirement</span></span> | <span data-ttu-id="ade81-130">值</span><span class="sxs-lookup"><span data-stu-id="ade81-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ade81-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ade81-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ade81-132">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ade81-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ade81-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ade81-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ade81-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ade81-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ade81-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ade81-135">End of client support</span></span><br/>    | <span data-ttu-id="ade81-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ade81-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ade81-137">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ade81-137">End of server support</span></span><br/>    | <span data-ttu-id="ade81-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ade81-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ade81-139">標頭</span><span class="sxs-lookup"><span data-stu-id="ade81-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ade81-140"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="ade81-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ade81-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ade81-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="ade81-142"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ade81-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ade81-143">DLL</span><span class="sxs-lookup"><span data-stu-id="ade81-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ade81-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ade81-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ade81-145">IID</span><span class="sxs-lookup"><span data-stu-id="ade81-145">IID</span></span><br/>                      | <span data-ttu-id="ade81-146">IID \_ ISCardTypeConv 定義為53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ade81-146">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ade81-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ade81-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ade81-148">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="ade81-148">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="ade81-149">智慧卡傳回值</span><span class="sxs-lookup"><span data-stu-id="ade81-149">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
