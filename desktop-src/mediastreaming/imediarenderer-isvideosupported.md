---
title: IMediaRenderer IsVideoSupported 方法
description: 抓取值，指出 DMR 是否能夠播放影片內容。
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- IsVideoSupported 方法媒體串流 API
- IsVideoSupported 方法媒體串流 API，IMediaRenderer 介面
- IMediaRenderer 介面媒體串流 API，IsVideoSupported 方法
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c1f6fa149c6c5025d3fd2c785dc2f4a8451fabed3906b559674d8038662c21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972307"
---
# <a name="imediarendererisvideosupported-method"></a>IMediaRenderer：： IsVideoSupported 方法

抓取值，指出 DMR 是否能夠播放影片內容。

## <a name="syntax"></a>語法


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

布林值，如果 DMR 能夠播放影片內容則為 **True** ，否則為 **False** 。

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

 

 





