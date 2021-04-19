---
description: Get \_ EnumerationIf 方法會傳回列舉 ITTime 的 IEnumTime 列舉介面。
ms.assetid: 31f6fa94-d047-4c53-96ae-8dd7e66a4e33
title: 'ITTimeCollection：： get_EnumerationIf 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a698fca73e923597b2dff5b82e3258dd79306f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990590"
---
# <a name="ittimecollectionget_enumerationif-method"></a><span data-ttu-id="886a5-103">ITTimeCollection：： get \_ EnumerationIf 方法</span><span class="sxs-lookup"><span data-stu-id="886a5-103">ITTimeCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="886a5-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="886a5-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="886a5-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="886a5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="886a5-106">**Get \_ EnumerationIf** 方法會傳回列舉 [**ITTime**](ittime.md)的 [**IEnumTime**](ienumtime.md)列舉介面。</span><span class="sxs-lookup"><span data-stu-id="886a5-106">The **get\_EnumerationIf** method returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="886a5-107">語法</span><span class="sxs-lookup"><span data-stu-id="886a5-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="886a5-108">參數</span><span class="sxs-lookup"><span data-stu-id="886a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="886a5-109">*pVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="886a5-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="886a5-110">[**IEnumTime**](ienumtime.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="886a5-110">Pointer to the [**IEnumTime**](ienumtime.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="886a5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="886a5-111">Return value</span></span>

<span data-ttu-id="886a5-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="886a5-112">This method can return one of these values.</span></span>



| <span data-ttu-id="886a5-113">值</span><span class="sxs-lookup"><span data-stu-id="886a5-113">Value</span></span>                                                                                         | <span data-ttu-id="886a5-114">意義</span><span class="sxs-lookup"><span data-stu-id="886a5-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="886a5-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="886a5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="886a5-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="886a5-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="886a5-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="886a5-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="886a5-118">*PVal* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="886a5-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="886a5-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="886a5-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="886a5-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="886a5-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="886a5-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="886a5-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="886a5-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="886a5-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="886a5-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="886a5-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="886a5-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="886a5-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="886a5-125">備註</span><span class="sxs-lookup"><span data-stu-id="886a5-125">Remarks</span></span>

<span data-ttu-id="886a5-126">這個方法可以與 [**get \_ \_ NewEnum**](ittimecollection-get--newenum.md)互換，不同之處在于它會傳回 [**IEnumTime**](ienumtime.md)而不是 **IUnknown**。</span><span class="sxs-lookup"><span data-stu-id="886a5-126">This method is interchangeable with [**get\_\_NewEnum**](ittimecollection-get--newenum.md) except that it returns [**IEnumTime**](ienumtime.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="886a5-127">TAPI 會在 **ITTimeCollection：： get \_ EnumerationIf** 所傳回的 [**IEnumTime**](ienumtime.md)介面上呼叫 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="886a5-127">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **ITTimeCollection::get\_EnumerationIf**.</span></span> <span data-ttu-id="886a5-128">應用程式必須在 [**IEnumTime**](ienumtime.md)介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="886a5-128">The application must call **Release** on the [**IEnumTime**](ienumtime.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="886a5-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="886a5-129">Requirements</span></span>



| <span data-ttu-id="886a5-130">需求</span><span class="sxs-lookup"><span data-stu-id="886a5-130">Requirement</span></span> | <span data-ttu-id="886a5-131">值</span><span class="sxs-lookup"><span data-stu-id="886a5-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="886a5-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="886a5-132">TAPI version</span></span><br/> | <span data-ttu-id="886a5-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="886a5-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="886a5-134">標頭</span><span class="sxs-lookup"><span data-stu-id="886a5-134">Header</span></span><br/>       | <dl> <span data-ttu-id="886a5-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="886a5-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="886a5-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="886a5-136">Library</span></span><br/>      | <dl> <span data-ttu-id="886a5-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="886a5-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="886a5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="886a5-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="886a5-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="886a5-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="886a5-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="886a5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="886a5-141">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="886a5-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> <dt>

[<span data-ttu-id="886a5-142">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="886a5-142">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="886a5-143">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="886a5-143">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




