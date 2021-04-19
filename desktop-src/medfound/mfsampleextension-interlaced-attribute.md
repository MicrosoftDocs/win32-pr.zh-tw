---
description: 指出影片框架是否為交錯式或漸進式。
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: 'MFSampleExtension_Interlaced 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974569"
---
# <a name="mfsampleextension_interlaced-attribute"></a>MFSampleExtension \_ 交錯屬性

指出影片框架是否為交錯式或漸進式。 若 **為 TRUE**，則框架為交錯式。 如果 **為 FALSE**，則表示框架為漸進式。 如果未設定，則媒體類型會描述交錯。 這個屬性會套用至媒體範例。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>備註

若為包含混合漸進和交錯框架的影片內容，請將媒體類型設定為交錯式，並在每個框架上使用此屬性，以指出框架是漸進式或交錯式。

若為完全交錯的影片內容，請將媒體類型設定為交錯式並省略這個屬性，或在每個範例上將它設定為 **TRUE** 。

若為完全漸進的影片內容，請將媒體類型設定為漸進式並省略這個屬性，或在每個範例上將它設定為 **FALSE** 。

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

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[範例屬性](sample-attributes.md)
</dt> <dt>

[媒體範例](media-samples.md)
</dt> <dt>

[影片交錯](video-interlacing.md)
</dt> </dl>

 

 




