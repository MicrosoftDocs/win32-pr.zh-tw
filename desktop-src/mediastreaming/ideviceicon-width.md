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
ms.openlocfilehash: 4b04f8c40cc209ccf1261af0fc2f6cdfd329db88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315082"
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

 

