---
description: 定義轉碼拓撲之資料流程設定的設定檔旗標。 這些旗標定義于 MF \_ 轉碼 \_ 調整 \_ 設定檔 \_ 旗標列舉中。
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: 'MF_TRANSCODE_ADJUST_PROFILE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974540"
---
# <a name="mf_transcode_adjust_profile-attribute"></a>MF \_ 轉碼 \_ 調整 \_ 配置檔案屬性

定義轉碼拓撲之資料流程設定的設定檔旗標。 這些旗標定義于 [**MF \_ 轉碼 \_ 調整 \_ 設定檔 \_ 旗標**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) 列舉中。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

應用程式可以在轉碼設定檔上的容器層級設定這個屬性。 如果設定此屬性， [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) 函式會在拓撲建立期間變更資料流程屬性，視指定的旗標而定。 例如，如果應用程式指定 [ **MF \_ 轉碼 \_ 調整 \_ 設定檔] \_ 預設** 旗標，則會使用應用程式指定的資料流程設定來建立設定檔。

針對影片串流，畫面速率會根據媒體來源進行更新。 如果應用程式未指定交錯模式，預設會將設定檔更新為使用漸進式框架。

如果應用程式指定「 **MF \_ 轉碼 \_ 調整 \_ 設定檔 \_ 使用 \_ 來源 \_ 屬性** 」旗標，則會將遺失的資料流程屬性從輸入媒體來源複製到轉碼設定檔中的串流設定。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[轉碼 API](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




