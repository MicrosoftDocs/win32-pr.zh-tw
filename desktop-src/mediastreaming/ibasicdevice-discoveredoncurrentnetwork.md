---
title: IBasicDevice DiscoveredOnCurrentNetwork 方法
description: 抓取值，指出裝置是否在目前的網路上。
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- DiscoveredOnCurrentNetwork 方法媒體串流 API
- DiscoveredOnCurrentNetwork 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，DiscoveredOnCurrentNetwork 方法
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e79a012413b3b3d78a9c4617f01ca6cc01cf7e1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104372928"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a>IBasicDevice：:D iscoveredOnCurrentNetwork 方法

抓取值，指出裝置是否在目前的網路上。

## <a name="syntax"></a>語法


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

如果裝置位於目前的網路上 **，則接收** 布林值的指標。

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

 

 





