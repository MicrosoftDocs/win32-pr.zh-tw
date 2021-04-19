---
description: 指定輸出媒體類型上影片編碼的設定檔。 這是 MF \_ MT \_ MPEG2 \_ 配置檔案屬性的別名。
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: 'MF_MT_VIDEO_PROFILE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971601"
---
# <a name="mf_mt_video_profile-attribute"></a>MF \_ MT \_ 影片 \_ 配置檔案屬性

指定輸出媒體類型上影片編碼的設定檔。 這是 [MF \_ MT \_ MPEG2 \_ 設定檔](mf-mt-mpeg2-profile-attribute.md) 屬性的別名。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

**H.264 編碼器：**

已超出支援的設定檔，以包含 [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) 和 **eAVEncH264VProfile \_ ConstrainedHigh**。

編碼器應同時支援此屬性的 [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 和 [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) 。

這是靜態的，因此必須先設定影片編碼器，才能開始串流。 如果應用程式設定編碼器不支援的設定檔，則編碼器應該拒絕媒體類型。

建議的預設值： [**eAVEncH264VProfile \_ 主要**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) 設定檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
