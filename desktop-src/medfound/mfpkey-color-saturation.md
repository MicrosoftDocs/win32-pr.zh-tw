---
description: 調整飽和度。
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: 'MFPKEY_COLOR_SATURATION 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496b1f017ceff6ab4bd01ce01ccfd5da0759befc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513117"
---
# <a name="mfpkey_color_saturation-property"></a>MFPKEY \_ 色彩 \_ 飽和度屬性

調整飽和度。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="applies-to"></a>套用至

-   [色彩控制轉換 DSP](colorcontroltransform.md)

## <a name="remarks"></a>備註

飽和度調整是藉由將 Cb 和 Cr 值乘以常數來執行。

這個屬性的範圍為-127 到127。 零表示飽和度沒有變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
