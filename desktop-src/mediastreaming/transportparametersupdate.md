---
title: TransportParametersUpdate 事件
description: 當 DMR 上有任何一組傳輸參數更新時發生。
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- TransportParametersUpdate 事件媒體串流 API
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e3a600b7345b2cf05b5fb76f20b968e1af9ddecfb72f8442ada34dfd98ae3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034516"
---
# <a name="transportparametersupdate-event"></a>TransportParametersUpdate 事件

當 DMR 上有任何一組傳輸參數更新時發生。

## <a name="syntax"></a>語法


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

若要處理此事件的通知，請使用 [**add \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate)方法來註冊 [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))事件處理常式函式。 若要取消註冊事件處理常式，請使用 [**remove \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) 方法。

 

 