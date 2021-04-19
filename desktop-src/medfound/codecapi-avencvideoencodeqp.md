---
description: 指定適用于影片編碼 (QP) 的量化參數。
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: 'CODECAPI_AVEncVideoEncodeQP 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972993"
---
# <a name="codecapi_avencvideoencodeqp-property"></a>CODECAPI \_ AVEncVideoEncodeQP 屬性

指定適用于影片編碼 (QP) 的量化參數。

## <a name="data-type"></a>資料類型

**ULONGLONG** (VT \_ UI8) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoEncodeQP**

## <a name="property-value"></a>屬性值

一組 4 16 位欄位，用來以固定的 QP 編碼指定框架 QPs。

這些欄位包括：

-   Bits 0-15：預設的 QP
-   Bits 16-31：用於 I 框架的 QP
-   Bits 32-47：用於 P 框架的 QP
-   Bits 48-63：用於 B 框架的 QP

## <a name="remarks"></a>備註

這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。

若要確保不同編碼器之間的一致使用方式，您應該假設編碼器只會查看預設的 QP，並且可以忽略 I/P/B 圖片的 QP 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

