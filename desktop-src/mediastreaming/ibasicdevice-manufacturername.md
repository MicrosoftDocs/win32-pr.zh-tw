---
title: IBasicDevice ManufacturerName 方法
description: 抓取裝置的製造商名稱。
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- ManufacturerName 方法媒體串流 API
- ManufacturerName 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，ManufacturerName 方法
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 453e11fc547998b6dc3e39017684c30cacd205c0c17b21846925d4de472f43a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011828"
---
# <a name="ibasicdevicemanufacturername-method"></a>IBasicDevice：： ManufacturerName 方法

抓取裝置的製造商名稱。

## <a name="syntax"></a>語法


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收裝置製造商名稱的指標。

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

 

 





