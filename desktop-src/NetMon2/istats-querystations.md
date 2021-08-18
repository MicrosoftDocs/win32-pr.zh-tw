---
description: QueryStations 方法會提供目前使用網路監視器來捕捉資料的所有電腦清單。
ms.assetid: feebcb28-914b-450e-95d4-10a60cbf1438
title: 'IStats：： QueryStations 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b2d4ead22b3e7308aee3c44b3ff6dff407591cbe675b09a3300f3e7a8720726c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742638"
---
# <a name="istatsquerystations-method"></a>IStats：： QueryStations 方法

**QueryStations** 方法會提供目前使用網路監視器來捕捉資料的所有電腦清單。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpQueryTable* \[in、out\]
</dt> <dd>

指向 [[工作]](querytable.md) 結構的指標。 在輸入時，此結構必須包含您想要網路監視器傳回的電腦數目上限，以及 [STATIONQUERY](stationquery.md) 結構的陣列。

在輸出時，此結構會傳回每一部電腦的捕獲資料和 [STATIONQUERY](stationquery.md) 結構的電腦數目。 請注意，這項資訊可能包括使用早2.0 版的網路監視器版本的電腦。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值會是下列錯誤碼：



| 傳回碼                                                                                           | 描述                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ \_ 記憶體不足 \_**</dt> </dl> | 無法使用處理此查詢所需的記憶體。<br/> |



 

## <a name="remarks"></a>備註

呼叫 [CreateNPPInterface](createnppinterface.md) 之後，隨時都可以呼叫這個方法。 呼叫這個方法是同步呼叫，這可能需要幾秒鐘的時間才能完成，因為網路監視器等候遠端電腦回應查詢。 只有本機子網上的電腦可以進行查詢。

您必須負責為 [資料表結構配置](querytable.md) 記憶體，並在不再需要資料表之後釋放該記憶體。 這項需求包括用於查看 [STATIONQUERY](stationquery.md) 陣列所需的記憶體。

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

[透視](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




