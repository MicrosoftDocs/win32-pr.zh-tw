---
description: CanSeekBackward 方法會判斷資料流程是否可反向 seeked。 這個方法會實 IMediaPosition：： CanSeekBackward 方法。
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: 'CPosPassThru. CanSeekBackward 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1d989acf074eb20e6ea3387c37129700320ce782e3c5d7c8bd4320641839ca1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108428"
---
# <a name="cpospassthrucanseekbackward-method"></a>CPosPassThru. CanSeekBackward 方法

`CanSeekBackward`方法會判斷資料流程是否可以向後 seeked。 這個方法會實 [**IMediaPosition：： CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCanSeekBackward* 
</dt> <dd>

如果篩選準則可以向前搜尋，則為收到值 OATRUE 之變數的指標，否則為 OAFALSE。

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

 

 




