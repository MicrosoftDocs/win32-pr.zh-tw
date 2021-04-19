---
description: 函式方法。
ms.assetid: fe7b2d62-0e6a-4253-b469-6cede5dc9bb1
title: 'CTransInPlaceOutputPin. CTransInPlaceOutputPin (Transip. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2c9ca668d3780ece082f9cab55db8406af7ad3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989533"
---
# <a name="ctransinplaceoutputpinctransinplaceoutputpin-constructor"></a>CTransInPlaceOutputPin. CTransInPlaceOutputPin 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CTransInPlaceOutputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pObjectName* 
</dt> <dd>

包含物件之偵錯工具名稱的字串。 如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。

</dd> <dt>

*pFilter* 
</dt> <dd>

建立此 pin 之篩選準則的指標，其必須是 [**CTransInPlaceFilter**](ctransinplacefilter.md) 物件。

</dd> <dt>

*phr* 
</dt> <dd>

變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。 在建立物件之前，將值初始化為「 \_ 確定」。 只有在發生錯誤時，才會變更此值。

</dd> <dt>

*pName* 
</dt> <dd>

包含 pin 名稱的寬字元字串。

</dd> </dl>

## <a name="remarks"></a>備註

*PName* 參數會指定 [**IPin：： QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)方法所傳回的 pin 名稱。 不過，此字串不會用於 pin 識別碼。 此類別的 pin 識別碼一律為 "Out"。 如需詳細資訊，請參閱 [**QueryId**](ctransforminputpin-queryid.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceOutputPin 類別**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




