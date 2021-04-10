---
description: STATIONSTATS 結構會提供目前 capture 所描述之特定工作站的相關統計資料。
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: 'STATIONSTATS 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026558"
---
# <a name="stationstats-structure"></a>STATIONSTATS 結構

**STATIONSTATS** 結構會提供目前 capture 所描述之特定 [*工作站*](s.md)的相關統計資料。

## <a name="syntax"></a>語法


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a>成員

<dl> <dt>

**NextStationStats**
</dt> <dd>

**STATIONSTATS** 結構陣列中記錄的下一個站索引。

</dd> <dt>

**SessionPartnerList**
</dt> <dd>

站夥伴清單的索引。

</dd> <dt>

**旗標**
</dt> <dd>

這個成員已過時。

</dd> <dt>

**StationAddress**
</dt> <dd>

工作站的 MAC 位址。

</dd> <dt>

**墊**
</dt> <dd>

**DWORD** 對齊。

</dd> <dt>

**TotalPacketsReceived**
</dt> <dd>

傳送至工作站的封包總數。

</dd> <dt>

**TotalDirectedPacketsSent**
</dt> <dd>

站送出的導向封包總數。

</dd> <dt>

**TotalBroadcastPacketsSent**
</dt> <dd>

廣播導向封包總數 (MAC 位址 FF FF ff ff ff ff) 由工作站傳送。

</dd> <dt>

**TotalMulticastPacketsSent**
</dt> <dd>

目的地位址中設定的多播封包總數 (群組位) 由工作站傳送。

</dd> <dt>

**TotalBytesReceived**
</dt> <dd>

傳送至工作站的位元組總數。

</dd> <dt>

**TotalBytesSent**
</dt> <dd>

工作站傳送的位元組總數。

</dd> </dl>

## <a name="remarks"></a>備註

網路監視器會將會話和站資訊儲存在兩個相關聯的陣列中。 其元素分別為 [SESSIONSTATS](sessionstats.md) 和 **STATIONSTATS** 結構。 這些結構的成員可以用來在兩者之間進行導覽。 例如，若要移至下一個站，請使用 **NextStationStats**。 若要跳至 SESSIONSTATS 陣列中的會話夥伴清單，請使用 **SessionPartnerList** 中提供的索引。

> [!Note]  
> **STATIONSTATS** 陣列包含目前捕獲期間使用的每個工作站的元素。 網路監視器用來將專案加入至這個陣列的演算法，是以最有效率的方式，在進行捕獲時記錄資訊。 因此，下一個站不一定是陣列中的下一個元素。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> </dl>

 

 




