---
title: ITransportParameters Actioninformation .action 方法
description: 取得 IMediaRendererActionInformation 介面，以提供目前可在 DMR 上叫用之方法的相關資訊。
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- Actioninformation .action 方法媒體串流 API
- Actioninformation .action 方法媒體串流 API，ITransportParameters 介面
- ITransportParameters 介面媒體串流 API，Actioninformation .action 方法
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 551612fcaffb9379823efea15f29ed9feba1ff3d0c5af6e7271b61ad9d6036f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235853"
---
# <a name="itransportparametersactioninformation-method"></a>ITransportParameters：： Actioninformation .action 方法

取得 [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) 介面，以提供目前可在 DMR 上叫用之方法的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[退出，retval\]
</dt> <dd>

接收 [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) 介面的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

