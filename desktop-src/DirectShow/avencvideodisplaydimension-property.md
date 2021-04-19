---
description: 指定解碼時影片資料流程的大小。
ms.assetid: db7b101a-5ff8-4a62-b9e2-d05fcdc44b3d
title: 'AVEncVideoDisplayDimension 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e5f611525e68f6f47c442c6e733c6c3e7de14d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106967003"
---
# <a name="avencvideodisplaydimension-property"></a>AVEncVideoDisplayDimension 屬性

指定解碼時影片資料流程的大小。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoDisplayDimension**

## <a name="property-value"></a>屬性值

值的上層16位包含寬度（以圖元為單位）。 較低的16個位包含高度（以圖元為單位）。

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

 

 




