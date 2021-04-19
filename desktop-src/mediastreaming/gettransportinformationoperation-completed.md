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
# <a name="gettransportinformationoperationcompleted-property"></a>GetTransportInformationOperation：： Completed 屬性

取得或設定當 [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) 啟動的非同步作業完成時叫用的事件處理常式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a>屬性值

事件處理常式。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 

 