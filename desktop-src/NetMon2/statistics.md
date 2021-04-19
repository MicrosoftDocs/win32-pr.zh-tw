---
description: 統計資料結構會提供 capture 的統計資料。 其中某些統計資料是由網路監視器產生的，有些則是由 NPP 所連接的 NIC 所產生。
ms.assetid: 5e30ae30-d8ad-4336-9e4d-fa10ceefc966
title: " (Netmon. h) 的統計資料結構"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATISTICS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a3798f32f7341722432441272eded7d7605cf8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981521"
---
# <a name="statistics-structure"></a>統計資料結構

**統計資料** 結構會提供 capture 的統計資料。 其中某些統計資料是由網路監視器產生的，有些則是由 NPP 所連接的 NIC 所產生。

## <a name="syntax"></a>語法


```C++
typedef struct _STATISTICS {
  __int64 TimeElapsed;
  DWORD   TotalFramesCaptured;
  DWORD   TotalBytesCaptured;
  DWORD   TotalFramesFiltered;
  DWORD   TotalBytesFiltered;
  DWORD   TotalMulticastsFiltered;
  DWORD   TotalBroadcastsFiltered;
  DWORD   TotalFramesSeen;
  DWORD   TotalBytesSeen;
  DWORD   TotalMulticastsReceived;
  DWORD   TotalBroadcastsReceived;
  DWORD   TotalFramesDropped;
  DWORD   TotalFramesDroppedFromBuffer;
  DWORD   MacFramesReceived;
  DWORD   MacCRCErrors;
  __int64 MacBytesReceivedEx;
  DWORD   MacFramesDropped_NoBuffers;
  DWORD   MacMulticastsReceived;
  DWORD   MacBroadcastsReceived;
  DWORD   MacFramesDropped_HwError;
} STATISTICS, *LPSTATISTICS;
```



## <a name="members"></a>成員

<dl> <dt>

**>timeelapsed**
</dt> <dd>

經過時間（以微秒為單位）。

</dd> <dt>

**TotalFramesCaptured**
</dt> <dd>

目前儲存的框架總數。 此數目受限於用來儲存框架的捕獲檔案或緩衝區大小。

</dd> <dt>

**TotalBytesCaptured**
</dt> <dd>

目前儲存的位元組總數。 此數目受限於用來儲存框架的捕獲檔案或緩衝區大小。

</dd> <dt>

**TotalFramesFiltered**
</dt> <dd>

透過目前的捕獲篩選準則傳遞的框架總數。 如果未使用篩選，此值與 **TotalFramesSeen** 相同。

</dd> <dt>

**TotalBytesFiltered**
</dt> <dd>

透過目前的捕獲篩選準則傳遞的框架總數。 如果未使用篩選，此值與 **TotalBytesSeen** 相同。

</dd> <dt>

**TotalMulticastsFiltered**
</dt> <dd>

這個成員已過時。

</dd> <dt>

**TotalBroadcastsFiltered**
</dt> <dd>

這個成員已過時。

</dd> <dt>

**TotalFramesSeen**
</dt> <dd>

NIC 所處理的框架總數。

</dd> <dt>

**TotalBytesSeen**
</dt> <dd>

NIC 所處理的總位元組數。

</dd> <dt>

**TotalMulticastsReceived**
</dt> <dd>

這個成員已過時。

</dd> <dt>

**TotalBroadcastsReceived**
</dt> <dd>

這個成員已過時。

</dd> <dt>

**TotalFramesDropped**
</dt> <dd>

傳遞篩選但未) 儲存的框架 (框架的總頁數。

</dd> <dt>

**TotalFramesDroppedFromBuffer**
</dt> <dd>

從捕獲檔案或緩衝區卸載的框架數。 當緩衝區已滿時，會移除舊的框架，以騰出空間給新的框架。

</dd> <dt>

**MacFramesReceived**
</dt> <dd>

NIC 回報已接收的框架數目。

</dd> <dt>

**MacCRCErrors**
</dt> <dd>

NIC 回報的 CRC 錯誤數目。

</dd> <dt>

**MacBytesReceivedEx**
</dt> <dd>

NIC 回報收到的位元組數目。

</dd> <dt>

**MacFramesDropped \_ NoBuffers**
</dt> <dd>

NIC 回報因為缺少緩衝區空間而捨棄的框架數目。

</dd> <dt>

**MacMulticastsReceived**
</dt> <dd>

NIC 報告收到的多播數目。

</dd> <dt>

**MacBroadcastsReceived**
</dt> <dd>

收到的 NIC 報告廣播數目。

</dd> <dt>

**MacFramesDropped \_ HwError**
</dt> <dd>

NIC 回報因硬體錯誤而捨棄的畫面格數。

</dd> </dl>

## <a name="remarks"></a>備註

此結構是用來取出 [*總計統計資料*](t.md)，以及暫停或停止目前的捕獲。

使用 [IESP](iesp.md) NPP 介面時，無法取出統計資料總計。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IStats::GetTotalStatistics](istats-gettotalstatistics.md)
</dt> <dt>

[IDelaydC：:P ause](idelaydc-pause.md)
</dt> <dt>

[IESP：:P ause](iesp-pause.md)
</dt> <dt>

[IRTC：:P ause](irtc-pause.md)
</dt> <dt>

[IStats：:P ause](istats-pause.md)
</dt> <dt>

[IDelaydC：： Stop](idelaydc-stop.md)
</dt> <dt>

[IESP：： Stop](iesp-stop.md)
</dt> <dt>

[IRTC：： Stop](irtc-stop.md)
</dt> <dt>

[IStatsC：： Stop](istats-stop.md)
</dt> </dl>

 

 




