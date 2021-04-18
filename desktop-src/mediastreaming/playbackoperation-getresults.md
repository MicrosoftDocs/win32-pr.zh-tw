---
title: PlaybackOperation. GetResults 方法
description: 傳回由其中一個 MediaRenderer 播放方法啟動的非同步作業結果。
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，PlaybackOperation 介面
- PlaybackOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f146876966cc4e003bd88ad295c9938e5240abfe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104372795"
---
# <a name="playbackoperationgetresults-method"></a><span data-ttu-id="803ac-106">PlaybackOperation. GetResults 方法</span><span class="sxs-lookup"><span data-stu-id="803ac-106">PlaybackOperation.GetResults method</span></span>

<span data-ttu-id="803ac-107">傳回由其中一個 [**MediaRenderer**](mediarenderer.md) 播放方法啟動的非同步作業結果。</span><span class="sxs-lookup"><span data-stu-id="803ac-107">Returns the results of an asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="803ac-108">語法</span><span class="sxs-lookup"><span data-stu-id="803ac-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="803ac-109">參數</span><span class="sxs-lookup"><span data-stu-id="803ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="803ac-110">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="803ac-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="803ac-111">運算的結果。</span><span class="sxs-lookup"><span data-stu-id="803ac-111">The result of the operation.</span></span> <span data-ttu-id="803ac-112">值為0表示作業已完成。</span><span class="sxs-lookup"><span data-stu-id="803ac-112">A value of 0 indicates that the operation completed.</span></span> <span data-ttu-id="803ac-113">其他值則會保留。</span><span class="sxs-lookup"><span data-stu-id="803ac-113">Other values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="803ac-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="803ac-114">Return value</span></span>

<span data-ttu-id="803ac-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="803ac-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="803ac-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="803ac-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="803ac-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="803ac-117">Return code</span></span>                                                                          | <span data-ttu-id="803ac-118">Description</span><span class="sxs-lookup"><span data-stu-id="803ac-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="803ac-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="803ac-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="803ac-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="803ac-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="803ac-121">備註</span><span class="sxs-lookup"><span data-stu-id="803ac-121">Remarks</span></span>

<span data-ttu-id="803ac-122">**GetResults** 方法通常是由設定 [**Completed**](playbackoperation-completed.md)屬性所註冊的事件處理常式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="803ac-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](playbackoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="803ac-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="803ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803ac-124">**PlaybackOperation**</span><span class="sxs-lookup"><span data-stu-id="803ac-124">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 





