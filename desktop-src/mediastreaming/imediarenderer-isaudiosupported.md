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
ms.openlocfilehash: 4f7670d0a2818cf5518bee0b2586531caeea20fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965614"
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



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





