---
title: ConnectionStatus 列舉
description: 表示網路中的裝置在上一次看到的狀態。
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- ConnectionStatus 列舉媒體串流 API
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985765"
---
# <a name="connectionstatus-enumeration"></a>ConnectionStatus 列舉

表示網路中的裝置在上一次看到的狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**線上**
</dt> <dd>

裝置處於線上狀態且在網路上作用中。

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線**
</dt> <dd>

裝置已離線。

</dd> <dt>

<span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**睡覺**
</dt> <dd>

裝置目前為離線狀態，但可能會在嘗試與其進行通訊時自動喚醒。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt> (參考) 的 windows...。 </dt> </dl> |



 

 





