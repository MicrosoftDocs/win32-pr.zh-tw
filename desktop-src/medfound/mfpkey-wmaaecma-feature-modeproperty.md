---
description: 讓應用程式覆寫語音捕獲 DSP 之各種屬性的預設設定。
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: 'MFPKEY_WMAAECMA_FEATURE_MODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a47ef86a2acf83131800e9cb55b86de2cd3d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691656"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a>MFPKEY \_ WMAAECMA \_ 功能 \_ 模式屬性

讓應用程式覆寫語音捕獲 DSP 之各種屬性的預設設定。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="default-value"></a>預設值

VARIANT \_ FALSE

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

如果此屬性為 VARIANT \_ TRUE，則應用程式可以在 DSP 上設定下列屬性：

-   [MFPKEY \_ WMAAECMA \_ FEATR \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ 中心 \_ 剪輯](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ ECHO \_ LENGTH](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ 畫面格 \_ 大小](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ 模式](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ PREPROC](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ 雜訊 \_ 填滿](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ NS](mfpkey-wmaaecma-featr-nsproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)

如果此屬性為 VARIANT \_ FALSE，則 DSP 會忽略這些屬性，並使用其預設設定。 這個屬性的預設值為 VARIANT \_ FALSE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[語音捕獲 DSP](voicecapturedmo.md)
</dt> </dl>

 

 
