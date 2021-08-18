---
title: IMediaRendererActionInformation IsVolumeAvailable 方法
description: 抓取指出 DMR 是否能夠調整音訊音量層級的值。
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- IsVolumeAvailable 方法媒體串流 API
- IsVolumeAvailable 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，IsVolumeAvailable 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce36a9151998a5f7b0a7785aebc1795bd29d31ff47cfdd2368978ad040f3597c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972207"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a>IMediaRendererActionInformation：： IsVolumeAvailable 方法

抓取指出 DMR 是否能夠調整音訊音量層級的值。

## <a name="syntax"></a>語法


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

布林值，如果 DMR 能夠調整音訊音量層級，則為 **True** ，否則為 **False** 。

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

 

