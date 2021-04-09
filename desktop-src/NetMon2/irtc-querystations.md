---
description: 提供目前使用網路監視器來捕捉網路資料的所有電腦清單。
ms.assetid: 57e7b8e1-99b8-4194-b6dc-401235be4ef4
title: 'IRTC：： QueryStations 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a0cebd789284dd41c293424a70686f30eb4601d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943881"
---
# <a name="irtcquerystations-method"></a>IRTC：： QueryStations 方法

**QueryStations** 方法會提供目前使用網路監視器來捕捉網路資料的所有電腦清單。

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

指向 [工作] [**結構的**](querytable.md) 指標。 在輸入時，此結構必須包含您想要網路監視器傳回的電腦數目上限，以及 [**STATIONQUERY**](stationquery.md) 結構的陣列。

在輸出時，此結構會傳回每一部電腦的捕獲資料和 [**STATIONQUERY**](stationquery.md) 結構的電腦數目。 請注意，這可能包括使用早2.0 版的網路監視器版本的電腦。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 **NMERR \_ SUCCESS**。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                           | Description                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ \_ 記憶體不足 \_**</dt> </dl> | 無法使用處理此查詢所需的記憶體。<br/> |



 

## <a name="remarks"></a>備註

呼叫 [**CreateNPPInterface**](createnppinterface.md) 方法之後，隨時都可以呼叫這個方法。 呼叫這個方法是同步呼叫，這可能需要幾秒鐘的時間才能完成，網路監視器等候遠端電腦回應查詢。 只有本機子網上的電腦可以進行查詢。

使用者必須配置 [**資料表結構的**](querytable.md) 記憶體，並在不再需要資料表之後釋放該記憶體。 這項需求包括用於查看 [**STATIONQUERY**](stationquery.md)陣列所 **需的記憶體。**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRTC**](irtc.md)
</dt> <dt>

[**透視**](querytable.md)
</dt> <dt>

[**STATIONQUERY**](stationquery.md)
</dt> </dl>

 

 




