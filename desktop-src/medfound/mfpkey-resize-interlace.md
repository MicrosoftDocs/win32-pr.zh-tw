---
description: 指定輸入資料流程是否為交錯式。
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: 'MFPKEY_RESIZE_INTERLACE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a27504bd6da92bc48fee04afc999568a514fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981525"
---
# <a name="mfpkey_resize_interlace-property"></a>MFPKEY 重 \_ 設大小 \_ 交錯屬性

指定輸入資料流程是否為交錯式。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="applies-to"></a>套用至

-   [影片尺寸調整 DSP](videoresizer.md)

## <a name="remarks"></a>備註

請使用下列其中一個值：



| 值     | 描述 |
|-----------|-------------|
| VT \_ FALSE | 漸進式 |
| VT \_ TRUE  | Interlaced  |



 

如果未設定此屬性，則 DSP 會使用輸入媒體類型來判斷影片是否為交錯式。 您可以設定這個屬性來覆寫媒體類型設定。

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

 

 
