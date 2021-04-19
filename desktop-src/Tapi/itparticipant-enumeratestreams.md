---
description: EnumerateStreams 方法會列舉目前與參與者的資料流程。 這個方法是針對 C 和 c + + 應用程式所提供。 Automation 用戶端應用程式（例如以 Visual Basic 撰寫的應用程式）必須使用「取得 \_ 資料流程」方法。
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'ITParticipant：： EnumerateStreams 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981310"
---
# <a name="itparticipantenumeratestreams-method"></a><span data-ttu-id="fcbf0-105">ITParticipant：： EnumerateStreams 方法</span><span class="sxs-lookup"><span data-stu-id="fcbf0-105">ITParticipant::EnumerateStreams method</span></span>

<span data-ttu-id="fcbf0-106">\[**EnumerateStreams** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="fcbf0-106">\[**EnumerateStreams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fcbf0-107">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="fcbf0-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fcbf0-108">**EnumerateStreams** 方法會列舉目前與參與者的資料流程。</span><span class="sxs-lookup"><span data-stu-id="fcbf0-108">The **EnumerateStreams** method enumerates streams currently with the participants.</span></span> <span data-ttu-id="fcbf0-109">這個方法是針對 C 和 c + + 應用程式所提供。</span><span class="sxs-lookup"><span data-stu-id="fcbf0-109">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="fcbf0-110">Automation 用戶端應用程式（例如以 Visual Basic 撰寫的應用程式）必須使用「 [**取得 \_ 資料流程**](itparticipant-get-streams.md) 」方法。</span><span class="sxs-lookup"><span data-stu-id="fcbf0-110">Automation client applications, such as those written in Visual Basic, must use the [**get\_Streams**](itparticipant-get-streams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcbf0-111">語法</span><span class="sxs-lookup"><span data-stu-id="fcbf0-111">Syntax</span></span>


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a><span data-ttu-id="fcbf0-112">參數</span><span class="sxs-lookup"><span data-stu-id="fcbf0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcbf0-113">*ppEnumStream* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fcbf0-113">*ppEnumStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbf0-114">[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)介面指標的指標。</span><span class="sxs-lookup"><span data-stu-id="fcbf0-114">Pointer to [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcbf0-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fcbf0-115">Return value</span></span>

<span data-ttu-id="fcbf0-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fcbf0-116">This method can return one of these values.</span></span>



| <span data-ttu-id="fcbf0-117">值</span><span class="sxs-lookup"><span data-stu-id="fcbf0-117">Value</span></span>                                                                                     | <span data-ttu-id="fcbf0-118">意義</span><span class="sxs-lookup"><span data-stu-id="fcbf0-118">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fcbf0-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="fcbf0-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="fcbf0-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="fcbf0-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fcbf0-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="fcbf0-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="fcbf0-122">*PpEnumStream* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="fcbf0-122">The *ppEnumStream* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fcbf0-123">備註</span><span class="sxs-lookup"><span data-stu-id="fcbf0-123">Remarks</span></span>

<span data-ttu-id="fcbf0-124">TAPI 會在 **ITParticipant：： EnumerateStreams** 傳回的 [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)介面上呼叫 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="fcbf0-124">TAPI calls the **AddRef** method on the [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface returned by **ITParticipant::EnumerateStreams**.</span></span> <span data-ttu-id="fcbf0-125">應用程式必須在 **IEnumStream** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="fcbf0-125">The application must call **Release** on the **IEnumStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcbf0-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="fcbf0-126">Requirements</span></span>



| <span data-ttu-id="fcbf0-127">需求</span><span class="sxs-lookup"><span data-stu-id="fcbf0-127">Requirement</span></span> | <span data-ttu-id="fcbf0-128">值</span><span class="sxs-lookup"><span data-stu-id="fcbf0-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fcbf0-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="fcbf0-129">TAPI version</span></span><br/> | <span data-ttu-id="fcbf0-130">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="fcbf0-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="fcbf0-131">標頭</span><span class="sxs-lookup"><span data-stu-id="fcbf0-131">Header</span></span><br/>       | <dl> <span data-ttu-id="fcbf0-132"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fcbf0-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fcbf0-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="fcbf0-133">Library</span></span><br/>      | <dl> <span data-ttu-id="fcbf0-134"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="fcbf0-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="fcbf0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fcbf0-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="fcbf0-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcbf0-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcbf0-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fcbf0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcbf0-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="fcbf0-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="fcbf0-139">**取得 \_ 資料流程**</span><span class="sxs-lookup"><span data-stu-id="fcbf0-139">**get\_Streams**</span></span>](itparticipant-get-streams.md)
</dt> <dt>

[<span data-ttu-id="fcbf0-140">**IEnumStream**</span><span class="sxs-lookup"><span data-stu-id="fcbf0-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




