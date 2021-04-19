---
description: SetObjects 方法會為與屬性頁相關聯的物件提供 IUnknown 指標。 這個方法會實 IPropertyPage：： SetObjects 方法。
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: 'CBasePropertyPage. SetObjects 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993439"
---
# <a name="cbasepropertypagesetobjects-method"></a>CBasePropertyPage. SetObjects 方法

`SetObjects`方法會為與屬性頁相關聯的物件提供 **IUnknown** 指標。 這個方法會實 **IPropertyPage：： SetObjects** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cObjects* 
</dt> <dd>

指定 *ppUnk* 所指定陣列中的 **IUnknown** 指標數目。

</dd> <dt>

*ppUnk* 
</dt> <dd>

指定 **IUnknown** 指標的陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                  | Description                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>                   |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | **Null** 指標引數。<br/> |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 發生非預期的失敗。<br/>        |



 

## <a name="remarks"></a>備註

雖然 *ppUnk* 會指定 **IUnknown** 指標的陣列，但 **CBasePropertyPage** 類別的設計只是為了支援一個相關聯的物件。 如果 *cObjects* 大於1，方法會傳回 E 非 \_ 預期的。

如果 *cObjects* 等於1，這個方法會呼叫 [**CBasePropertyPage：： OnConnect**](cbasepropertypage-onconnect.md) 方法。 如果 *cObjects* 等於0，這個方法會呼叫 [**CBasePropertyPage：： OnDisconnect**](cbasepropertypage-ondisconnect.md) 方法。 衍生類別應該覆寫這兩種方法;如需詳細資訊，請參閱這些方法的備註。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePropertyPage 類別**](cbasepropertypage.md)
</dt> </dl>

 

 




