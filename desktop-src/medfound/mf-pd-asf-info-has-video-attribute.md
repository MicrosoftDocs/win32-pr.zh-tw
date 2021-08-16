---
description: 指定 Advanced Systems Format (ASF) 檔案是否至少包含一個影片串流。
ms.assetid: 98411c75-519f-4ace-999f-1ea22457ed4a
title: 'MF_PD_ASF_INFO_HAS_VIDEO 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b5012a7fc20628cf8b50a4fc72242c02779623beb8126525a51501f51e412a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876269"
---
# <a name="mf_pd_asf_info_has_video-attribute"></a>MF \_ PD \_ ASF \_ 資訊 \_ 有 \_ 影片屬性

指定 Advanced Systems Format (ASF) 檔案是否至少包含一個影片串流。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。 如果此值為 **TRUE**，表示檔案至少有一個影片資料流程。 否則，檔案不會包含任何影片串流。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Wmcontainer。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF 標頭物件](asf-file-structure.md)
</dt> </dl>

 

 




