---
description: 時間軸 \_ 主要 \_ 類型列舉會指定物件的主要類型。
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: 'TIMELINE_MAJOR_TYPE 列舉 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 25c3e829aa73d1da78c110ffd148fb0ebaaebdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992556"
---
# <a name="timeline_major_type-enumeration"></a>時間軸 \_ 主要 \_ 類型列舉

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`TIMELINE_MAJOR_TYPE`列舉會指定物件的主要類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**時間軸 \_ 主要 \_ 類型 \_ 複合**
</dt> <dd>

綜合物件。 保存一或多個曲目。

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**時間軸 \_ 主要 \_ 類型 \_ 追蹤**
</dt> <dd>

追蹤物件。 保存一或多個來源。

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**時間軸 \_ 主要 \_ 類型 \_ 來源**
</dt> <dd>

來源物件。 包含媒體來源的參考。

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**時間軸 \_ 主要 \_ 類型 \_ 轉換**
</dt> <dd>

轉換物件。 定義複合、追蹤或來源之間的轉換。

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**時間軸 \_ 主要 \_ 類型 \_ 效果**
</dt> <dd>

效果物件。 定義要套用至複合、追蹤或來源物件的單一輸入效果。

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**時間軸 \_ 主要 \_ 類型 \_ 群組**
</dt> <dd>

群組物件。 包含一或多個指定類型的軌跡。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Qedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimeline**](iamtimeline.md)
</dt> <dt>

[**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[**IAMTimelineObj::GetTimelineType**](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




