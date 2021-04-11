---
title: IBasicDevice Description 方法
description: 抓取裝置的描述。
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- 描述方法媒體串流 API
- Description 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，Description 方法
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f094246d1424c458e624d4a49358b63a84b9b7d2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022348"
---
# <a name="ibasicdevicedescription-method"></a>IBasicDevice：:D 描述 e) 方法

抓取裝置的描述。

## <a name="syntax"></a>語法


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收裝置描述的指標。

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

 

 





