---
description: 指定是否要重複交錯框架中的第一個欄位。 這個屬性會套用至媒體範例。
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: 'MFSampleExtension_RepeatFirstField 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114404"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a>MFSampleExtension \_ RepeatFirstField 屬性

指定是否要重複交錯框架中的第一個欄位。 這個屬性會套用至媒體範例。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>備註

如果值為 **FALSE** 或未設定屬性，則不會重複第一個欄位。 如果值為 **TRUE**，則會重複第一個欄位。 只有當下列條件成立時，值 **true** 才有效：

-   媒體類型為混合交錯和漸進式。  (媒體類型上的 [**MF \_ MT \_ 交錯 \_ 模式**](mf-mt-interlace-mode-attribute.md) 屬性屬性為 **MFVideoInterlace \_ MixedInterlaceOrProgressive**。 ) 
-   框架是漸進式的，而範例上的 [**MFSampleExtension \_ 交錯**](mfsampleextension-interlaced-attribute.md) 屬性是 **TRUE**。
-   範例上會設定 [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) 屬性。 值可以是 **TRUE** 或 **FALSE**。 欄位的排序是由這個屬性所決定。

這個屬性是用於3:2 的下拉。 下表顯示欄位顯示的順序。



| MFSampleExtension \_ RepeatFirstField | MFSampleExtension \_ BottomFieldFirst | 欄位順序         |
|-------------------------------------|-------------------------------------|---------------------|
| **TRUE**                            | **TRUE**                            | Lower、upper、lower |
| **TRUE**                            | **FALSE**                           | Upper、lower、upper |
| **FALSE**                           | **TRUE**                            | Lower、upper        |
| **FALSE**                           | **FALSE**                           | Upper、lower        |



 

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

 

 




