---
description: CountPrefixBits 方法會計算指定位欄位開頭的零位位數。
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: 'CImageDisplay. CountPrefixBits 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 510ac01baab55fbf45e3441296018426335a8f50061f06400872fd7275d3e273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108478"
---
# <a name="cimagedisplaycountprefixbits-method"></a>CImageDisplay. CountPrefixBits 方法

`CountPrefixBits`方法會計算在指定位欄位開頭的零位位數。

## <a name="syntax"></a>語法


```C++
DWORD CountPrefixBits(
   const DWORD Field
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*欄位* 
</dt> <dd>

將位欄位指定為 **DWORD** 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回前1位之前發生的零位位數，如果所有位都是零，則傳回0x80000000。

## <a name="remarks"></a>備註

這個方法適用于使用 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構中的色遮罩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageDisplay 類別**](cimagedisplay.md)
</dt> </dl>

 

 




