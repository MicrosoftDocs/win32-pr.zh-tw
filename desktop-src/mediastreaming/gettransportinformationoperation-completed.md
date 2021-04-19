---
title: GetTransportInformationOperation Completed 屬性
description: 取得或設定當 GetTransportInformationAsync 啟動的非同步作業完成時叫用的事件處理常式。
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- 完成的屬性媒體串流 API
- 完成的屬性媒體串流 API、GetTransportInformationOperation 介面
- GetTransportInformationOperation 介面媒體串流 API，已完成屬性
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.Completed
- GetTransportInformationOperation.get_Completed
- GetTransportInformationOperation.put_Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2948af2ed84a70c9f37efbc4aae985e9b1ab5804
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106991103"
---
# <a name="gettransportinformationoperationcompleted-property"></a><span data-ttu-id="84a87-106">GetTransportInformationOperation：： Completed 屬性</span><span class="sxs-lookup"><span data-stu-id="84a87-106">GetTransportInformationOperation::Completed property</span></span>

<span data-ttu-id="84a87-107">取得或設定當 [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) 啟動的非同步作業完成時叫用的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="84a87-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) is completed.</span></span>

<span data-ttu-id="84a87-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="84a87-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="84a87-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="84a87-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="84a87-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="84a87-110">Property value</span></span>

<span data-ttu-id="84a87-111">事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="84a87-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="84a87-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84a87-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a87-113">**GetTransportInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="84a87-113">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

 