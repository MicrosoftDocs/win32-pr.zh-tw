---
title: IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync 方法
description: 以非同步方式建立物件的新實例，這個實例會使用指定的 IBasicDevice 介面來執行 IMediaRenderer 介面。
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- CreateMediaRendererFromBasicDeviceAsync 方法媒體串流 API
- CreateMediaRendererFromBasicDeviceAsync 方法媒體串流 API，IMediaRendererFactory 介面
- IMediaRendererFactory 介面媒體串流 API，CreateMediaRendererFromBasicDeviceAsync 方法
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b9ee80a4f681bb57d62f84d35cf3a254e38982a10f642a35e35187f6af9e48e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092287"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a>IMediaRendererFactory：： CreateMediaRendererFromBasicDeviceAsync 方法

以非同步方式建立物件的新實例，這個實例會使用指定的 [**IBasicDevice**](ibasicdevice.md)介面來執行 [**IMediaRenderer**](imediarenderer.md)介面。

## <a name="syntax"></a>語法


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*basicDevice* \[在\]
</dt> <dd>

[**IBasicDevice**](ibasicdevice.md)介面的指標，代表將建立 [**IMediaRenderer**](imediarenderer.md)實例的裝置。

</dd> <dt>

*值* \[退出，retval\]
</dt> <dd>

接收 [**CreateMediaRendererOperation**](createmediarendereroperation.md) 物件的參考，這個物件是用來從非同步作業取得結果。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

