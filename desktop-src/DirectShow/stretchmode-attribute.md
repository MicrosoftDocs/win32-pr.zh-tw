---
description: Stretchmode 屬性會指定如何延展不符合輸出維度的影像。
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: stretchmode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed398fbe193ef262bdfc9a28cf66bef3a5b11f759d90c460cc99342ec7cd66b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903868"
---
# <a name="stretchmode-attribute"></a>stretchmode 屬性

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`stretchmode`屬性會指定如何延展不符合輸出維度的影像。

## <a name="possible-values"></a>可能的值

必須具有下列其中一個值。

-   「延展」：影像會伸展以符合輸出框架大小，而不會保留長寬比。 (預設值)
-   「裁剪」：影像會裁剪以符合輸出框架大小。
-   "preserveaspectratio"：保留原始的外觀比例，且沿著較短的維度有黑色的黑邊。
-   "preserveaspectrationoletterbox"：影像會調整大小以填滿整個目標框架，同時保留外觀比例。

## <a name="applies-to"></a>套用至

[**clip**](clip-element.md)

## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 屬性](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



