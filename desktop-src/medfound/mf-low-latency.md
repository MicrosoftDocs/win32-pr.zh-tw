---
description: 在 Microsoft 媒體基礎管線中啟用低延遲處理。
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: 'MF_LOW_LATENCY 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693884"
---
# <a name="mf_low_latency-attribute"></a>MF \_ 低 \_ 延遲屬性

在 Microsoft 媒體基礎管線中啟用低延遲處理。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

低延遲是定義為產生媒體資料時的最小可能延遲， (或在轉譯時接收) 。 即時通訊案例需要低延遲。 針對其他案例，例如本機播放或轉碼，您通常不應該啟用低延遲模式，因為它可能會影響品質。

> [!Note]  
> 這個屬性的 GUID 值與針對 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)介面定義的 [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)屬性相同。

 

在管線元件上設定此屬性，如下所示：

-   媒體來源：使用 [**IMFMediaSourceEx：： GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) 方法。
-   媒體基礎轉換 (MFT) ：使用 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。 針對編碼器，編碼器可能會透過 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面支援低延遲。
-   媒體接收器：查詢 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的媒體接收器。

應用程式通常不會直接在管線元件上設定此屬性，而是在下列其中一個物件上設定屬性：

-   [媒體會話](media-session.md)：使用 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)或 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguation* 參數，否則請在拓撲上設定屬性。
-   [來源讀取器](source-reader.md)：當您建立來源讀取器時，使用設定屬性設定屬性。 如需詳細資訊，請參閱 [來源讀取器屬性](source-reader-attributes.md)。
-   [接收寫入器](sink-writer.md)：當您建立接收寫入器時，使用設定屬性設定屬性。 如需詳細資訊，請參閱 [接收寫入器屬性](sink-writer-attributes.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[接收寫入器屬性](sink-writer-attributes.md)
</dt> <dt>

[來源讀取器屬性](source-reader-attributes.md)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 
