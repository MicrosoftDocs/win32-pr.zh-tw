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
ms.openlocfilehash: eec2c28e8118f6cf11e89c7ab4a5ba04abd8b8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977144"
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

 

