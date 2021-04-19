---
description: Get \_ NumPorts 方法會取得會話所需的埠數目。 會話會使用從 get StartPort 傳回的值開始的指定埠數目 \_ 。
ms.assetid: 9ebdcf51-e095-4173-97d6-7754560abfb5
title: 'ITMedia：： get_NumPorts 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc223ddd5d210d2c1d440c52ca4201ccd6334b08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981670"
---
# <a name="itmediaget_numports-method"></a><span data-ttu-id="14bcf-104">ITMedia：： get \_ NumPorts 方法</span><span class="sxs-lookup"><span data-stu-id="14bcf-104">ITMedia::get\_NumPorts method</span></span>

<span data-ttu-id="14bcf-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="14bcf-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="14bcf-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="14bcf-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="14bcf-107">**Get \_ NumPorts** 方法會取得會話所需的埠數目。</span><span class="sxs-lookup"><span data-stu-id="14bcf-107">The **get\_NumPorts** method gets the number of ports needed for the session.</span></span> <span data-ttu-id="14bcf-108">會話會使用從 [**get \_ StartPort**](itmedia-get-startport.md)傳回的值開始的指定埠數目。</span><span class="sxs-lookup"><span data-stu-id="14bcf-108">The session uses the specified number of ports starting from the value returned by [**get\_StartPort**](itmedia-get-startport.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="14bcf-109">語法</span><span class="sxs-lookup"><span data-stu-id="14bcf-109">Syntax</span></span>


```C++
HRESULT get_NumPorts(
  [out] LONG *pNumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="14bcf-110">參數</span><span class="sxs-lookup"><span data-stu-id="14bcf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14bcf-111">*pNumPorts* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="14bcf-111">*pNumPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14bcf-112">埠數目的指標。</span><span class="sxs-lookup"><span data-stu-id="14bcf-112">Pointer to the number of ports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14bcf-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="14bcf-113">Return value</span></span>

<span data-ttu-id="14bcf-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="14bcf-114">This method can return one of these values.</span></span>



| <span data-ttu-id="14bcf-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="14bcf-115">Return code</span></span>                                                                                   | <span data-ttu-id="14bcf-116">Description</span><span class="sxs-lookup"><span data-stu-id="14bcf-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="14bcf-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="14bcf-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="14bcf-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="14bcf-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="14bcf-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="14bcf-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="14bcf-120">*PNumPorts* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="14bcf-120">The *pNumPorts* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="14bcf-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="14bcf-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="14bcf-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="14bcf-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="14bcf-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="14bcf-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="14bcf-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="14bcf-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="14bcf-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="14bcf-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="14bcf-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="14bcf-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="14bcf-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="14bcf-127">Requirements</span></span>



| <span data-ttu-id="14bcf-128">需求</span><span class="sxs-lookup"><span data-stu-id="14bcf-128">Requirement</span></span> | <span data-ttu-id="14bcf-129">值</span><span class="sxs-lookup"><span data-stu-id="14bcf-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14bcf-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="14bcf-130">TAPI version</span></span><br/> | <span data-ttu-id="14bcf-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="14bcf-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="14bcf-132">標頭</span><span class="sxs-lookup"><span data-stu-id="14bcf-132">Header</span></span><br/>       | <dl> <span data-ttu-id="14bcf-133"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="14bcf-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="14bcf-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="14bcf-134">Library</span></span><br/>      | <dl> <span data-ttu-id="14bcf-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="14bcf-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="14bcf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="14bcf-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="14bcf-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14bcf-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14bcf-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14bcf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14bcf-139">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="14bcf-139">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




