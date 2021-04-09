---
title: CreateMediaRendererOperation。 Completed 屬性
description: 取得或設定當 CreateMediaRendererAsync 或 CreateMediaRendererFromBasicDeviceAsync 啟動的非同步作業完成時叫用的事件處理常式。
ms.assetid: B62CF929-13D0-4665-89E4-DEC48A38DDF7
keywords:
- 完成的屬性媒體串流 API
- 完成的屬性媒體串流 API、CreateMediaRendererOperation 介面
- CreateMediaRendererOperation 介面媒體串流 API，已完成屬性
topic_type:
- apiref
api_name:
- CreateMediaRendererOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3b4ebafc1441741a352f4573709495228bf13e4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678479"
---
# <a name="createmediarendereroperationcompleted-property"></a><span data-ttu-id="2764a-106">CreateMediaRendererOperation。 Completed 屬性</span><span class="sxs-lookup"><span data-stu-id="2764a-106">CreateMediaRendererOperation.Completed property</span></span>

<span data-ttu-id="2764a-107">取得或設定當 [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) 或 [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) 啟動的非同步作業完成時叫用的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="2764a-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) or [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) is completed.</span></span>

<span data-ttu-id="2764a-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2764a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2764a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2764a-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a><span data-ttu-id="2764a-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="2764a-110">Property value</span></span>

<span data-ttu-id="2764a-111">事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="2764a-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="2764a-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2764a-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2764a-113">**CreateMediaRendererOperation**</span><span class="sxs-lookup"><span data-stu-id="2764a-113">**CreateMediaRendererOperation**</span></span>](createmediarendereroperation.md)
</dt> </dl>

 

 




