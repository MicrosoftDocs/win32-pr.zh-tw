---
description: 函式方法。
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: 'CEnumMediaTypes. CEnumMediaTypes (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e17357d90c57f1a7d489d07fa56206343f50788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995359"
---
# <a name="cenummediatypescenummediatypes-constructor"></a>CEnumMediaTypes. CEnumMediaTypes 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPin* 
</dt> <dd>

要在其上執行列舉的釘選指標。

</dd> <dt>

*pEnumMediaTypes* 
</dt> <dd>

要複製之列舉值的 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面指標，或 **Null**。

</dd> </dl>

## <a name="remarks"></a>備註

如果 *pEnumMediaTypes* 是 **Null**，這個方法會將列舉值初始化為列舉序列的開頭。 否則，它會複製 *pEnumMediaTypes* 所指定之列舉值的內部狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CEnumMediaTypes 類別**](cenummediatypes.md)
</dt> </dl>

 

 




