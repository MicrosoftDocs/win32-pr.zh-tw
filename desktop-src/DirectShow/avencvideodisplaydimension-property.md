---
description: 指定解碼時影片資料流程的大小。
ms.assetid: db7b101a-5ff8-4a62-b9e2-d05fcdc44b3d
title: 'AVEncVideoDisplayDimension 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe4c6f6fbcd3f4746b4ee3b807ebb098c1bfce728c9c01614943f05351f5bb18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540718"
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
| 最低支援的用戶端<br/> | Windows 2000 Professional \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop apps \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




