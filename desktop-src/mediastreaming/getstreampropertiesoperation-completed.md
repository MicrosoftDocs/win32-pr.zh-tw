---
title: GetStreamPropertiesOperation。 Completed 屬性
description: 取得或設定當 GetStreamPropertiesAsync 啟動的非同步作業完成時叫用的事件處理常式。
ms.assetid: 97194F8E-DE36-4DC6-ADB5-F1EDE8AEF079
keywords:
- 完成的屬性媒體串流 API
- 完成的屬性媒體串流 API、GetStreamPropertiesOperation 介面
- GetStreamPropertiesOperation 介面媒體串流 API，已完成屬性
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb60ad137c8dafa42a58394d58a105267dabda3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375113"
---
# <a name="getstreampropertiesoperationcompleted-property"></a><span data-ttu-id="462a2-106">GetStreamPropertiesOperation。 Completed 屬性</span><span class="sxs-lookup"><span data-stu-id="462a2-106">GetStreamPropertiesOperation.Completed property</span></span>

<span data-ttu-id="462a2-107">取得或設定當 [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) 啟動的非同步作業完成時叫用的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="462a2-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) is completed.</span></span>

<span data-ttu-id="462a2-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="462a2-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="462a2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="462a2-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="462a2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="462a2-110">Property value</span></span>

<span data-ttu-id="462a2-111">事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="462a2-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="462a2-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="462a2-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="462a2-113">**GetStreamPropertiesOperation**</span><span class="sxs-lookup"><span data-stu-id="462a2-113">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

 