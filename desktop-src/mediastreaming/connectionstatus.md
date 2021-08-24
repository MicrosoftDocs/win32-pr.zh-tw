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
ms.openlocfilehash: 8617012abe75d213e0de7be70811152315a888693c7336ef58cd34ceb98eba55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721248"
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
| IDL<br/> | <dl> <dt>Windows。 (參考 Windows 的參考。) 的串流 .idl</dt> </dl> |



 

 





