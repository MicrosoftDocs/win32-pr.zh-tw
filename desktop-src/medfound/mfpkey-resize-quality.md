---
description: 指定是否使用產生更高品質影片或更快速演算法的演算法。
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: 'MFPKEY_RESIZE_QUALITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8aeb59935c8fc3462b713967ed2b14a0adfcf731fa1a71fec434b0e07d4309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973407"
---
# <a name="mfpkey_resize_quality-property"></a>MFPKEY \_ 調整 \_ 品質屬性

指定是否使用產生更高品質影片或更快速演算法的演算法。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="applies-to"></a>套用至

-   [影片尺寸調整 DSP](videoresizer.md)

## <a name="remarks"></a>備註

請使用下列其中一個值：



| 值     | 描述          |
|-----------|----------------------|
| VT \_ FALSE | 更快速的演算法     |
| VT \_ TRUE  | 品質較高的影片 |



 

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

 

 
