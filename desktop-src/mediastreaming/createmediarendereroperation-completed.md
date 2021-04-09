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
# <a name="createmediarendereroperationcompleted-property"></a>CreateMediaRendererOperation。 Completed 屬性

取得或設定當 [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) 或 [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) 啟動的非同步作業完成時叫用的事件處理常式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a>屬性值

事件處理常式。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CreateMediaRendererOperation**](createmediarendereroperation.md)
</dt> </dl>

 

 




