---
title: MediaRenderer. StopAsync 方法
description: 指示 DMR 以非同步方式停止播放目前的內容。 |MediaRenderer. StopAsync 方法
ms.assetid: 04cf6d5a-8aa5-4821-8117-f250bfaf7ebd
keywords:
- StopAsync 方法媒體串流 API
- StopAsync 方法媒體串流 API，MediaRenderer 介面
- MediaRenderer 介面媒體串流 API，StopAsync 方法
topic_type:
- apiref
api_name:
- MediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 205c69a83572539974c1b8ad2cf45159c45335cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104116145"
---
# <a name="mediarendererstopasync-method"></a>MediaRenderer. StopAsync 方法

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



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 





