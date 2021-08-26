---
description: SESSIONSTATS 結構提供會話的相關統計資料。
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: 'SESSIONSTATS 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 231c94d2abda40974249f6c3cc82c8efc7518cb21d5881f44e63f647bcb21de2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128828"
---
# <a name="sessionstats-structure"></a>SESSIONSTATS 結構

**SESSIONSTATS** 結構提供 [*會話*](s.md)的相關統計資料。

## <a name="syntax"></a>語法


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a>成員

<dl> <dt>

**NextSession**
</dt> <dd>

站擁有者下一個會話的索引。

</dd> <dt>

**StationOwner**
</dt> <dd>

關聯 [STATIONSTATS](stationstats.md) 結構陣列中的擁有者站索引。 擁有者工作站是起始會話的站，也就是傳送會話封包的站。

</dd> <dt>

**StationPartner**
</dt> <dd>

相關聯之 [STATIONSTATS](stationstats.md) 結構陣列內其他站的索引。 夥伴工作站是接收會話封包的站。

</dd> <dt>

**旗標**
</dt> <dd>

這個成員已過時。

</dd> <dt>

**TotalPacketsSent**
</dt> <dd>

會話中傳送的封包數目。

</dd> </dl>

## <a name="remarks"></a>備註

網路監視器會將會話和站資訊儲存在兩個相關聯的陣列中，其元素分別為 **SESSIONSTATS** 和 [STATIONSTATS](stationstats.md) 結構。 這些結構的成員可以用來在兩者之間進行導覽。 例如，若要移至特定工作站擁有者的下一個會話，請使用 **NextSession**。 若要跳至 STATIONSTATS 陣列中會話的擁有者和夥伴站，請使用 **StationOwner** 和 **StationPartner** 中提供的索引。

> [!Note]  
> SESSIONSTATS 陣列包含目前 capture 中每個會話的元素。 網路監視器用來將專案新增至 SESSIONSTATS 陣列的演算法，會根據在進行中時，有效率地記錄資訊。 因此，特定擁有者工作站的下一個會話不一定是陣列中的下一個元素。

 

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

 

 




