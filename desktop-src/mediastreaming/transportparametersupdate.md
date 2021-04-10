---
title: TransportParametersUpdate 事件
description: 當 DMR 上有任何一組傳輸參數更新時發生。
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- TransportParametersUpdate 事件媒體串流 API
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58df04862275af5da8714f8a954dc5b127f833f2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842248"
---
# <a name="transportparametersupdate-event"></a><span data-ttu-id="592e7-104">TransportParametersUpdate 事件</span><span class="sxs-lookup"><span data-stu-id="592e7-104">TransportParametersUpdate event</span></span>

<span data-ttu-id="592e7-105">當 DMR 上有任何一組傳輸參數更新時發生。</span><span class="sxs-lookup"><span data-stu-id="592e7-105">Occurs whenever any of a set of transport parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="592e7-106">語法</span><span class="sxs-lookup"><span data-stu-id="592e7-106">Syntax</span></span>


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="592e7-107">參數</span><span class="sxs-lookup"><span data-stu-id="592e7-107">Parameters</span></span>

<span data-ttu-id="592e7-108">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="592e7-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="592e7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="592e7-109">Return value</span></span>

<span data-ttu-id="592e7-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="592e7-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="592e7-111">備註</span><span class="sxs-lookup"><span data-stu-id="592e7-111">Remarks</span></span>

<span data-ttu-id="592e7-112">若要處理此事件的通知，請使用 [**add \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate)方法來註冊 [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))事件處理常式函式。</span><span class="sxs-lookup"><span data-stu-id="592e7-112">To handle notifications from this event, register a [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) event handler function using the [**add\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) method.</span></span> <span data-ttu-id="592e7-113">若要取消註冊事件處理常式，請使用 [**remove \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) 方法。</span><span class="sxs-lookup"><span data-stu-id="592e7-113">To unregister the event handler, use the [**remove\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) method.</span></span>

 

 