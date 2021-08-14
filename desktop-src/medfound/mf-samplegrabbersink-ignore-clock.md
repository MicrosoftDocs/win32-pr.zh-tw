---
description: 指定範例-捕獲接收是否使用呈現時鐘來排程範例。
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: 'MF_SAMPLEGRABBERSINK_IGNORE_CLOCK 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d757b02a060b4e598ff42d3bd8b9ad7f38af41143c807647aa6f2b8528677cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474421"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a>MF \_ SAMPLEGRABBERSINK \_ 忽略 \_ 時鐘屬性

指定範例-捕獲接收是否使用呈現時鐘來排程範例。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

您可以在 [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) 函數所建立的啟用物件上設定此屬性。 在啟用物件上呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 方法之前，請先設定屬性。

根據預設，當範例抓取器接收到範例時，它會等候範例的呈現時間叫用應用程式的回呼。 如果 MF \_ SAMPLEGRABBERSINK \_ 忽略 \_ 時鐘屬性為非零值，則範例抓取器接收會忽略標記法，並在收到每個範例時立即叫用回呼。

建議使用方式：

-   如果您想要儘快處理範例，請將此屬性設定為 **TRUE**。
-   如果您想要讓回呼方法的呼叫與時鐘同步，請不要設定這個屬性，或將它設定為 **FALSE**。 您可以藉由設定 [ [**MF \_ SAMPLEGRABBERSINK \_ SAMPLE \_ TIME \_ OFFSET**](mf-samplegrabbersink-sample-time-offset-attribute.md) ] 屬性，以稍微早于時鐘的方式取得範例，仍保持同步處理。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> </dl>

 

 




