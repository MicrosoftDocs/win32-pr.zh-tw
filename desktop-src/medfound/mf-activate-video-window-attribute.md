---
description: 影片裁剪視窗的控制碼。
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: 'MF_ACTI加值稅E_VIDEO_WINDOW 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994382"
---
# <a name="mf_activate_video_window-attribute"></a>MF \_ 啟用 \_ 影片 \_ 視窗屬性

影片裁剪視窗的控制碼。

## <a name="data-type"></a>資料類型

**UINT64**

視為 **DWORD \_ PTR** (**HWND**) 。

## <a name="remarks"></a>備註

這個屬性會套用至增強型影片轉譯器的啟用物件 (EVR) 。 當您呼叫 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) 來建立 EVR 啟用物件時，會自動設定此值。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[增強的影片轉譯器屬性](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[啟用物件](activation-objects.md)
</dt> </dl>

 

 




