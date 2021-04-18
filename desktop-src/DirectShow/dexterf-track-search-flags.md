---
description: DEXTERF \_ TRACK \_ 搜尋 \_ 旗標列舉會指定在時間軸中搜尋物件的界限條件。
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: 'DEXTERF_TRACK_SEARCH_FLAGS 列舉 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976171"
---
# <a name="dexterf_track_search_flags-enumeration"></a>DEXTERF \_ 追蹤 \_ 搜尋 \_ 旗標列舉

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`DEXTERF_TRACK_SEARCH_FLAGS`列舉會指定在時間軸中搜尋物件的界限條件。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**DEXTERF \_ 周框**
</dt> <dd>

搜尋橫跨指定時間的物件。

</dd> <dt>

<span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF \_ 正好 \_ 在**
</dt> <dd>

搜尋正好在指定時間開始的物件。

</dd> <dt>

<span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF \_ 轉送**
</dt> <dd>

搜尋在指定時間或更新版本啟動的物件。

</dd> </dl>

## <a name="remarks"></a>備註

下表摘要說明這些界限條件。



| 列舉值    | 界限條件                        |
|----------------------|-------------------------------------------|
| DEXTERF \_ 周框    | 開始 <= TimeStop > 時間<br/> |
| DEXTERF \_ 正好 \_ 在 | 開始 = = 時間                             |
| DEXTERF \_ 轉送    | 開始 >= 時間                          |



 

-   Start：抓取物件的開始時間。
-   停止：抓取物件的停止時間。
-   時間：指定的搜尋時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Qedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




