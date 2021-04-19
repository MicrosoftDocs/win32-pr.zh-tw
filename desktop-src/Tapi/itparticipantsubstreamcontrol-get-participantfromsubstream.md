---
description: Get \_ ParticipantFromSubStream 方法可讓應用程式探索哪些參與者與指定的子串流相關聯。
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'ITParticipantSubStreamControl：： get_ParticipantFromSubStream 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999630"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a><span data-ttu-id="0e239-103">ITParticipantSubStreamControl：： get \_ ParticipantFromSubStream 方法</span><span class="sxs-lookup"><span data-stu-id="0e239-103">ITParticipantSubStreamControl::get\_ParticipantFromSubStream method</span></span>

<span data-ttu-id="0e239-104">\[**取得 \_ParticipantFromSubStream** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="0e239-104">\[**get\_ParticipantFromSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0e239-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="0e239-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0e239-106">**Get \_ ParticipantFromSubStream** 方法可讓應用程式探索哪些參與者與指定的子串流相關聯。</span><span class="sxs-lookup"><span data-stu-id="0e239-106">The **get\_ParticipantFromSubStream** method allows an application to discover which participants are associated with a given substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e239-107">語法</span><span class="sxs-lookup"><span data-stu-id="0e239-107">Syntax</span></span>


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="0e239-108">參數</span><span class="sxs-lookup"><span data-stu-id="0e239-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e239-109">*pITSubStream* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0e239-109">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e239-110">[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0e239-110">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0e239-111">*ppParticipant* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0e239-111">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e239-112">[**ITParticipant**](itparticipant.md)介面指標的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="0e239-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e239-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e239-113">Return value</span></span>

<span data-ttu-id="0e239-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0e239-114">This method can return one of these values.</span></span>



| <span data-ttu-id="0e239-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0e239-115">Return code</span></span>                                                                                     | <span data-ttu-id="0e239-116">Description</span><span class="sxs-lookup"><span data-stu-id="0e239-116">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e239-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0e239-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="0e239-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="0e239-118">Method succeeded.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="0e239-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="0e239-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="0e239-120">*PITSubStream* 或 *ppParticipant* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="0e239-120">The *pITSubStream* or *ppParticipant* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="0e239-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0e239-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="0e239-122">*PITSubStream* 參數未指向有效的介面。</span><span class="sxs-lookup"><span data-stu-id="0e239-122">The *pITSubStream* parameter does not point to valid interface.</span></span><br/>         |
| <dl> <span data-ttu-id="0e239-123"><dt>**TAPI \_ E \_ NOITEMS**</dt></span><span class="sxs-lookup"><span data-stu-id="0e239-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="0e239-124">沒有任何與子流相關聯的參與者。</span><span class="sxs-lookup"><span data-stu-id="0e239-124">There are no participants associated with the substream.</span></span><br/>                |
| <dl> <span data-ttu-id="0e239-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0e239-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="0e239-126">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="0e239-126">Insufficient memory exists to perform the operation.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="0e239-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e239-127">Requirements</span></span>



| <span data-ttu-id="0e239-128">需求</span><span class="sxs-lookup"><span data-stu-id="0e239-128">Requirement</span></span> | <span data-ttu-id="0e239-129">值</span><span class="sxs-lookup"><span data-stu-id="0e239-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e239-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="0e239-130">TAPI version</span></span><br/> | <span data-ttu-id="0e239-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0e239-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0e239-132">標頭</span><span class="sxs-lookup"><span data-stu-id="0e239-132">Header</span></span><br/>       | <dl> <span data-ttu-id="0e239-133"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e239-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="0e239-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="0e239-134">Library</span></span><br/>      | <dl> <span data-ttu-id="0e239-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="0e239-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0e239-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0e239-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="0e239-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e239-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0e239-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e239-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e239-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="0e239-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="0e239-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="0e239-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="0e239-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="0e239-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

