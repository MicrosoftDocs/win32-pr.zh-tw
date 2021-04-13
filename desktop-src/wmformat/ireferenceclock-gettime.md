---
title: IReferenceClock GetTime 方法
description: GetTime 方法會抓取目前的參考時間。
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- GetTime 方法 windows Media 格式
- GetTime 方法 windows Media Format，IReferenceClock 介面
- IReferenceClock 介面 windows Media Format，GetTime 方法
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373405"
---
# <a name="ireferenceclockgettime-method"></a><span data-ttu-id="b90a2-106">IReferenceClock：： GetTime 方法</span><span class="sxs-lookup"><span data-stu-id="b90a2-106">IReferenceClock::GetTime method</span></span>

<span data-ttu-id="b90a2-107">**GetTime** 方法會抓取目前的參考時間。</span><span class="sxs-lookup"><span data-stu-id="b90a2-107">The **GetTime** method retrieves the current reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="b90a2-108">語法</span><span class="sxs-lookup"><span data-stu-id="b90a2-108">Syntax</span></span>


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="b90a2-109">參數</span><span class="sxs-lookup"><span data-stu-id="b90a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b90a2-110">*pTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b90a2-110">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b90a2-111">接收目前時間的變數指標，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="b90a2-111">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b90a2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b90a2-112">Return value</span></span>

<span data-ttu-id="b90a2-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="b90a2-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b90a2-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="b90a2-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b90a2-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b90a2-115">Return code</span></span>                                                                               | <span data-ttu-id="b90a2-116">Description</span><span class="sxs-lookup"><span data-stu-id="b90a2-116">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="b90a2-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b90a2-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b90a2-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="b90a2-118">The method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="b90a2-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="b90a2-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b90a2-120">*PTime* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b90a2-120">The *pTime* parameter is **NULL**.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="b90a2-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b90a2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b90a2-122">**IReferenceClock 介面**</span><span class="sxs-lookup"><span data-stu-id="b90a2-122">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





