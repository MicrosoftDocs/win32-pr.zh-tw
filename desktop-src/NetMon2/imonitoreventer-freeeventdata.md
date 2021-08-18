---
description: FreeEventData 方法會釋出配置給 NMEVENTDATA 結構的空間。
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'IMonitorEventer：： FreeEventData 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: f2bf462ef63045c8c4e5822e3d28fc21b44dfeed5848da3ac89c8232dfacc062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037438"
---
# <a name="imonitoreventerfreeeventdata-method"></a>IMonitorEventer：： FreeEventData 方法

**FreeEventData** 方法會釋出配置給 [**NMEVENTDATA**](nmeventdata.md)結構的空間。

## <a name="syntax"></a>語法


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNMEventData* \[在\]
</dt> <dd>

[**NMEVENTDATA**](nmeventdata.md)結構的位址，也就是釋放的記憶體。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 S \_ OK。

## <a name="remarks"></a>備註

監視器會呼叫這個方法來釋放它們配置給事件資料結構的記憶體。 請注意，雖然監視器仍具有已配置之 [**NMEVENTDATA**](nmeventdata.md) 結構中字串的指標，但是在呼叫 **FreeEventData** 方法之前，必須先釋放這些字串的記憶體。

如需有關如何為 [**NMEVENTDATA**](nmeventdata.md) 結構配置記憶體的詳細資訊，請參閱 [**IMonitorEventer：： GetEventData**](imonitoreventer-geteventdata.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md)
</dt> <dt>

[**NMEVENTDATA**](nmeventdata.md)
</dt> </dl>

 

 




