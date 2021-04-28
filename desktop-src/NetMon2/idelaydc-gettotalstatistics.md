---
description: IDelaydC：： GetTotalStatistics 方法-GetTotalStatistics 方法會抓取目前 capture 的統計資料總計。
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: 'IDelaydC：： GetTotalStatistics 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b3a0ce4f230236e276fede528a5e778ecafd51fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113526"
---
# <a name="idelaydcgettotalstatistics-method"></a>IDelaydC：： GetTotalStatistics 方法

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

用來告訴網路監視器如何處理統計資料總計的內部儲存體的旗標。 設定為 [ **TRUE** ] 會告知網路監視器在抓取目前的資訊之後，清除總統計資料的內部儲存體。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                          | Description                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl> | NPP 未連接到網路。 呼叫 [IDelaydC：： connect](idelaydc-connect.md) 以連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 未 \_ 延遲**</dt> </dl>   | NPP 已連接到網路，但不是使用 [IDelaydC：： Connect](idelaydc-connect.md) 方法。<br/>             |
| <dl> <dt>**NMERR \_ 未 \_ 捕獲**</dt> </dl> | NPP 不會捕捉資料。 呼叫 [IDelaydC：： start](idelaydc-start.md) 以開始捕獲資料。<br/>                 |



 

## <a name="remarks"></a>備註

只有在正在進行捕捉時，此方法才會傳回資料;當捕捉暫停時，對此方法的呼叫將不會成功。

網路監視器也會儲存 [*對話統計資料*](c.md)，您可以藉由呼叫 [IDelaydC：： GetConversationStatistics](idelaydc-getconversationstatistics.md) 方法來加以取出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC：： Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IDelaydC：： Start](idelaydc-start.md)
</dt> <dt>

[統計](statistics.md)
</dt> </dl>

 

 




