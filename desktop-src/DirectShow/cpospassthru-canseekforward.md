---
description: CanSeekForward 方法會判斷是否可以向前 seeked 資料流程。 這個方法會實 IMediaPosition：： CanSeekForward 方法。
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: 'CPosPassThru. CanSeekForward 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f07491a94522280357c85d773d28ea4732f2f85879b55cf5d1b5a99ec72d23f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073562"
---
# <a name="cpospassthrucanseekforward-method"></a>CPosPassThru. CanSeekForward 方法

`CanSeekForward`方法會判斷資料流程是否可以向前 seeked。 這個方法會實 [**IMediaPosition：： CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCanSeekForward* 
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

 

 




