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
# <a name="getstreampropertiesoperationcompleted-property"></a>GetStreamPropertiesOperation。 Completed 屬性

取得或設定當 [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) 啟動的非同步作業完成時叫用的事件處理常式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a>屬性值

事件處理常式。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetStreamPropertiesOperation**](getstreampropertiesoperation.md)
</dt> </dl>

 

 