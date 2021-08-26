---
description: GetEventData 方法會為 NMEVENTDATA 和 NMCOLUMNINFO 結構配置空間。
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'IMonitorEventer：： GetEventData 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3a089e57ac5f66187f97dfa6ae7533aeda620632bdbf35c7b5bf3a34d4654b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037368"
---
# <a name="imonitoreventergeteventdata-method"></a>IMonitorEventer：： GetEventData 方法

**GetEventData** 方法會為 [NMEVENTDATA](nmeventdata.md)和 [NMCOLUMNINFO](nmcolumninfo.md)結構配置空間。

## <a name="syntax"></a>語法


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bNumColumns* \[在\]
</dt> <dd>

所需的 **NMCOLUMNINFO** 結構數目。

</dd> <dt>

*ppNMEventData* \[擴展\]
</dt> <dd>

傳回之 **NMEVENTDATA** 結構的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 S \_ OK。

如果此方法不成功，傳回值就會 \_ 從記憶體中 NMERR 出來 \_ \_ 。

## <a name="remarks"></a>備註

監視器會呼叫這個方法，以配置事件資料和資料行資訊結構的記憶體。 若要釋放配置給 **NMEVENTDATA** 結構的記憶體，請參閱 [IMonitorEventer：： FreeEventData](imonitoreventer-freeeventdata.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IMonitorEventer](imonitoreventer.md)
</dt> <dt>

[IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md)
</dt> <dt>

[NMEVENTDATA](nmeventdata.md)
</dt> <dt>

[NMCOLUMNINFO](nmcolumninfo.md)
</dt> </dl>

 

 




