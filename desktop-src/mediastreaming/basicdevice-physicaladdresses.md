---
title: BasicDevice. PhysicalAddresses 屬性
description: 取得實體位址的向量。
ms.assetid: E9D86D13-8DD4-40BA-8608-54F8B3832E05
keywords:
- PhysicalAddresses 屬性媒體串流 API
- PhysicalAddresses 屬性媒體串流 API，BasicDevice 介面
- BasicDevice 介面媒體串流 API，PhysicalAddresses 屬性
topic_type:
- apiref
api_name:
- BasicDevice.PhysicalAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93f5517008d4195dace53d77a8f9a4f6ca4f50aa704e52540ffbf2553aa76c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236601"
---
# <a name="basicdevicephysicaladdresses-property"></a>BasicDevice. PhysicalAddresses 屬性

取得實體位址的向量。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_PhysicalAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="property-value"></a>屬性值

實體位址指標的可列舉集合。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

 