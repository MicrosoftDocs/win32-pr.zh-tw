---
title: IMediaRenderer IsAudioSupported 方法
description: 抓取值，指出 DMR 是否能夠播放音訊內容。
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- IsAudioSupported 方法媒體串流 API
- IsAudioSupported 方法媒體串流 API，IMediaRenderer 介面
- IMediaRenderer 介面媒體串流 API，IsAudioSupported 方法
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5abe42e65e451464a5f7f3a4d59679db62c3634e95e89e5e275919dd0ece869e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777008"
---
# <a name="imediarendererisaudiosupported-method"></a>IMediaRenderer：： IsAudioSupported 方法

抓取值，指出 DMR 是否能夠播放音訊內容。

## <a name="syntax"></a>語法


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

布林值，如果 DMR 能夠播放音訊內容，則為 **True** ，否則為 **False** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





