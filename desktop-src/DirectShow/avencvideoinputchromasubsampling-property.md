---
description: 指定輸入影片的色度地點。 色度地點會定義每個色度樣本的位置，相對於 luma 範例。
ms.assetid: e9f8fef5-73da-424d-a239-09779b81a02b
title: 'AVEncVideoInputChromaSubsampling 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 958237a50c42ef7e5387c89cb7476a12ae72968f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935919"
---
# <a name="avencvideoinputchromasubsampling-property"></a>AVEncVideoInputChromaSubsampling 屬性

指定輸入影片的色度地點。 色度地點會定義每個色度樣本的位置，相對於 luma 範例。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoInputChromaSubsampling**

## <a name="property-value"></a>屬性值

這個屬性的值是 [**eAVEncVideoChromaSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling) 列舉中的位 or 旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




