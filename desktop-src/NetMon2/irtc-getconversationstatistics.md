---
description: IRTC：： GetConversationStatistics 方法-GetConversationStatistics 方法會抓取目前 capture 的會話和站資訊。
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: 'IRTC：： GetConversationStatistics 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4d2476f4eb33d7e74d0de8363fa88d5e688a2e73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110696"
---
# <a name="irtcgetconversationstatistics-method"></a>IRTC：： GetConversationStatistics 方法

**GetConversationStatistics** 方法會抓取目前 capture 的 [*會話*](s.md)和 [*站資訊*](s.md)。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nSessions* \[擴展\]
</dt> <dd>

DWORD 的指標，其中包含記錄給目前 capture 的 [*會話*](s.md) 數目。

</dd> <dt>

*lpSessionStats* \[擴展\]
</dt> <dd>

[SESSIONSTATS](sessionstats.md)結構的指標。

</dd> <dt>

*nStations* \[擴展\]
</dt> <dd>

DWORD 的指標，其中包含記錄給目前 capture 的 [*電臺*](s.md) 數目。

</dd> <dt>

*lpStationStats* \[擴展\]
</dt> <dd>

[STATIONSTATS](stationstats.md)結構的指標。

</dd> <dt>

*fClearAfterReading* \[在\]
</dt> <dd>

用來告知網路監視器在抓取目前資訊之後，清除 [SESSIONSTATS](sessionstats.md) 和 [STATIONSTATS](stationstats.md) 結構內部儲存體的旗標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                                   | Description                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>          | NPP 未連接到網路。 呼叫 [IRTC：： connect](irtc-connect.md) 以將 NPP 連接到網路。<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ 未 \_ 捕獲**</dt> </dl>          | NPP 不會捕捉資料。 呼叫 [IRTC：： start](irtc-start.md) 以開始捕獲。<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ 無法 \_ 即時**</dt> </dl>           | NPP 已連接到網路，但不是使用 [IRTC：： Connect](irtc-connect.md) 方法。<br/>                                                                                                                          |
| <dl> <dt>**NMERR \_ 沒有 \_ 交談 \_ 統計資料**</dt> </dl> | 此連接的設定會設定為 [不儲存對話統計資料]。 若要儲存對話統計資料，請停止 capture，在設定 BLOB 中設定 NoConversationStats = YES，然後重新開機捕獲。<br/> |



 

## <a name="remarks"></a>備註

只有在您要捕獲資料時，才可以呼叫這個方法。如果您在目前的捕獲暫停時呼叫這個方法，方法將會失敗。 若要啟動 capture，請呼叫 [IRTC：： start](irtc-start.md) 方法。

若要取得其他類型的統計資料，請呼叫 [IRTC：： GetTotalStatistics](irtc-gettotalstatistics.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC：： Connect](irtc-connect.md)
</dt> <dt>

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IRTC：： Start](irtc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 




