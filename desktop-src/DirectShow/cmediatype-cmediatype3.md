---
description: 深入瞭解 CMediaType. CMediaType (Mtype 的) 方法。 這個方法會使用 ' mtype ' 和 ' phr ' 參數。
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: CMediaType. CMediaType (Mtype. h) -Mtype 和 phr 參數
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
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106997432"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a>CMediaType. CMediaType (Mtype. h) -Mtype 和 phr 參數

函式方法。

## <a name="syntax"></a>語法


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mtype* \[裁判\]
</dt> <dd>

[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的參考。 此函式會將媒體類型複製到新的物件，包括格式區塊（如果有的話）。

</dd> <dt>

*phr* 
</dt> <dd>

接收 HRESULT 值之變數的指標。 這個參數可以是 **Null** 指標。 否則，呼叫端必須在呼叫此函式之前，將值設定為 S \_ OK。 如果此函式失敗，則會將值設定為失敗碼。

</dd> </dl>

## <a name="remarks"></a>備註

此函式會呼叫 [**CMediaType：： InitMediaType**](cmediatype-initmediatype.md) 方法來初始化媒體類型。

## <a name="requirements"></a>規格需求

| 需求                   | 值                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭  | Mtype (包含： .h)                                                                                      |
| 程式庫 |  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




