---
title: IBasicDevice SerialNumber 方法
description: 抓取裝置序號。
ms.assetid: 238A5999-0E8B-4462-AFCF-790DB58CFCB4
keywords:
- SerialNumber 方法媒體串流 API
- SerialNumber 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，SerialNumber 方法
topic_type:
- apiref
api_name:
- IBasicDevice.SerialNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37a4985754982b8b64246d8d0d0fac0d2c37f4a37f159d2e5087497442c97a75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712938"
---
# <a name="ibasicdeviceserialnumber-method"></a>IBasicDevice：： SerialNumber 方法

抓取裝置序號。

## <a name="syntax"></a>語法


```C++
HRESULT SerialNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收裝置序號的指標。

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

 

 





