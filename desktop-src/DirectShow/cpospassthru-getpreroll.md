---
description: GetPreroll 方法會抓取在開始位置之前將排入佇列的資料量。 這個方法會實 IMediaSeeking：： GetPreroll 方法。
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: 'CPosPassThru. GetPreroll 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997714"
---
# <a name="cpospassthrugetpreroll-method"></a>CPosPassThru. GetPreroll 方法

`GetPreroll`方法會抓取在開始位置之前將排入佇列的資料量。 這個方法會實 [**IMediaSeeking：： GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pllPreroll* 
</dt> <dd>

變數的指標，此變數會接收預先計算的時間，以目前時間格式的單位為單位。

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

 

 




