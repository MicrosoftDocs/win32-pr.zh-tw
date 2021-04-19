---
title: StreamSelectOperation。 Completed 屬性
description: 取得或設定當 SelectBestStreamAsync 啟動的非同步作業完成時叫用的事件處理常式。
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- 完成的屬性媒體串流 API
- 完成的屬性媒體串流 API、StreamSelectOperation 介面
- StreamSelectOperation 介面媒體串流 API，已完成屬性
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74cfdf1a3db4f6843a5f12522b688e889e156f33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106983297"
---
# <a name="streamselectoperationcompleted-property"></a><span data-ttu-id="cb068-106">StreamSelectOperation。 Completed 屬性</span><span class="sxs-lookup"><span data-stu-id="cb068-106">StreamSelectOperation.Completed property</span></span>

<span data-ttu-id="cb068-107">取得或設定當 [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) 啟動的非同步作業完成時叫用的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="cb068-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span>

<span data-ttu-id="cb068-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb068-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb068-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb068-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="cb068-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="cb068-110">Property value</span></span>

<span data-ttu-id="cb068-111">事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="cb068-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb068-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb068-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb068-113">**StreamSelectOperation**</span><span class="sxs-lookup"><span data-stu-id="cb068-113">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

 