---
description: Get \_ SubStreamFromParticipant 方法可讓應用程式探索哪些子串流與指定的參與者相關聯。
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'ITParticipantSubStreamControl：： get_SubStreamFromParticipant 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0eae68cd62c38348e1a576f114a9e93ac52f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993247"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a><span data-ttu-id="5939d-103">ITParticipantSubStreamControl：： get \_ SubStreamFromParticipant 方法</span><span class="sxs-lookup"><span data-stu-id="5939d-103">ITParticipantSubStreamControl::get\_SubStreamFromParticipant method</span></span>

<span data-ttu-id="5939d-104">\[**取得 \_SubStreamFromParticipant** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="5939d-104">\[**get\_SubStreamFromParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5939d-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="5939d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5939d-106">**Get \_ SubStreamFromParticipant** 方法可讓應用程式探索哪些子串流與指定的參與者相關聯。</span><span class="sxs-lookup"><span data-stu-id="5939d-106">The **get\_SubStreamFromParticipant** method allows an application to discover which substreams are associated with a given participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="5939d-107">語法</span><span class="sxs-lookup"><span data-stu-id="5939d-107">Syntax</span></span>


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="5939d-108">參數</span><span class="sxs-lookup"><span data-stu-id="5939d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5939d-109">*pParticipant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5939d-109">*pParticipant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5939d-110">[**ITParticipant**](itparticipant.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5939d-110">Pointer to [**ITParticipant**](itparticipant.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="5939d-111">*ppITSubStream* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5939d-111">*ppITSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5939d-112">[**ITParticipant**](itparticipant.md)介面指標的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="5939d-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5939d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5939d-113">Return value</span></span>

<span data-ttu-id="5939d-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5939d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="5939d-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5939d-115">Return code</span></span>                                                                                   | <span data-ttu-id="5939d-116">Description</span><span class="sxs-lookup"><span data-stu-id="5939d-116">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5939d-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5939d-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5939d-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="5939d-118">Method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="5939d-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="5939d-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5939d-120">*PpITSubStream* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="5939d-120">The *ppITSubStream* parameter is not a valid pointer.</span></span><br/>             |
| <dl> <span data-ttu-id="5939d-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5939d-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5939d-122">*PParticipant* 參數未指向有效的介面。</span><span class="sxs-lookup"><span data-stu-id="5939d-122">The *pParticipant* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="5939d-123"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="5939d-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="5939d-124">無法存取資料流程的參與者資訊。</span><span class="sxs-lookup"><span data-stu-id="5939d-124">The stream's participant information could not be accessed.</span></span><br/>       |
| <dl> <span data-ttu-id="5939d-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5939d-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5939d-126">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="5939d-126">Insufficient memory exists to perform the operation.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="5939d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="5939d-127">Requirements</span></span>



| <span data-ttu-id="5939d-128">需求</span><span class="sxs-lookup"><span data-stu-id="5939d-128">Requirement</span></span> | <span data-ttu-id="5939d-129">值</span><span class="sxs-lookup"><span data-stu-id="5939d-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5939d-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="5939d-130">TAPI version</span></span><br/> | <span data-ttu-id="5939d-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5939d-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5939d-132">標頭</span><span class="sxs-lookup"><span data-stu-id="5939d-132">Header</span></span><br/>       | <dl> <span data-ttu-id="5939d-133"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="5939d-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="5939d-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="5939d-134">Library</span></span><br/>      | <dl> <span data-ttu-id="5939d-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="5939d-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5939d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5939d-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="5939d-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5939d-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5939d-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5939d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5939d-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="5939d-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="5939d-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="5939d-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="5939d-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="5939d-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

