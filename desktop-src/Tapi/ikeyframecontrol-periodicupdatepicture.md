---
description: 應用程式會呼叫 PeriodicUpdatePicture 方法來設定資料流程中的計時器，以定期要求圖片更新。 圖片更新會導致高頻寬使用量，因此通常會使用這個方法，而不是 UpdatePicture。
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: 'IKeyFrameControl：:P eriodicUpdatePicture 方法 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989271"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a><span data-ttu-id="c9721-104">IKeyFrameControl：:P eriodicUpdatePicture 方法</span><span class="sxs-lookup"><span data-stu-id="c9721-104">IKeyFrameControl::PeriodicUpdatePicture method</span></span>

<span data-ttu-id="c9721-105">\[**PeriodicUpdatePicture** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="c9721-105">\[**PeriodicUpdatePicture** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c9721-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="c9721-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c9721-107">應用程式會呼叫 **PeriodicUpdatePicture** 方法來設定資料流程中的計時器，以定期要求圖片更新。</span><span class="sxs-lookup"><span data-stu-id="c9721-107">The **PeriodicUpdatePicture** method is called by an application to configure a timer in the stream that will ask for picture updates periodically.</span></span> <span data-ttu-id="c9721-108">圖片更新會導致高頻寬使用量，因此通常會使用這個方法，而不是 [**UpdatePicture**](ikeyframecontrol-updatepicture.md)。</span><span class="sxs-lookup"><span data-stu-id="c9721-108">Picture updates cause high bandwidth usage, so this method will normally be used instead of [**UpdatePicture**](ikeyframecontrol-updatepicture.md).</span></span>

<span data-ttu-id="c9721-109">如果在資料流程為使用中時呼叫方法，計時器將會立即啟動。</span><span class="sxs-lookup"><span data-stu-id="c9721-109">If the method is called when the stream is active, the timer will start immediately.</span></span> <span data-ttu-id="c9721-110">如果資料流程未處於使用中狀態，則當資料流程進入作用中狀態時，就會啟動計時器。</span><span class="sxs-lookup"><span data-stu-id="c9721-110">If the stream is not active, the timer will be started when the stream enters the active state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9721-111">語法</span><span class="sxs-lookup"><span data-stu-id="c9721-111">Syntax</span></span>


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a><span data-ttu-id="c9721-112">參數</span><span class="sxs-lookup"><span data-stu-id="c9721-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9721-113">*fEnable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9721-113">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9721-114">**TRUE** 會啟用計時器。</span><span class="sxs-lookup"><span data-stu-id="c9721-114">**TRUE** enables the timer.</span></span> <span data-ttu-id="c9721-115">**FALSE** 會停用它。</span><span class="sxs-lookup"><span data-stu-id="c9721-115">**FALSE** disables it.</span></span>

</dd> <dt>

<span data-ttu-id="c9721-116">*dwInterval* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9721-116">*dwInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9721-117">計時器的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c9721-117">The interval for the timer, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9721-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9721-118">Return value</span></span>

<span data-ttu-id="c9721-119">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c9721-119">This method can return one of these values.</span></span>



| <span data-ttu-id="c9721-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c9721-120">Return code</span></span>                                                                            | <span data-ttu-id="c9721-121">Description</span><span class="sxs-lookup"><span data-stu-id="c9721-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="c9721-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c9721-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="c9721-123">方法成功。</span><span class="sxs-lookup"><span data-stu-id="c9721-123">Method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="c9721-124"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="c9721-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="c9721-125">因為未預期的原因而失敗。</span><span class="sxs-lookup"><span data-stu-id="c9721-125">Failed for unexpected reasons.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9721-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9721-126">Requirements</span></span>



| <span data-ttu-id="c9721-127">需求</span><span class="sxs-lookup"><span data-stu-id="c9721-127">Requirement</span></span> | <span data-ttu-id="c9721-128">值</span><span class="sxs-lookup"><span data-stu-id="c9721-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9721-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="c9721-129">TAPI version</span></span><br/> | <span data-ttu-id="c9721-130">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c9721-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c9721-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c9721-131">Header</span></span><br/>       | <dl> <span data-ttu-id="c9721-132"><dt>H323priv。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9721-132"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="c9721-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9721-133">Library</span></span><br/>      | <dl> <span data-ttu-id="c9721-134"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="c9721-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c9721-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c9721-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="c9721-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9721-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c9721-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9721-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9721-138">H323 MSP</span><span class="sxs-lookup"><span data-stu-id="c9721-138">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

 




