---
title: GetPositionInformationOperation。 Completed 屬性
description: 取得或設定當 GetPositionInformationAsync 啟動的非同步作業完成時叫用的事件處理常式。
ms.assetid: 144065AE-6C23-4E9D-B9D0-6849E7FB74C4
keywords:
- 完成的屬性媒體串流 API
- 完成的屬性媒體串流 API、GetPositionInformationOperation 介面
- GetPositionInformationOperation 介面媒體串流 API，已完成屬性
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90b4ed4a6402b8c7bfc1ee559bd0b43765a64cec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375249"
---
# <a name="getpositioninformationoperationcompleted-property"></a>GetPositionInformationOperation。 Completed 屬性

取得或設定當 [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) 啟動的非同步作業完成時叫用的事件處理常式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  GetPositionInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetPositionInformationCompletedHandler **value
);
```



## <a name="property-value"></a>屬性值

事件處理常式。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetPositionInformationOperation**](getpositioninformationoperation.md)
</dt> </dl>

 

 