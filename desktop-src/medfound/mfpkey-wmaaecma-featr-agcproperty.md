---
description: 指定語音捕獲 DSP 是否執行自動增益控制。
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: 'MFPKEY_WMAAECMA_FEATR_AGC 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991839"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ AGC 屬性

指定語音捕獲 DSP 是否執行自動增益控制。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="default-value"></a>預設值

VARIANT \_ FALSE

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

自動增益控制是數位信號處理 (DSP) 元件，可調整增益，讓信號的輸出層級維持在相同的大約範圍內。

這個屬性可以具有下列值。



| 值          | 描述                     |
|----------------|---------------------------------|
| VARIANT \_ FALSE | 停用自動增益控制。 |
| VARIANT \_ TRUE  | 啟用自動增益控制。  |



 

這個屬性的預設值為 VARIANT \_ FALSE (disabled) 。 設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。

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

 

 
