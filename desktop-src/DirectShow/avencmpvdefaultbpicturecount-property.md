---
description: 指定 I 與 P 框架之間的連續 B 框架預設數目。
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: 'AVEncMPVDefaultBPictureCount 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025757"
---
# <a name="avencmpvdefaultbpicturecount-property"></a>AVEncMPVDefaultBPictureCount 屬性

指定 I 與 P 框架之間的連續 B 框架預設數目。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncMPVDefaultBPictureCount**

## <a name="property-value"></a>屬性值

這個屬性具有線性範圍的值。 若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。

## <a name="remarks"></a>備註

在 Windows 8 之前，此屬性會套用至 MPEG 視頻編碼器。 從 Windows 8 開始，MPEG、WMV 和 h.264 影片編碼器會使用這個屬性。

如果編碼器支援這個屬性，它可以用來控制 (GOP) 結構的圖片群組。

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

 

 




