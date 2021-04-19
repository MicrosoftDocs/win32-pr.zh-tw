---
description: 指出增強型影片轉譯器 (EVR) 媒體接收器需要進行去交錯的未壓縮緩衝區數目。
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: 'MF_SA_REQUIRED_SAMPLE_COUNT 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe7d47370cd4877a0f9722d443bc6bb3f7bdeb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976965"
---
# <a name="mf_sa_required_sample_count-attribute"></a>MF \_ SA \_ 必要 \_ 範例 \_ 計數屬性

指出增強型影片轉譯器 (EVR) 媒體接收器需要進行去交錯的未壓縮緩衝區數目。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這是資料流程層級的屬性。 若要從 EVR 取得屬性，請執行下列動作：

1.  呼叫 [**IMFMediaSink：： GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) 以取得資料流程接收。
2.  查詢 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的資料流程接收。
3.  呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

就內部而言，混音器會提供此屬性給 EVR。 若要從混音器取得屬性，請呼叫 [**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> </dl>

 

 




