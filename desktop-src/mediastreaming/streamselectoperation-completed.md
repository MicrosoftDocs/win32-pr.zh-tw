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
# <a name="streamselectoperationcompleted-property"></a>StreamSelectOperation。 Completed 屬性

取得或設定當 [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) 啟動的非同步作業完成時叫用的事件處理常式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a>屬性值

事件處理常式。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

 