---
description: 調整對比。
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: 'MFPKEY_COLOR_CONTRAST 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c1c794b10580cbb323d19f52eed7d3bfb5fc6cf96e316d708491025776cfff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954468"
---
# <a name="mfpkey_color_contrast-property"></a>MFPKEY \_ 色彩 \_ 對比屬性

調整對比。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="applies-to"></a>套用至

-   [色彩控制轉換 DSP](colorcontroltransform.md)

## <a name="remarks"></a>備註

對比調整是藉由將 YCbCr 值乘以縮放因數來執行。

這個屬性的範圍為-127 到127。 零表示對比沒有變更。

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

 

 
