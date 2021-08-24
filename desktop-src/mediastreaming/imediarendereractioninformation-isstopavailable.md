---
title: IMediaRendererActionInformation IsStopAvailable 方法
description: 抓取值，這個值表示 DMR 目前是否接受 StopAsync 方法。
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- IsStopAvailable 方法媒體串流 API
- IsStopAvailable 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，IsStopAvailable 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c177c46c62309525d9362f985075cec293105a80678b3b857eafa0524179d17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712888"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a>IMediaRendererActionInformation：： IsStopAvailable 方法

抓取值，這個值表示 DMR 目前是否接受 [**StopAsync**](imediarenderer-stopasync.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

如果 DMR 目前接受 [**StopAsync**](imediarenderer-stopasync.md)方法，則布林值為 **True** ，否則為 **False** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

