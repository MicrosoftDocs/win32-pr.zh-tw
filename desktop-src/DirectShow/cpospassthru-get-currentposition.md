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
ms.openlocfilehash: 6c146eb1ee3d0a48da90973ab181a4bd02182331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994052"
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

 

 




