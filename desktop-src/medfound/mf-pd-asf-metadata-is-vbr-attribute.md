---
description: 指定 Advanced 的系統格式 (ASF) 檔案是否使用 (VBR) 編碼的變數位元速率。
ms.assetid: 69888d66-8e96-4a20-b8c5-a01267ff3c05
title: 'MF_PD_ASF_METADATA_IS_VBR 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e97d471c6a6466290c5b2ac490f88ae33de29aa3823af420ef8b8116a81192a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955418"
---
# <a name="mf_pd_asf_metadata_is_vbr-attribute"></a>MF \_ PD \_ ASF \_ 中繼資料 \_ 是 \_ VBR 屬性

指定 Advanced 的系統格式 (ASF) 檔案是否使用 (VBR) 編碼的變數位元速率。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。 如果值為 **TRUE**，則表示檔案是使用 VBR 編碼。 如果值為 **FALSE** 或屬性不存在，則檔案不會使用 VBR 編碼。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會產生這個屬性，並在表示描述項上設定它。

> [!Note]  
> 這個屬性會對應至 Windows 媒體格式 SDK 中的 **IsVBR** 屬性。

 

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
</dt> <dt>

[簡報描述項](presentation-descriptors.md)
</dt> </dl>

 

 




