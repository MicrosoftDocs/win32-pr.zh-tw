---
title: RenderingParametersUpdate 事件
description: 每當 DMR 上有任何一組轉譯控制項參數進行更新時發生。
ms.assetid: 863ca879-a420-43d6-9ac8-94f8303bb759
keywords:
- RenderingParametersUpdate 事件媒體串流 API
topic_type:
- apiref
api_name:
- RenderingParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35e4898bae876babb0e5fbc1c4b9760eec6a9b62
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314848"
---
# <a name="renderingparametersupdate-event"></a><span data-ttu-id="89584-104">RenderingParametersUpdate 事件</span><span class="sxs-lookup"><span data-stu-id="89584-104">RenderingParametersUpdate event</span></span>

<span data-ttu-id="89584-105">每當 DMR 上有任何一組轉譯控制項參數進行更新時發生。</span><span class="sxs-lookup"><span data-stu-id="89584-105">Occurs whenever any of a set of rendering control parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="89584-106">語法</span><span class="sxs-lookup"><span data-stu-id="89584-106">Syntax</span></span>


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="89584-107">參數</span><span class="sxs-lookup"><span data-stu-id="89584-107">Parameters</span></span>

<span data-ttu-id="89584-108">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="89584-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89584-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="89584-109">Return value</span></span>

<span data-ttu-id="89584-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="89584-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89584-111">備註</span><span class="sxs-lookup"><span data-stu-id="89584-111">Remarks</span></span>

<span data-ttu-id="89584-112">若要處理此事件的通知，請使用 [**add \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate)方法來註冊 [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))事件處理常式函式。</span><span class="sxs-lookup"><span data-stu-id="89584-112">To handle notifications from this event, register a [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) event handler function using the [**add\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) method.</span></span> <span data-ttu-id="89584-113">若要取消註冊事件處理常式，請使用 [**remove \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) 方法。</span><span class="sxs-lookup"><span data-stu-id="89584-113">To unregister the event handler, use the [**remove\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) method.</span></span>

 

 