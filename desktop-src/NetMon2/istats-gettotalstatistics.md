---
description: IStats：： GetTotalStatistics 方法-GetTotalStatistics 方法會抓取目前 capture 的統計資料總計。
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: 'IStats：： GetTotalStatistics 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e6566a58212e8f20d0d999302f41ab97cb9f005e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098406"
---
# <a name="istatsgettotalstatistics-method"></a>IStats：： GetTotalStatistics 方法

**GetTotalStatistics** 方法會 [*抓取目前 capture*](c.md)的 [*統計資料總計*](t.md)。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpStats* \[擴展\]
</dt> <dd>

[統計資料](statistics.md)結構的指標，此結構會提供捕獲的統計資料總計。 呼叫端負責配置和釋放 **統計資料** 結構所使用的記憶體。

</dd> <dt>

*fClearAfterReading* \[在\]
</dt> <dd>

用來告訴網路監視器如何處理統計資料總計的內部儲存體的旗標。 設定為 [TRUE] 會告知網路監視器在抓取目前的資訊之後，清除總統計資料的內部儲存體。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                            | Description                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>   | NPP 未連接到網路。 呼叫 [IStats：： connect](istats-connect.md) 方法，將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt> </dl> | NPP 已連接到網路，但不是使用 [IStats：： Connect](istats-connect.md) 方法。<br/>                                |
| <dl> <dt>**NMERR \_ 未 \_ 捕獲**</dt> </dl>   | NPP 不會捕捉資料。 呼叫 [IStats：： start](istats-start.md) 方法以開始捕獲資料。<br/>                         |



 

## <a name="remarks"></a>備註

只有在正在進行捕捉時，此方法才會傳回資料，包括在暫停時暫停。

網路監視器也會儲存 [*對話統計資料*](c.md)，您可以藉由呼叫 [IStats：： GetConversationStatistics](istats-getconversationstatistics.md) 方法來加以取出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats：： Connect](istats-connect.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> <dt>

[IStats：： Start、](istats-start.md)
</dt> <dt>

[統計](statistics.md)
</dt> </dl>

 

 




