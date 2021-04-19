---
description: 指定語音捕獲 DSP 的麥克風陣列幾何。
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: 'MFPKEY_WMAAECMA_MICARRAY_DESCPTR 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981461"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a>MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR 屬性

指定語音捕獲 DSP 的麥克風陣列幾何。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ BLOB

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

這個屬性的值是 [**KSAUDIO \_ MIC \_ 陣列 \_ 幾何**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) 結構。 此結構是在標頭檔 KsMedia 中定義。 若要取得麥克風陣列幾何，請 \_ \_ \_ \_ 在裝置上呼叫 **IKsControl：： KSPROPERTY** 方法，以查詢音訊裝置以取得 KSPROPERTY 音訊 MIC 陣列幾何屬性。 如需麥克風陣列的詳細資訊，請下載技術白皮書， [以瞭解如何建立和使用適用于 Windows Vista 的麥克風陣列](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format)。

如果您在篩選模式中使用 DSP，且已啟用麥克風陣列處理，請設定此屬性。 如果您在來源模式中使用 DSP，DSP 會自動查詢裝置的幾何資訊。

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

 

 
