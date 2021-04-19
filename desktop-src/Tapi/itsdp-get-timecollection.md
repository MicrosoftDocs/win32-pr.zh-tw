---
description: Get \_ TimeCollection 方法會取得會議的 ITTimeCollection 介面指標。
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: 'ITSdp：： get_TimeCollection 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1bac0f38f8c96762d4e36d8d3dfdff2136bdb86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981378"
---
# <a name="itsdpget_timecollection-method"></a><span data-ttu-id="a89a2-103">ITSdp：： get \_ TimeCollection 方法</span><span class="sxs-lookup"><span data-stu-id="a89a2-103">ITSdp::get\_TimeCollection method</span></span>

<span data-ttu-id="a89a2-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="a89a2-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a89a2-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="a89a2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a89a2-106">**Get \_ TimeCollection** 方法會取得會議的 [**ITTimeCollection**](ittimecollection.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="a89a2-106">The **get\_TimeCollection** method gets a pointer to an [**ITTimeCollection**](ittimecollection.md) interface for conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="a89a2-107">語法</span><span class="sxs-lookup"><span data-stu-id="a89a2-107">Syntax</span></span>


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a><span data-ttu-id="a89a2-108">參數</span><span class="sxs-lookup"><span data-stu-id="a89a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a89a2-109">*ppTimeCollection* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a89a2-109">*ppTimeCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a89a2-110">[**ITTimeCollection**](ittimecollection.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="a89a2-110">Pointer to [**ITTimeCollection**](ittimecollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a89a2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a89a2-111">Return value</span></span>

<span data-ttu-id="a89a2-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a89a2-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a89a2-113">值</span><span class="sxs-lookup"><span data-stu-id="a89a2-113">Value</span></span>                                                                                                                           | <span data-ttu-id="a89a2-114">意義</span><span class="sxs-lookup"><span data-stu-id="a89a2-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a89a2-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a89a2-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="a89a2-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="a89a2-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="a89a2-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a89a2-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="a89a2-118">*PpTimeCollection* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="a89a2-118">The *ppTimeCollection* parameter is not a valid pointer.</span></span><br/>                         |
| <dl> <span data-ttu-id="a89a2-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a89a2-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="a89a2-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="a89a2-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="a89a2-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="a89a2-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="a89a2-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a89a2-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="a89a2-123"><dt>**\_錯誤碼中的 HRESULT \_ \_ (錯誤 \_ 不正確 \_ 資料)**</dt></span><span class="sxs-lookup"><span data-stu-id="a89a2-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="a89a2-124">發生內部錯誤，通常是因為先前的方法失敗。</span><span class="sxs-lookup"><span data-stu-id="a89a2-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="a89a2-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a89a2-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="a89a2-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="a89a2-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="a89a2-127">備註</span><span class="sxs-lookup"><span data-stu-id="a89a2-127">Remarks</span></span>

<span data-ttu-id="a89a2-128">您也可以使用 **QueryInterface** 來取得 [**ITTimeCollection**](ittimecollection.md)指標。</span><span class="sxs-lookup"><span data-stu-id="a89a2-128">An [**ITTimeCollection**](ittimecollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="a89a2-129">TAPI 會在 **ITSdp：： get \_ TimeCollection** 所傳回的 [**ITTimeCollection**](ittimecollection.md)介面上呼叫 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="a89a2-129">TAPI calls the **AddRef** method on the [**ITTimeCollection**](ittimecollection.md) interface returned by **ITSdp::get\_TimeCollection**.</span></span> <span data-ttu-id="a89a2-130">應用程式必須在 **ITTimeCollection** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="a89a2-130">The application must call **Release** on the **ITTimeCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a89a2-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="a89a2-131">Requirements</span></span>



| <span data-ttu-id="a89a2-132">需求</span><span class="sxs-lookup"><span data-stu-id="a89a2-132">Requirement</span></span> | <span data-ttu-id="a89a2-133">值</span><span class="sxs-lookup"><span data-stu-id="a89a2-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a89a2-134">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="a89a2-134">TAPI version</span></span><br/> | <span data-ttu-id="a89a2-135">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a89a2-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a89a2-136">標頭</span><span class="sxs-lookup"><span data-stu-id="a89a2-136">Header</span></span><br/>       | <dl> <span data-ttu-id="a89a2-137"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="a89a2-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a89a2-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="a89a2-138">Library</span></span><br/>      | <dl> <span data-ttu-id="a89a2-139"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="a89a2-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a89a2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a89a2-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="a89a2-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a89a2-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a89a2-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a89a2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a89a2-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="a89a2-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="a89a2-144">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="a89a2-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> </dl>

 

 




