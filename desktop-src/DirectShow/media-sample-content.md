---
description: 描述 MPEG-2 傳輸串流內的基本資料流程內容。 此列舉會在 IMPEG2PIDMap 介面中使用，此介面會在 MPEG-2 信號的輸出針腳上執行。
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: 'MEDIA_SAMPLE_CONTENT 列舉 (Bdatypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SAMPLE_CONTENT
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 9065f2af948ff28d181b24842673b086882837bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998741"
---
# <a name="media_sample_content-enumeration"></a>媒體 \_ 範例 \_ 內容列舉

描述 MPEG-2 傳輸串流內的基本資料流程內容。 此列舉會在 [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) 介面中使用，此介面會在 [mpeg-2 信號](mpeg-2-demultiplexer.md)的輸出針腳上執行。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**媒體 \_ 傳輸封 \_ 包**
</dt> <dd>

指定要在不處理的情況下傳遞的完整傳輸資料流程封包。

</dd> <dt>

<span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**媒體 \_ 基本 \_ 資料流程**
</dt> <dd>

指定音訊或影片 PE 裝載。

</dd> <dt>

<span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**媒體 \_ MPEG2 \_ PSI**
</dt> <dd>

指定 PAT、PMT、CAT 或私用資料流程。 這些是完全不需要重組的 PSI 區段。

</dd> <dt>

<span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**媒體 \_ 傳輸 \_ 承載**
</dt> <dd>

指定收集的 TS 封包承載，例如 PE 封包。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Bdatypes (包含 Bdaiface) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 列舉類型](directshow-enumerated-types.md)
</dt> </dl>

 

 




