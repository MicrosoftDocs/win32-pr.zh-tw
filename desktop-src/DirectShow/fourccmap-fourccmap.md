---
description: 提供舊樣式多媒體格式 DWORD 型別和 GUID 子類型之間對應的方法。 這個方法不會使用任何參數。
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: FOURCCMap：： FOURCCMap (Fourcc .h) -沒有參數
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
ms.openlocfilehash: cd37ac842ab46c0d46fb3db1567d42274a026c47
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106986556"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a>FOURCCMap：： FOURCCMap (Fourcc .h) -沒有參數

函式方法。 建構會提供舊樣式的多媒體格式 **DWORD** 類型與 **GUID** 子類型之間的對應。

## <a name="syntax"></a>語法


```C++
FOURCCMap();
```



## <a name="parameters"></a>參數

這個函式沒有參數。

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

 

 




