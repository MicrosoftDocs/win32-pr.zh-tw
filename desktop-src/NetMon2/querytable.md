---
description: 此資料表結構會提供目前使用網路監視器來捕捉網路資料的電腦清單。
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: " (Netmon .h 的) 的"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 9b8f291f055bfba159309b6c75a54d95514ed9c7614eb0456a4870e657f04209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555368"
---
# <a name="querytable-structure"></a>的

此 **資料表結構會** 提供目前使用網路監視器來捕捉網路資料的電腦清單。

## <a name="syntax"></a>語法


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a>成員

<dl> <dt>

**nStationQueries**
</dt> <dd>

輸入時，您要網路監視器傳回的電腦數目上限。

在輸出時，網路監視器所傳回的 [STATIONQUERY](stationquery.md) 結構數目。 每個 **STATIONQUERY** 結構都代表目前正在捕獲資料的電腦。

</dd> <dt>

**StationQuery**
</dt> <dd>

在輸入時，為空白 [STATIONQUERY](stationquery.md) 結構的陣列，其中包含在 **nStationQueries** 中指定的元素數目。

在輸出時，為正在捕捉資料的每部電腦填入已填滿的 [STATIONQUERY](stationquery.md) 結構。 **NStationQueries** 會傳回已填滿的元素數目。

</dd> </dl>

## <a name="remarks"></a>備註

此結構和 [STATIONQUERY](stationquery.md) 陣列的記憶體必須由呼叫應用程式佈建，並在不再需要資訊之後釋放。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDelaydC::QueryStations](idelaydc-querystations.md)
</dt> <dt>

[IESP::QueryStations](iesp-querystations.md)
</dt> <dt>

[IRTC::QueryStations](irtc-querystations.md)
</dt> <dt>

[IStats::QueryStations](istats-querystations.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




