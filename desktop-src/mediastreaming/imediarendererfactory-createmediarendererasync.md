---
title: IMediaRendererFactory CreateMediaRendererAsync 方法
description: 以非同步方式建立物件的新實例，這個實例會使用指定的唯一裝置名稱（ (UDN) ）來執行 IMediaRenderer 介面。
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- CreateMediaRendererAsync 方法媒體串流 API
- CreateMediaRendererAsync 方法媒體串流 API，IMediaRendererFactory 介面
- IMediaRendererFactory 介面媒體串流 API，CreateMediaRendererAsync 方法
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682003"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a>IMediaRendererFactory：： CreateMediaRendererAsync 方法

以非同步方式建立物件的新實例，這個實例會使用指定的唯一裝置名稱（ (UDN) ）來執行 [**IMediaRenderer**](imediarenderer.md) 介面。

## <a name="syntax"></a>語法


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*deviceIdentifier* \[在\]
</dt> <dd>

包含 UDN 的 HSTRING，此會識別要建立 [**IMediaRenderer**](imediarenderer.md) 實例的 DLNA DMR 裝置。

</dd> <dt>

*值* \[退出，retval\]
</dt> <dd>

接收 [**CreateMediaRendererOperation**](createmediarendereroperation.md) 物件的參考，這個物件是用來從非同步作業取得結果。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

