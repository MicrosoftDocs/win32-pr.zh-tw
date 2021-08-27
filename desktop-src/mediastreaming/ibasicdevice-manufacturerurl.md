---
title: IBasicDevice ManufacturerUrl 方法
description: 抓取裝置的製造商 URL。
ms.assetid: E8372D15-D8B5-49E4-950A-96B4A88B0450
keywords:
- ManufacturerUrl 方法媒體串流 API
- ManufacturerUrl 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，ManufacturerUrl 方法
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 306b4c194d7354b071d4daaf223a17f977b38b44243adaef856f9acffbf49c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972337"
---
# <a name="ibasicdevicemanufacturerurl-method"></a>IBasicDevice：： ManufacturerUrl 方法

抓取裝置的製造商 URL。

## <a name="syntax"></a>語法


```C++
HRESULT ManufacturerUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收裝置製造商 URL 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





