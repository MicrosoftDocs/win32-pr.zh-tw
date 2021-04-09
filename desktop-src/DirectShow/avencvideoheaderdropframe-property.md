---
description: 在圖片群組 (GOP) 標頭中指定放置框架旗標的值。
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: 'AVEncVideoHeaderDropFrame 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846739"
---
# <a name="avencvideoheaderdropframe-property"></a>AVEncVideoHeaderDropFrame 屬性

在圖片群組 (GOP) 標頭中指定放置框架旗標的值。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoHeaderDropFrame**

## <a name="property-value"></a>屬性值

這個屬性的值可以是0或1。

## <a name="remarks"></a>備註

NTSC 影片中會使用放置畫面格模式來修正影片之間的差異，也就是每秒29.97 個畫面格，以及時間代碼顯示，也就是每秒30個畫面格。 在拖放框架模式中，會在每分鐘的開頭略過畫面格數位00和01，但大約是 10 (00、10、20等等) 的倍數。 只有時間碼中的框架號碼會被捨棄;不會卸載任何實際的畫面格。

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

 

 




