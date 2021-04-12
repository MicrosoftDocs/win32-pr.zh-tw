---
title: IBasicDevice 類型方法
description: 抓取列舉值，指出 DLNA 裝置的裝置類型。
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- 類型方法媒體串流 API
- 類型方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，類型方法
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a69f0671c82363ff61179c0120b3db8f6e755de9
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383229"
---
# <a name="ibasicdevicetype-method"></a>IBasicDevice：： Type 方法

抓取列舉值，指出 DLNA 裝置的裝置類型。

## <a name="syntax"></a>語法


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收 [**DeviceTypes**](devicetypes.md) 值的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





