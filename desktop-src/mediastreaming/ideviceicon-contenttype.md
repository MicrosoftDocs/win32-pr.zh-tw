---
title: IDeviceIcon ContentType 方法
description: 抓取圖示的內容類型。
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- ContentType 方法媒體串流 API
- ContentType 方法媒體串流 API，IDeviceIcon 介面
- IDeviceIcon 介面媒體串流 API，ContentType 方法
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8fb9cb639381b60bb59965d12ce3f0545daf6d2725cde69d3dea3dee589f8f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461740"
---
# <a name="ideviceiconcontenttype-method"></a>IDeviceIcon：： ContentType 方法

抓取圖示的內容類型。

## <a name="syntax"></a>語法


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收圖示內容類型的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

