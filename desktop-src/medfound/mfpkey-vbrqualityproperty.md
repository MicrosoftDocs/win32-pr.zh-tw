---
description: 指定以品質為基礎的實際品質層級 (1-傳遞) 可變位速率 (VBR) 編碼。
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: 'MFPKEY_VBRQUALITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dff57fc27b952780737d63fa8f04faf722ed8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943906"
---
# <a name="mfpkey_vbrquality-property"></a>MFPKEY \_ VBRQUALITY 屬性

指定以品質為基礎的實際品質層級 (1-傳遞) 可變位速率 (VBR) 編碼。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCVBRQuality、g \_ wszWMCPAudioVBRQuality

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

並非範圍內的所有值都有唯一的意義。 代表上一層級之品質上階的值為：1、4、8、11、15、18、22、25、29、33、36、40、43、47、50、54、58、61、65、68、72、75、79、83、86、90、93和97。

若為音訊編碼器物件，則會在您使用 [**IMediaObject：： GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)取出的輸出類型 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構中提供品質模式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列舉特定編碼模式的音訊類型](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
