---
title: IMediaRenderer StopAsync 方法
description: 指示 DMR 以非同步方式停止播放目前的內容。 |IMediaRenderer StopAsync 方法
ms.assetid: B6B0F3F2-E95E-4A58-9CBD-CF4CB24FDAD0
keywords:
- StopAsync 方法媒體串流 API
- StopAsync 方法媒體串流 API，IMediaRenderer 介面
- IMediaRenderer 介面媒體串流 API，StopAsync 方法
topic_type:
- apiref
api_name:
- IMediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 802821e909f5882e4f7a7c64ea824fc36d1801748c763b56ee7878b680c3c0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871102"
---
# <a name="imediarendererstopasync-method"></a>IMediaRenderer：： StopAsync 方法

指示 DMR 以非同步方式停止播放目前的內容。

## <a name="syntax"></a>語法


```C++
HRESULT StopAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收 [**PlaybackOperation**](playbackoperation.md) 物件的參考，這個物件是用來從非同步作業取得結果。

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

 

 





