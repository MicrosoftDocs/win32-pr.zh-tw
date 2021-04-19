---
description: Get \_ Count 方法會取得會話中的媒體數目。
ms.assetid: 9d085a34-9a49-4447-8d11-56d71a2a3592
title: 'ITMediaCollection：： get_Count 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f5a4fb6d7f1b942f37aae1356c7b49e0e60f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997720"
---
# <a name="itmediacollectionget_count-method"></a><span data-ttu-id="3286a-103">ITMediaCollection：： get \_ Count 方法</span><span class="sxs-lookup"><span data-stu-id="3286a-103">ITMediaCollection::get\_Count method</span></span>

<span data-ttu-id="3286a-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="3286a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3286a-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="3286a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3286a-106">**Get \_ Count** 方法會取得會話中的媒體數目。</span><span class="sxs-lookup"><span data-stu-id="3286a-106">The **get\_Count** method gets the number of media in the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="3286a-107">語法</span><span class="sxs-lookup"><span data-stu-id="3286a-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="3286a-108">參數</span><span class="sxs-lookup"><span data-stu-id="3286a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3286a-109">*pVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3286a-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3286a-110">會話中的媒體計數。</span><span class="sxs-lookup"><span data-stu-id="3286a-110">Count of media in the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3286a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3286a-111">Return value</span></span>

<span data-ttu-id="3286a-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3286a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3286a-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3286a-113">Return code</span></span>                                                                                   | <span data-ttu-id="3286a-114">Description</span><span class="sxs-lookup"><span data-stu-id="3286a-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3286a-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3286a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3286a-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="3286a-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3286a-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="3286a-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3286a-118">*PVal* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="3286a-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="3286a-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3286a-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3286a-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="3286a-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3286a-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="3286a-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3286a-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3286a-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3286a-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="3286a-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3286a-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="3286a-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="3286a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3286a-125">Requirements</span></span>



| <span data-ttu-id="3286a-126">需求</span><span class="sxs-lookup"><span data-stu-id="3286a-126">Requirement</span></span> | <span data-ttu-id="3286a-127">值</span><span class="sxs-lookup"><span data-stu-id="3286a-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3286a-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="3286a-128">TAPI version</span></span><br/> | <span data-ttu-id="3286a-129">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3286a-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3286a-130">標頭</span><span class="sxs-lookup"><span data-stu-id="3286a-130">Header</span></span><br/>       | <dl> <span data-ttu-id="3286a-131"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="3286a-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3286a-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="3286a-132">Library</span></span><br/>      | <dl> <span data-ttu-id="3286a-133"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="3286a-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3286a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3286a-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="3286a-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3286a-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3286a-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3286a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3286a-137">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="3286a-137">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




