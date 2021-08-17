---
title: IMediaRendererActionInformation IsPauseAvailable 方法
description: 抓取值，這個值表示 DMR 目前是否接受 PauseAsync 方法。
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- IsPauseAvailable 方法媒體串流 API
- IsPauseAvailable 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，IsPauseAvailable 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fad69863306a8a937771f16c2ab9a83a2622c571d2cd5ee5658a279bf7564132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870845"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a>IMediaRendererActionInformation：： IsPauseAvailable 方法

抓取值，這個值表示 DMR 目前是否接受 [**PauseAsync**](imediarenderer-pauseasync.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

如果 DMR 目前接受 [**PauseAsync**](imediarenderer-pauseasync.md)方法，則布林值為 **True** ，否則為 **False** 。

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

 

