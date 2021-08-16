---
title: IMediaRendererActionInformation IsSeekAvailable 方法
description: 抓取值，這個值表示 DMR 目前是否接受 SeekAsync 方法。
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- IsSeekAvailable 方法媒體串流 API
- IsSeekAvailable 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，IsSeekAvailable 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32b5c7eef78dad4ebfeeebb40c323d7b13e540033eb54852f7da41942f5ec83e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735511"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a>IMediaRendererActionInformation：： IsSeekAvailable 方法

抓取值，這個值表示 DMR 目前是否接受 [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

如果 DMR 目前接受 [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync)方法，則布林值為 **True** ，否則為 **False** 。

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

 

