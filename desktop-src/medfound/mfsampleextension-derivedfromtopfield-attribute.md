---
description: 指定 deinterlaced 的影片框架是否衍生自上方欄位或下方欄位。
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: 'MFSampleExtension_DerivedFromTopField 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974610"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a>MFSampleExtension \_ DerivedFromTopField 屬性

指定 deinterlaced 的影片框架是否衍生自上方欄位或下方欄位。 這個屬性會套用至媒體範例。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>備註

這個屬性僅適用于 deinterlaced 範例。 如果框架是藉由插上其中一個欄位來 deinterlaced，則設定這個屬性。

如果值為 **TRUE**，則會從上方欄位中插入較低的欄位。 如果值為 **FALSE**，則會從較低的欄位內插上上方欄位。

如果未設定屬性，則不會 deinterlaced 框架。 框架是真實的漸進式框架，也就是交錯的框架。

這個屬性是參考資訊。 軟體 deinterlacer 可以設定此屬性。 如果設定此屬性，它會提供提示，讓您藉由卸載插入的掃描行來復原原始欄位。 例如，如果屬性為 **TRUE**，您可以藉由卸載插入的下半部欄位來復原原始的上方欄位。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[範例屬性](sample-attributes.md)
</dt> <dt>

[媒體範例](media-samples.md)
</dt> <dt>

[影片交錯](video-interlacing.md)
</dt> </dl>

 

 




