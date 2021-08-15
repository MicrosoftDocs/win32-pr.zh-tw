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
ms.openlocfilehash: 389d7b281c10458e854407f9ce02bd2656fe6d4b16574408d75ae06ccc06d7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735781"
---
# <a name="gettransportinformationoperationcompleted-property"></a>GetTransportInformationOperation：： Completed 屬性

取得或設定當 [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) 啟動的非同步作業完成時叫用的事件處理常式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a>屬性值

事件處理常式。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 

 