---
description: 移動方法會放置並調整對話方塊的大小。 這個方法會實 IPropertyPage：： Move 方法。
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: 'CBasePropertyPage： Move 方法 (Cprop. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987178"
---
# <a name="cbasepropertypagemove-method"></a>CBasePropertyPage. Move 方法

`Move`方法會放置並調整對話方塊的大小。 這個方法會實 **IPropertyPage：： Move** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*prect* 
</dt> <dd>

**矩形** 結構的指標，其中包含位置資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                  | Description                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>                   |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | **Null** 指標引數。<br/> |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 發生非預期的失敗。<br/>        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePropertyPage 類別**](cbasepropertypage.md)
</dt> </dl>

 

 




