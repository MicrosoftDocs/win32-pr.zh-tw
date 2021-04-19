---
description: 函式方法。
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: CMediaType. CMediaType (Mtype. h) -cmtype 和 phr 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a40929bb6f53df7ce721e20eefba3019eb71cb0e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106990513"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a>CMediaType. CMediaType (Mtype. h) 

函式方法。

## <a name="syntax"></a>語法


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cmtype* \[裁判\]
</dt> <dd>

物件的參考 `CMediaType` 。 此函式會將媒體類型複製到新的物件，包括格式區塊（如果有的話）。

</dd> <dt>

*phr* 
</dt> <dd>

接收 HRESULT 值之變數的指標。 這個參數可以是 **Null** 指標。 否則，呼叫端必須在呼叫此函式之前，將值設定為 S \_ OK。 如果此函式失敗，則會將值設定為失敗碼。

</dd> </dl>

## <a name="remarks"></a>備註

此函式會呼叫 [**CMediaType：： InitMediaType**](cmediatype-initmediatype.md) 方法來初始化媒體類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




