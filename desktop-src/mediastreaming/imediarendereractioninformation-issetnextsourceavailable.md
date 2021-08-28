---
title: IMediaRendererActionInformation IsSetNextSourceAvailable 方法
description: 抓取值，這個值表示 DMR 目前是否接受 SetNextSourceFromUriAsync 方法、SetNextSourceFromStreamAsync 方法或 SetNextSourceFromMediaSourceAsync 方法。
ms.assetid: 7588E992-4070-4E0F-8C4B-7DFC097A5076
keywords:
- IsSetNextSourceAvailable 方法媒體串流 API
- IsSetNextSourceAvailable 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，IsSetNextSourceAvailable 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSetNextSourceAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee18eadbc535dd2cd4b48ec6f77adb1d3dec2f5a0c1f5065cee009e27635eda9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092298"
---
# <a name="imediarendereractioninformationissetnextsourceavailable-method"></a>IMediaRendererActionInformation：： IsSetNextSourceAvailable 方法

抓取值，這個值表示 DMR 目前是否接受 [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) 方法、 [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) 方法或 [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT IsSetNextSourceAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

如果 DMR 目前接受 [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync)方法、 [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync)方法或 [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync)方法，則布林值為 **True** ，否則為 **False** 。

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

 

