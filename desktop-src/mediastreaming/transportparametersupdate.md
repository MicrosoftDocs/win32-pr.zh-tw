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
ms.openlocfilehash: 58df04862275af5da8714f8a954dc5b127f833f2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842248"
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

 

 