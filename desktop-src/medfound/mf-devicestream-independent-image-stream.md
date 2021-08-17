---
description: 指定影片捕獲來源上的影像資料流程是否與影片資料流程無關。
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: 'MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f52392839c5f196159692bc9c4624cbda67b869471d6737c4cff60c847f890e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956678"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a>MF \_ DEVICESTREAM \_ 獨立 \_ 映射 \_ 資料流程屬性

指定影片捕獲來源上的影像資料流程是否與影片資料流程無關。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

某些 USB 攝影機會公開產生仍為影像的資料流程。 在某些相機中，影像串流只會傳回影片串流中的下一個畫面格。 在其他相機中，影像串流會獨立于影片串流。 如果相機有獨立的影像串流，則在影像串流上，capture 裝置的媒體來源會將此屬性設定為 **TRUE** 。

若要取得這個屬性，請執行下列動作：

1.  查詢 [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) 介面的媒體來源。
2.  呼叫 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) 來取得資料流程的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。
3.  呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 以取得屬性。

只有當 [MF \_ DEVICESTREAM \_ 影像 \_ 資料流程](mf-devicestream-image-stream.md) 屬性為 **TRUE** 時，才會套用此屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




