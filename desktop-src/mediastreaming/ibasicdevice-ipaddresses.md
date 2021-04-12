---
title: IBasicDevice IpAddresses 方法
description: 傳回 IP 位址的向量。
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- IpAddresses 方法媒體串流 API
- IpAddresses 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，IpAddresses 方法
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0623b6e2e5d96cb0a400ab1e820424b7eecf46c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373012"
---
# <a name="ibasicdeviceipaddresses-method"></a>IBasicDevice：： IpAddresses 方法

傳回 IP 位址的向量。

## <a name="syntax"></a>語法


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收 IP 位址指標的可列舉集合。

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

 

 





