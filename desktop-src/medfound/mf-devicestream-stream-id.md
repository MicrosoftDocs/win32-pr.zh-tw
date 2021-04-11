---
description: 針對影片捕獲裝置上的資料流程，指定內核串流 (KS) 識別碼。
ms.assetid: 03C48CBA-FAD0-4127-89E5-3F1874BF32DB
title: 'MF_DEVICESTREAM_STREAM_ID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f7143487af1125da9334fc39c152aee9363b97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026449"
---
# <a name="mf_devicestream_stream_id-attribute"></a>MF \_ DEVICESTREAM \_ 串流 \_ 識別碼屬性

針對影片捕獲裝置上的資料流程，指定內核串流 (KS) 識別碼。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

若要取得這個屬性，請執行下列動作：

1.  查詢 [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) 介面的媒體來源。
2.  呼叫 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) 來取得資料流程的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。
3.  呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 以取得屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




