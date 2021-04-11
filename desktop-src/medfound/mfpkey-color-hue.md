---
description: 調整色調。
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: 'MFPKEY_COLOR_HUE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ddf0109090bfb56102560dc06a853c970e7ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115136"
---
# <a name="mfpkey_color_hue-property"></a>MFPKEY \_ 色彩 \_ 色調屬性

調整色調。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="applies-to"></a>套用至

-   [色彩控制轉換 DSP](colorcontroltransform.md)

## <a name="remarks"></a>備註

色調調整是藉由混用 Cb 和 Cr 值來執行。  (如果 Cb 和 Cr 繪製在二維空間中，則色調調整是藉由在原點周圍旋轉來執行。 ) 

這個屬性的範圍為-127 到127。 零表示色調沒有變更。

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

 

 
