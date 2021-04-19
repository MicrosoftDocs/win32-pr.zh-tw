---
title: IBasicDevice ModelName 方法
description: 抓取裝置的模型名稱。
ms.assetid: 8F871E89-97C1-4788-83AB-B7E0D8D6E0B5
keywords:
- ModelName 方法媒體串流 API
- ModelName 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，ModelName 方法
topic_type:
- apiref
api_name:
- IBasicDevice.ModelName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e486b372b2108bc85153f416032ef6bfbe8a397
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106996157"
---
# <a name="ibasicdevicemodelname-method"></a>IBasicDevice：： ModelName 方法

抓取裝置的模型名稱。

## <a name="syntax"></a>語法


```C++
HRESULT ModelName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收裝置 s 模型名稱的指標。

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

 

 





