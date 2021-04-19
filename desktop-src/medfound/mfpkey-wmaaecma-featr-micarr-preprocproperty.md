---
description: 指定語音捕獲 DSP 是否執行麥克風陣列前置處理。
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: 'MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f992d8d26ba547eb1b5d1eac470536a963209f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983530"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ PREPROC 屬性

指定語音捕獲 DSP 是否執行麥克風陣列前置處理。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="default-value"></a>預設值

VARIANT \_ TRUE

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

前置處理可以移除干擾處理的靜止聲音，例如具有固定音調的色調。

這個屬性可以具有下列值。



| 值          | 描述            |
|----------------|------------------------|
| VARIANT \_ FALSE | 停用前置處理。 |
| VARIANT \_ TRUE  | 啟用前置處理。  |



 

這個屬性的預設值為 VARIANT \_ TRUE (enabled) 。 設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。

只有在啟用麥克風陣列處理時，DSP 才會使用此屬性。

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

 

 
