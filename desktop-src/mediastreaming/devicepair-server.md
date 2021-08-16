---
title: 'DevicePair 伺服器屬性 (Asptlb .h) '
description: 取得 active basic 裝置配對的伺服器。
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- 伺服器屬性媒體串流 API
- 伺服器屬性媒體串流 API，DevicePair 介面
- DevicePair 介面媒體串流 API，伺服器屬性
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0939a27d96de8f2c8ff53ffd7b0bd766292b873450fb138d0877e916c691f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100722"
---
# <a name="devicepairserver-property"></a>DevicePair：： Server 屬性

取得 active basic 裝置配對的伺服器。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>屬性值

接收代表伺服器裝置的 [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Asptlb。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

