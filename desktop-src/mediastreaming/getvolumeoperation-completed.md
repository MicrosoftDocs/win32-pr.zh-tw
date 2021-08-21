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
ms.openlocfilehash: 84668f41f12c4920ec45bf70a3a931e6fc9234e213fe0a359ab93f3e34aac724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735754"
---
# <a name="getvolumeoperationcompleted-property"></a>GetVolumeOperation。 Completed 屬性

取得或設定當 [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) 啟動的非同步作業完成時叫用的事件處理常式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  GetVolumeCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetVolumeCompletedHandler **value
);
```



## <a name="property-value"></a>屬性值

事件處理常式。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetVolumeOperation**](getvolumeoperation.md)
</dt> </dl>

 

 