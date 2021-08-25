---
title: IBasicDevice ModelUrl 方法
description: 抓取裝置的模型 URL。
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- ModelUrl 方法媒體串流 API
- ModelUrl 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，ModelUrl 方法
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7595af295b0d0bc565d79bf5450ee6c5c16b0da4f3baa4fcf636e4e5386920
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847648"
---
# <a name="ibasicdevicemodelurl-method"></a>IBasicDevice：： ModelUrl 方法

抓取裝置的模型 URL。

## <a name="syntax"></a>語法


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收裝置的模型 URL 指標。

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

 

 





