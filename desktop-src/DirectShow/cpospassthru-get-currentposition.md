---
description: Get \_ CurrentPosition 方法會抓取目前的位置，相對於資料流程的總持續時間。 這個方法會實 IMediaPosition：： get \_ CurrentPosition 方法。
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: 'CPosPassThru.get_CurrentPosition 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db49717284f597249603b3c18340855793ebd342632aeb2091861f9742963a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084238"
---
# <a name="cpospassthruget_currentposition-method"></a>CPosPassThru. 取得 \_ CurrentPosition 方法

方法會抓取 `get_CurrentPosition` 目前的位置，相對於資料流程的總持續時間。 這個方法會實 [**IMediaPosition：： get \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pllTime* 
</dt> <dd>

接收目前位置之變數的指標（以秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

從連接的 pin 傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPosPassThru 類別**](cpospassthru.md)
</dt> </dl>

 

 




