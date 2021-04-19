---
description: Get \_ Item 方法會使用索引，從集合中取得專案。
ms.assetid: 7401ae21-190d-479c-aebc-51bf8a953b94
title: 'ITTimeCollection：： get_Item 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b9dec40070ff3abddce0e425300f6d805c1cc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989761"
---
# <a name="ittimecollectionget_item-method"></a><span data-ttu-id="9cf3b-103">ITTimeCollection：： get \_ Item 方法</span><span class="sxs-lookup"><span data-stu-id="9cf3b-103">ITTimeCollection::get\_Item method</span></span>

<span data-ttu-id="9cf3b-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9cf3b-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="9cf3b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9cf3b-106">**Get \_ Item** 方法會使用索引，從集合中取得專案。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-106">The **get\_Item** method gets an item from the collection using an index.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cf3b-107">語法</span><span class="sxs-lookup"><span data-stu-id="9cf3b-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG   Index,
  [out] ITTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="9cf3b-108">參數</span><span class="sxs-lookup"><span data-stu-id="9cf3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cf3b-109">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9cf3b-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cf3b-110">要取得之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="9cf3b-111">*pVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9cf3b-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cf3b-112">[**ITTime**](ittime.md)所需介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-112">Pointer to [**ITTime**](ittime.md) desired interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cf3b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9cf3b-113">Return value</span></span>

<span data-ttu-id="9cf3b-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="9cf3b-115">值</span><span class="sxs-lookup"><span data-stu-id="9cf3b-115">Value</span></span>                                                                                         | <span data-ttu-id="9cf3b-116">意義</span><span class="sxs-lookup"><span data-stu-id="9cf3b-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="9cf3b-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf3b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9cf3b-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9cf3b-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf3b-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9cf3b-120">*PVal* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="9cf3b-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf3b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9cf3b-122">*索引* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="9cf3b-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf3b-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9cf3b-124">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="9cf3b-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf3b-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9cf3b-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9cf3b-127"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf3b-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="9cf3b-128">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="9cf3b-129">備註</span><span class="sxs-lookup"><span data-stu-id="9cf3b-129">Remarks</span></span>

<span data-ttu-id="9cf3b-130">TAPI 會呼叫 **TTimeCollection：： get \_ 專案** 所傳回之 [**ITTime**](ittime.md)介面上的 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-130">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by I **TTimeCollection::get\_Item**.</span></span> <span data-ttu-id="9cf3b-131">應用程式必須在 **ITTime** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="9cf3b-131">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cf3b-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="9cf3b-132">Requirements</span></span>



| <span data-ttu-id="9cf3b-133">需求</span><span class="sxs-lookup"><span data-stu-id="9cf3b-133">Requirement</span></span> | <span data-ttu-id="9cf3b-134">值</span><span class="sxs-lookup"><span data-stu-id="9cf3b-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9cf3b-135">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="9cf3b-135">TAPI version</span></span><br/> | <span data-ttu-id="9cf3b-136">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9cf3b-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9cf3b-137">標頭</span><span class="sxs-lookup"><span data-stu-id="9cf3b-137">Header</span></span><br/>       | <dl> <span data-ttu-id="9cf3b-138"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="9cf3b-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9cf3b-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="9cf3b-139">Library</span></span><br/>      | <dl> <span data-ttu-id="9cf3b-140"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="9cf3b-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9cf3b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9cf3b-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="9cf3b-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cf3b-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cf3b-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cf3b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cf3b-144">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="9cf3b-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="9cf3b-145">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="9cf3b-145">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




