---
description: MFPKEY_COLORCONV_MODE 屬性-指定輸入資料流程是否為交錯式。
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: 'MFPKEY_COLORCONV_MODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f86ed10873c1587aefba342392afa7f84f8c635788339d64deca18b76629255
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242887"
---
# <a name="mfpkey_colorconv_mode-property"></a>MFPKEY \_ COLORCONV \_ MODE 屬性

指定輸入資料流程是否為交錯式。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

由來自來源影片的 DSP 所計算。

## <a name="applies-to"></a>套用至

-   [色彩轉換器 DSP](colorconverter.md)

## <a name="remarks"></a>備註

使用下列其中一個值。



| 值 | 描述 |
|-------|-------------|
| 0     | 漸進式 |
| 2     | Interlaced  |



 

如果未設定此屬性，則 DSP 會使用輸入媒體類型來判斷影片是否為交錯式。 您可以設定這個屬性來覆寫媒體類型設定。

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

 

 
