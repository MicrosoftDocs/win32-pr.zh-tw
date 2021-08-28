---
title: IMediaRenderer PauseAsync 方法
description: 指示 DMR 以非同步方式暫停播放目前的內容。 |IMediaRenderer PauseAsync 方法
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
keywords:
- PauseAsync 方法媒體串流 API
- PauseAsync 方法媒體串流 API，IMediaRenderer 介面
- IMediaRenderer 介面媒體串流 API，PauseAsync 方法
topic_type:
- apiref
api_name:
- IMediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a953d024ee0f90f7cb466574b29d7e3cfe150072bf1a3787734f8365916cb2a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972267"
---
# <a name="imediarendererpauseasync-method"></a>IMediaRenderer：:P auseAsync 方法

指示 DMR 以非同步方式暫停播放目前的內容。

## <a name="syntax"></a>語法


```C++
HRESULT PauseAsync(
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

 

 





