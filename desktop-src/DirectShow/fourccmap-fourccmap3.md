---
description: 提供舊樣式多媒體格式 DWORD 型別和 GUID 子類型之間對應的方法。 這個方法會使用 ' pguid ' 參數。
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: FOURCCMap：： FOURCCMap (Fourcc .h) -pguid 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c674791418a7668d7c7597e951e9a89613b9c8150865ff123263e9d0ef9ded2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330438"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a>FOURCCMap：： FOURCCMap (Fourcc .h) -pguid 參數

函式方法。 建構會提供舊樣式的多媒體格式 **DWORD** 類型與 **GUID** 子類型之間的對應。

## <a name="syntax"></a>語法


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pguid* 
</dt> <dd>

全域唯一識別碼 (**GUID**) 的指標。

</dd> </dl>

## <a name="remarks"></a>備註

如果使用 **FOURCC** 程式碼來建立此物件，則會建立 **GUID** 以與其相符。 如果此物件是使用現有的 **GUID** 建立的，則物件的 **FOURCC** 值會設定為零。 之後，您可以分別使用 [**SetFOURCC**](fourccmap-setfourcc.md)和 [**GetFOURCC**](fourccmap-getfourcc.md)成員函式來設定或取出 **FOURCC** 值。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭  | Fourcc (包含： .h)  |
| 程式庫 |  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FOURCCMap 類別**](fourccmap.md)
</dt> </dl>

 

 




