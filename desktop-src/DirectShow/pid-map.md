---
description: PID \_ 對應結構包含可識別 mpeg-2 傳輸資料流程封包識別碼的內容。
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: 'PID_MAP 結構 (Bdatypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983189"
---
# <a name="pid_map-structure"></a>PID \_ 對應結構

`PID_MAP`結構包含可識別 mpeg-2 傳輸資料流程封包識別碼的內容。

## <a name="syntax"></a>語法


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a>成員

<dl> <dt>

**ulPID**
</dt> <dd>

指定 (PID 的封包識別碼) 

</dd> <dt>

**MediaSampleContent**
</dt> <dd>

以 [**媒體 \_ 範例 \_ 內容**](media-sample-content.md) 列舉型別指定封包內容的內容。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Bdatypes (包含 Bdaiface) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 結構](directshow-structures.md)
</dt> <dt>

[**IEnumPIDMap 介面**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




