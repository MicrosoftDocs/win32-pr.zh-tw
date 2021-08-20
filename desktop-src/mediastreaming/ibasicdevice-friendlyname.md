---
title: IBasicDevice FriendlyName 方法
description: 抓取裝置的易記名稱。
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- FriendlyName 方法媒體串流 API
- FriendlyName 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，FriendlyName 方法
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35084fafb92b3716208aa6062f065cc4e25a45d2d1a412083076b9e355d2ce43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735608"
---
# <a name="ibasicdevicefriendlyname-method"></a>IBasicDevice：： FriendlyName 方法

抓取裝置的易記名稱。

## <a name="syntax"></a>語法


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收裝置易記名稱的指標。

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

 

 





