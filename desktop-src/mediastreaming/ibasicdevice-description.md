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
ms.openlocfilehash: cfaf3ba8ca9c74d094aa8cdc15f4c190d6e5141fb11ff255b6e7682b667846d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972347"
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



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





