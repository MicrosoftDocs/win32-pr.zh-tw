---
description: Get \_ EnumerationIf 方法會取得媒體列舉介面的指標。
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: 'ITMediaCollection：： get_EnumerationIf 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a7e7d85c1f7a433a31360fabc8b5dac71e68ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983115"
---
# <a name="itmediacollectionget_enumerationif-method"></a><span data-ttu-id="d1915-103">ITMediaCollection：： get \_ EnumerationIf 方法</span><span class="sxs-lookup"><span data-stu-id="d1915-103">ITMediaCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="d1915-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="d1915-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d1915-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d1915-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d1915-106">**Get \_ EnumerationIf** 方法會取得媒體列舉介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d1915-106">The **get\_EnumerationIf** method gets a pointer to a media enumeration interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1915-107">語法</span><span class="sxs-lookup"><span data-stu-id="d1915-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d1915-108">參數</span><span class="sxs-lookup"><span data-stu-id="d1915-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1915-109">*pVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d1915-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1915-110">所需專案的 [**IEnumMedia**](ienummedia.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="d1915-110">Pointer to the [**IEnumMedia**](ienummedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1915-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1915-111">Return value</span></span>

<span data-ttu-id="d1915-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d1915-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d1915-113">值</span><span class="sxs-lookup"><span data-stu-id="d1915-113">Value</span></span>                                                                                         | <span data-ttu-id="d1915-114">意義</span><span class="sxs-lookup"><span data-stu-id="d1915-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d1915-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d1915-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d1915-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="d1915-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d1915-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d1915-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d1915-118">*PVal* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="d1915-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="d1915-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d1915-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d1915-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="d1915-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d1915-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="d1915-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d1915-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d1915-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d1915-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="d1915-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d1915-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="d1915-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="d1915-125">備註</span><span class="sxs-lookup"><span data-stu-id="d1915-125">Remarks</span></span>

<span data-ttu-id="d1915-126">這個方法可以與 [**get \_ \_ NewEnum**](itmediacollection-get--newenum.md)互換，不同之處在于它會傳回 [**IEnumMedia**](ienummedia.md)而不是 **IUnknown**。</span><span class="sxs-lookup"><span data-stu-id="d1915-126">This method is interchangeable with [**get\_\_NewEnum**](itmediacollection-get--newenum.md) except that it returns [**IEnumMedia**](ienummedia.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="d1915-127">TAPI 會在 **ITMediaCollection：： get \_ Enumerationlf** 所傳回的 [**IEnumMedia**](ienummedia.md)介面上呼叫 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="d1915-127">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **ITMediaCollection::get\_Enumerationlf**.</span></span> <span data-ttu-id="d1915-128">應用程式必須在 **IEnumMedia** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="d1915-128">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1915-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1915-129">Requirements</span></span>



| <span data-ttu-id="d1915-130">需求</span><span class="sxs-lookup"><span data-stu-id="d1915-130">Requirement</span></span> | <span data-ttu-id="d1915-131">值</span><span class="sxs-lookup"><span data-stu-id="d1915-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1915-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="d1915-132">TAPI version</span></span><br/> | <span data-ttu-id="d1915-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d1915-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d1915-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d1915-134">Header</span></span><br/>       | <dl> <span data-ttu-id="d1915-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1915-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1915-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="d1915-136">Library</span></span><br/>      | <dl> <span data-ttu-id="d1915-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="d1915-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d1915-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d1915-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="d1915-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1915-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1915-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1915-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1915-141">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="d1915-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> <dt>

[<span data-ttu-id="d1915-142">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="d1915-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




