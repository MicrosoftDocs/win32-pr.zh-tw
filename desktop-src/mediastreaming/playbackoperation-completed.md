---
title: PlaybackOperation。 Completed 屬性
description: 取得或設定當其中一個 MediaRenderer 播放方法啟動的非同步作業完成時叫用的事件處理常式。
ms.assetid: E8F8D3FC-C31F-485C-A30B-2457F4B1DE82
keywords:
- 完成的屬性媒體串流 API
- 完成的屬性媒體串流 API、PlaybackOperation 介面
- PlaybackOperation 介面媒體串流 API，已完成屬性
topic_type:
- apiref
api_name:
- PlaybackOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf305b4028e223c36df0c8a59c5246228c5b8d40
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106966832"
---
# <a name="playbackoperationcompleted-property"></a><span data-ttu-id="346b4-106">PlaybackOperation。 Completed 屬性</span><span class="sxs-lookup"><span data-stu-id="346b4-106">PlaybackOperation.Completed property</span></span>

<span data-ttu-id="346b4-107">取得或設定當其中一個 [**MediaRenderer**](mediarenderer.md) 播放方法啟動的非同步作業完成時叫用的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="346b4-107">Gets or sets an event handler that is invoked when the asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods is completed.</span></span>

<span data-ttu-id="346b4-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="346b4-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="346b4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="346b4-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="346b4-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="346b4-110">Property value</span></span>

<span data-ttu-id="346b4-111">事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="346b4-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="346b4-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="346b4-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346b4-113">**PlaybackOperation**</span><span class="sxs-lookup"><span data-stu-id="346b4-113">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 




