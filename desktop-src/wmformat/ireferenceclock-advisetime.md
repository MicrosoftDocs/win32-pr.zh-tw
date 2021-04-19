---
title: IReferenceClock AdviseTime 方法
description: AdviseTime 方法會要求經過一段時間的非同步通知。
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- AdviseTime 方法 windows Media 格式
- AdviseTime 方法 windows Media Format，IReferenceClock 介面
- IReferenceClock 介面 windows Media Format，AdviseTime 方法
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968465"
---
# <a name="ireferenceclockadvisetime-method"></a><span data-ttu-id="0d31c-106">IReferenceClock：： AdviseTime 方法</span><span class="sxs-lookup"><span data-stu-id="0d31c-106">IReferenceClock::AdviseTime method</span></span>

<span data-ttu-id="0d31c-107">**AdviseTime** 方法會要求經過一段時間的非同步通知。</span><span class="sxs-lookup"><span data-stu-id="0d31c-107">The **AdviseTime** method requests an asynchronous notification that a time has elapsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d31c-108">語法</span><span class="sxs-lookup"><span data-stu-id="0d31c-108">Syntax</span></span>


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="0d31c-109">參數</span><span class="sxs-lookup"><span data-stu-id="0d31c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d31c-110">*rtBaseTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d31c-110">*rtBaseTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d31c-111">基底參考時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="0d31c-111">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="0d31c-112">*rtStreamTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d31c-112">*rtStreamTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d31c-113">資料流程位移時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="0d31c-113">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="0d31c-114">*hEvent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d31c-114">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d31c-115">事件的控制碼，由呼叫端建立。</span><span class="sxs-lookup"><span data-stu-id="0d31c-115">Handle to an event, created by the caller.</span></span> <span data-ttu-id="0d31c-116">當指定的時間結束時，將會通知此事件。</span><span class="sxs-lookup"><span data-stu-id="0d31c-116">This event will be signaled when the time specified elapses.</span></span>

</dd> <dt>

<span data-ttu-id="0d31c-117">*pdwAdviseCookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0d31c-117">*pdwAdviseCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d31c-118">變數的指標，此變數會接收要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d31c-118">Pointer to a variable that receives an identifier for the request.</span></span> <span data-ttu-id="0d31c-119">這是用來識別未來對 **AdviseTime** 的呼叫，例如取消要求。</span><span class="sxs-lookup"><span data-stu-id="0d31c-119">This is used to identify this call to **AdviseTime** in the future for example, to cancel the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d31c-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d31c-120">Return value</span></span>

<span data-ttu-id="0d31c-121">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="0d31c-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0d31c-122">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="0d31c-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0d31c-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0d31c-123">Return code</span></span>                                                                               | <span data-ttu-id="0d31c-124">Description</span><span class="sxs-lookup"><span data-stu-id="0d31c-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="0d31c-125"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0d31c-125"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="0d31c-126">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="0d31c-126">The method succeeded.</span></span><br/>                        |
| <dl> <span data-ttu-id="0d31c-127"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="0d31c-127"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="0d31c-128">*PdwAdviseCookie* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0d31c-128">The *pdwAdviseCookie* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="0d31c-129"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="0d31c-129"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="0d31c-130">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="0d31c-130">Unspecified failure.</span></span><br/>                         |



 

## <a name="see-also"></a><span data-ttu-id="0d31c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d31c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d31c-132">**IReferenceClock 介面**</span><span class="sxs-lookup"><span data-stu-id="0d31c-132">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





