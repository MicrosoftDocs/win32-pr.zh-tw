---
description: Get \_ Count 方法會取得集合中的專案數。
ms.assetid: 9fe96af3-bb7b-4f6c-8df2-85bf7850c527
title: 'ITTimeCollection：： get_Count 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a385c8fa3120cbeaa4b876a8af4f60e0df5cb48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993300"
---
# <a name="ittimecollectionget_count-method"></a><span data-ttu-id="d5c01-103">ITTimeCollection：： get \_ Count 方法</span><span class="sxs-lookup"><span data-stu-id="d5c01-103">ITTimeCollection::get\_Count method</span></span>

<span data-ttu-id="d5c01-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="d5c01-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d5c01-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d5c01-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d5c01-106">**Get \_ Count** 方法會取得集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="d5c01-106">The **get\_Count** method gets the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c01-107">語法</span><span class="sxs-lookup"><span data-stu-id="d5c01-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d5c01-108">參數</span><span class="sxs-lookup"><span data-stu-id="d5c01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c01-109">*pVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d5c01-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c01-110">集合中專案數的指標。</span><span class="sxs-lookup"><span data-stu-id="d5c01-110">Pointer to the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c01-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5c01-111">Return value</span></span>

<span data-ttu-id="d5c01-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d5c01-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d5c01-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d5c01-113">Return code</span></span>                                                                                   | <span data-ttu-id="d5c01-114">Description</span><span class="sxs-lookup"><span data-stu-id="d5c01-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d5c01-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d5c01-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d5c01-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="d5c01-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d5c01-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d5c01-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d5c01-118">*PVal* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="d5c01-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="d5c01-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d5c01-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d5c01-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="d5c01-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d5c01-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="d5c01-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d5c01-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d5c01-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d5c01-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="d5c01-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d5c01-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="d5c01-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="d5c01-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5c01-125">Requirements</span></span>



| <span data-ttu-id="d5c01-126">需求</span><span class="sxs-lookup"><span data-stu-id="d5c01-126">Requirement</span></span> | <span data-ttu-id="d5c01-127">值</span><span class="sxs-lookup"><span data-stu-id="d5c01-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c01-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="d5c01-128">TAPI version</span></span><br/> | <span data-ttu-id="d5c01-129">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d5c01-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d5c01-130">標頭</span><span class="sxs-lookup"><span data-stu-id="d5c01-130">Header</span></span><br/>       | <dl> <span data-ttu-id="d5c01-131"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5c01-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5c01-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5c01-132">Library</span></span><br/>      | <dl> <span data-ttu-id="d5c01-133"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="d5c01-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d5c01-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d5c01-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="d5c01-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5c01-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c01-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5c01-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c01-137">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="d5c01-137">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="d5c01-138">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="d5c01-138">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




