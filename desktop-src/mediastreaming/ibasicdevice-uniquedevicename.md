---
title: IBasicDevice UniqueDeviceName 方法
description: 抓取裝置的唯一裝置名稱 (UDN) 。
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- UniqueDeviceName 方法媒體串流 API
- UniqueDeviceName 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，UniqueDeviceName 方法
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b70fbc2021cf717cdb49d8a222aa33ad4e9213f297364b81af065c3bbeaed99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972317"
---
# <a name="ibasicdeviceuniquedevicename-method"></a>IBasicDevice：： UniqueDeviceName 方法

抓取裝置的唯一裝置名稱 (UDN) 。

## <a name="syntax"></a>語法


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收裝置 s 模型 UDN 的指標。

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

 

 





