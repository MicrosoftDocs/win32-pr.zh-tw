---
description: 抓取目前 capture 的會話和工作站資訊。
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: 'IStats：： GetConversationStatistics 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8e76bad23d79e261a27df5b83a94d4e477b21cde5057bb2587ffb49c93382df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890338"
---
# <a name="istatsgetconversationstatistics-method"></a>IStats：： GetConversationStatistics 方法

**GetConversationStatistics** 方法會抓取目前 capture 的會話和站資訊。

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

[**SESSIONSTATS**](sessionstats.md)結構的指標。

</dd> <dt>

*nStations* \[擴展\]
</dt> <dd>

DWORD 的指標，其中包含記錄給目前 capture 的 [*電臺*](s.md) 數目。

</dd> <dt>

*lpStationStats* \[擴展\]
</dt> <dd>

[**STATIONSTATS**](stationstats.md)結構的指標。

</dd> <dt>

*fClearAfterReading* \[在\]
</dt> <dd>

用來指示網路監視器在抓取目前的資料之後，清除 [**SESSIONSTATS**](sessionstats.md) 和 [**STATIONSTATS**](stationstats.md) 結構內部儲存的旗標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                                   | 描述                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>          | NPP 未連接到網路。 呼叫 [**IStats：：連線**](istats-connect.md)將 NPP 連接到網路。<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ 未 \_ 捕獲**</dt> </dl>          | NPP 不會捕捉資料。 呼叫 [**IStats：： start**](istats-start.md) 以開始捕獲。<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt> </dl>        | NPP 會連接到網路，但不會使用 [**IStats：：連線**](istats-connect.md)方法。<br/>                                                                                                                         |
| <dl> <dt>**NMERR \_ 沒有 \_ 交談 \_ 統計資料**</dt> </dl> | 此連接的設定會設定為 [不儲存對話統計資料]。 若要儲存對話統計資料，請停止 capture，在設定 BLOB 中設定 **NoConversationStats = YES** ，然後重新開機 capture。<br/> |



 

## <a name="remarks"></a>備註

只有在資料捕獲進行中時，才可以呼叫此方法;當目前的捕獲暫停時，對此方法的呼叫將不會成功。

若要啟動 capture，請呼叫 [**IStats：： start**](istats-start.md) 方法。 若要取得其他類型的統計資料，請呼叫 [**IStats：： GetTotalStatistics**](istats-gettotalstatistics.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats::GetTotalStatistics**](istats-gettotalstatistics.md)
</dt> <dt>

[**IStats：： Start**](istats-start.md)
</dt> <dt>

[**IStats：：連線**](istats-connect.md)
</dt> <dt>

[**SESSIONSTATS**](sessionstats.md)
</dt> <dt>

[**STATIONSTATS**](stationstats.md)
</dt> </dl>

 

 




