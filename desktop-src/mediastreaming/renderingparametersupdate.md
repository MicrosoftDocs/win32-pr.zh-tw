---
title: RenderingParametersUpdate 事件
description: 每當 DMR 上有任何一組轉譯控制項參數進行更新時發生。
ms.assetid: 863ca879-a420-43d6-9ac8-94f8303bb759
keywords:
- RenderingParametersUpdate 事件媒體串流 API
topic_type:
- apiref
api_name:
- RenderingParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08956baf37b0bf8bc2323138e5cad24d587a88af7283d52985559a8a8538571d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342928"
---
# <a name="renderingparametersupdate-event"></a>RenderingParametersUpdate 事件

每當 DMR 上有任何一組轉譯控制項參數進行更新時發生。

## <a name="syntax"></a>語法


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

若要處理此事件的通知，請使用 [**add \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate)方法來註冊 [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))事件處理常式函式。 若要取消註冊事件處理常式，請使用 [**remove \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) 方法。

 

 