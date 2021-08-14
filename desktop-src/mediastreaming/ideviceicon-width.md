---
title: IDeviceIcon Width 方法
description: 抓取圖示的寬度（以圖元為單位）。
ms.assetid: 28ADA921-6808-43B8-966E-BA42B1B52931
keywords:
- Width 方法媒體串流 API
- Width 方法媒體串流 API，IDeviceIcon 介面
- IDeviceIcon 介面媒體串流 API，Width 方法
topic_type:
- apiref
api_name:
- IDeviceIcon.Width
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc76fcd7915c350e04cbacfe756e424d31b0d27d5ced38b0ccf8664805fc9bb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473460"
---
# <a name="ideviceiconwidth-method"></a>IDeviceIcon：： Width 方法

抓取圖示的寬度（以圖元為單位）。

## <a name="syntax"></a>語法


```C++
HRESULT Width(
  [out] UINT32 *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收圖示寬度的指標（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

