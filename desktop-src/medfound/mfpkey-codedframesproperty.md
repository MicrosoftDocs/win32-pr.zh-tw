---
description: 指定編解碼器編碼的影片框架數目。
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: 'MFPKEY_CODEDFRAMES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e836f2177311a2ffc13065187a1affce93c6dbe74ff9ff4c99ef78a6f492b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954728"
---
# <a name="mfpkey_codedframes-property"></a>MFPKEY \_ CODEDFRAMES 屬性

指定編解碼器編碼的影片框架數目。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCCodedFrames

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

這個值等於 [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) 減去由於位速率限制而捨棄的任何框架。 完成傳遞範例之後，您可以取得此值。

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

 

 




