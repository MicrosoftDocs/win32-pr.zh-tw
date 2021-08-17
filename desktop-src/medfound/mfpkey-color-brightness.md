---
description: 調整亮度。
ms.assetid: 1b3f56eb-3f22-4120-ba6c-331eccd5d303
title: 'MFPKEY_COLOR_BRIGHTNESS 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a43969dff8d743e493916303c31e3d57760a2b025bfadaeaf8cc03e7e25430d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954648"
---
# <a name="mfpkey_color_brightness-property"></a>MFPKEY \_ 色彩 \_ 亮度屬性

調整亮度。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="applies-to"></a>套用至

-   [色彩控制轉換 DSP](colorcontroltransform.md)

## <a name="remarks"></a>備註

亮度調整是藉由將值新增至 luma 通道來執行。

這個屬性的範圍為-127 到127。 零表示亮度沒有變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
