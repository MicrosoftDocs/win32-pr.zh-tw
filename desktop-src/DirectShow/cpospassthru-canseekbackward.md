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
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990535"
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

 

 




