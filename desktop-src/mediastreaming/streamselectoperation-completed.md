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
ms.openlocfilehash: 554874c19054f4b2ee46fbfe29fb4dfb8149e476ff96d040ffdbdd9b39de4612
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847578"
---
# <a name="streamselectoperationcompleted-property"></a>StreamSelectOperation。 Completed 屬性

取得或設定當 [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) 啟動的非同步作業完成時叫用的事件處理常式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a>屬性值

事件處理常式。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

 