---
description: CEnumMediaTypes。 CEnumMediaTypes 函式-函數方法。
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
ms.openlocfilehash: 2d243ed25cc48c5d30d467f97e2ec20e1f0f2b58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095676"
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

 

 




