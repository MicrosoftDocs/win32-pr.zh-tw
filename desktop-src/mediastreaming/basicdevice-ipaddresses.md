---
title: BasicDevice. IpAddresses 屬性
description: 取得 IP 位址的向量。
ms.assetid: 00096782-E1A8-41A2-86CE-EA2296A1C047
keywords:
- IpAddresses 屬性媒體串流 API
- IpAddresses 屬性媒體串流 API，BasicDevice 介面
- BasicDevice 介面媒體串流 API，IpAddresses 屬性
topic_type:
- apiref
api_name:
- BasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f9b12abfc87420471f8049cbb97cf629a09d17e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681882"
---
# <a name="basicdeviceipaddresses-property"></a>BasicDevice. IpAddresses 屬性

取得 IP 位址的向量。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="property-value"></a>屬性值

IP 位址指標的可列舉集合。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

 