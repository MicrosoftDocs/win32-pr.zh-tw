---
title: GetMuteOperation。 Completed 屬性
description: 取得或設定當 GetMuteAsync 啟動的非同步作業完成時叫用的事件處理常式。
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- 完成的屬性媒體串流 API
- 完成的屬性媒體串流 API、GetMuteOperation 介面
- GetMuteOperation 介面媒體串流 API，已完成屬性
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40c360dc3597d8cf04d1a8c505e479a38136f592
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682177"
---
# <a name="getmuteoperationcompleted-property"></a><span data-ttu-id="8a91d-106">GetMuteOperation。 Completed 屬性</span><span class="sxs-lookup"><span data-stu-id="8a91d-106">GetMuteOperation.Completed property</span></span>

<span data-ttu-id="8a91d-107">取得或設定當 [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) 啟動的非同步作業完成時叫用的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="8a91d-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) is completed.</span></span>

<span data-ttu-id="8a91d-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="8a91d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a91d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a91d-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="8a91d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="8a91d-110">Property value</span></span>

<span data-ttu-id="8a91d-111">事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="8a91d-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a91d-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a91d-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a91d-113">**GetMuteOperation**</span><span class="sxs-lookup"><span data-stu-id="8a91d-113">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

 