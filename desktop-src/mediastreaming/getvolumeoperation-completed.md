---
title: GetVolumeOperation。 Completed 屬性
description: 取得或設定當 GetVolumeAsync 啟動的非同步作業完成時叫用的事件處理常式。
ms.assetid: 34100EE7-C4CB-4AE0-BD3E-9E23A643F87E
keywords:
- 完成的屬性媒體串流 API
- 完成的屬性媒體串流 API、GetVolumeOperation 介面
- GetVolumeOperation 介面媒體串流 API，已完成屬性
topic_type:
- apiref
api_name:
- GetVolumeOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21577d57e1e29aff1d2b12b92bcbef58a529eba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092667"
---
# <a name="getvolumeoperationcompleted-property"></a><span data-ttu-id="1933f-106">GetVolumeOperation。 Completed 屬性</span><span class="sxs-lookup"><span data-stu-id="1933f-106">GetVolumeOperation.Completed property</span></span>

<span data-ttu-id="1933f-107">取得或設定當 [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) 啟動的非同步作業完成時叫用的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="1933f-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) is completed.</span></span>

<span data-ttu-id="1933f-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="1933f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1933f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1933f-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetVolumeCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetVolumeCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="1933f-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="1933f-110">Property value</span></span>

<span data-ttu-id="1933f-111">事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="1933f-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="1933f-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1933f-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1933f-113">**GetVolumeOperation**</span><span class="sxs-lookup"><span data-stu-id="1933f-113">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

 