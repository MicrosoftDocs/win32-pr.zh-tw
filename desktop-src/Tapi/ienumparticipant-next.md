---
description: 下一個方法會取得列舉順序中的下一個指定元素數目。 這種方法在 Visual Basic 和指令碼語言中是隱藏的。
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'IEnumParticipant：： Next 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996496"
---
# <a name="ienumparticipantnext-method"></a><span data-ttu-id="dc542-104">IEnumParticipant：： Next 方法</span><span class="sxs-lookup"><span data-stu-id="dc542-104">IEnumParticipant::Next method</span></span>

<span data-ttu-id="dc542-105">\[**接下來** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="dc542-105">\[**Next** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dc542-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="dc542-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dc542-107">**下一個** 方法會取得列舉順序中的下一個指定元素數目。</span><span class="sxs-lookup"><span data-stu-id="dc542-107">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="dc542-108">這種方法在 Visual Basic 和指令碼語言中是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="dc542-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc542-109">語法</span><span class="sxs-lookup"><span data-stu-id="dc542-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="dc542-110">參數</span><span class="sxs-lookup"><span data-stu-id="dc542-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc542-111">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dc542-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc542-112">要求的元素數目。</span><span class="sxs-lookup"><span data-stu-id="dc542-112">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="dc542-113">*ppElements* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dc542-113">*ppElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc542-114">[**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="dc542-114">Pointer to [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="dc542-115">*pceltFetched* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dc542-115">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc542-116">實際提供的元素數目指標。</span><span class="sxs-lookup"><span data-stu-id="dc542-116">Pointer to number of elements actually supplied.</span></span> <span data-ttu-id="dc542-117">如果 *celt* 是1，則可能為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="dc542-117">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc542-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc542-118">Return value</span></span>

<span data-ttu-id="dc542-119">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="dc542-119">This method can return one of these values.</span></span>



| <span data-ttu-id="dc542-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dc542-120">Return code</span></span>                                                                                   | <span data-ttu-id="dc542-121">Description</span><span class="sxs-lookup"><span data-stu-id="dc542-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="dc542-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dc542-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dc542-123">方法傳回 *celt* 元素數目。</span><span class="sxs-lookup"><span data-stu-id="dc542-123">Method returned *celt* number of elements.</span></span><br/>           |
| <dl> <span data-ttu-id="dc542-124"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="dc542-124"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="dc542-125">剩餘的元素數目小於 *celt*。</span><span class="sxs-lookup"><span data-stu-id="dc542-125">Number of elements remaining was less than *celt*.</span></span><br/>   |
| <dl> <span data-ttu-id="dc542-126"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="dc542-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dc542-127">*PpElements* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="dc542-127">The *ppElements* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="dc542-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dc542-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dc542-129">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="dc542-129">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc542-130">備註</span><span class="sxs-lookup"><span data-stu-id="dc542-130">Remarks</span></span>

<span data-ttu-id="dc542-131">TAPI 會呼叫 **IEnumParticipant：： Next** 所傳回的 [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)介面上的 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)方法。</span><span class="sxs-lookup"><span data-stu-id="dc542-131">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interface returned by **IEnumParticipant::Next**.</span></span> <span data-ttu-id="dc542-132">應用程式必須在 **ITAgentHandler** 介面上呼叫 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="dc542-132">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **ITAgentHandler** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc542-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc542-133">Requirements</span></span>



| <span data-ttu-id="dc542-134">需求</span><span class="sxs-lookup"><span data-stu-id="dc542-134">Requirement</span></span> | <span data-ttu-id="dc542-135">值</span><span class="sxs-lookup"><span data-stu-id="dc542-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc542-136">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="dc542-136">TAPI version</span></span><br/> | <span data-ttu-id="dc542-137">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="dc542-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="dc542-138">標頭</span><span class="sxs-lookup"><span data-stu-id="dc542-138">Header</span></span><br/>       | <dl> <span data-ttu-id="dc542-139"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc542-139"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="dc542-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="dc542-140">Library</span></span><br/>      | <dl> <span data-ttu-id="dc542-141"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="dc542-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="dc542-142">DLL</span><span class="sxs-lookup"><span data-stu-id="dc542-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="dc542-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc542-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dc542-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc542-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc542-145">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="dc542-145">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="dc542-146">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="dc542-146">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

