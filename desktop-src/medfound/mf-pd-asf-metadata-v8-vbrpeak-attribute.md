---
description: 以變動的位元速率指定最高的瞬間位元速率 (VBR) Advanced Systems 格式 (ASF) 檔。
ms.assetid: a31f447d-b718-4f8d-b0d5-643497339557
title: 'MF_PD_ASF_METADATA_V8_VBRPEAK 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bfe0784a9bd43ddb68ef2b8457205b389149a41011e46cb748cc7c6d4b7f4f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876232"
---
# <a name="mf_pd_asf_metadata_v8_vbrpeak-attribute"></a>MF \_ PD \_ ASF \_ 中繼資料 \_ V8 \_ VBRPEAK 屬性

以變動的位元速率指定最高的瞬間位元速率 (VBR) Advanced Systems 格式 (ASF) 檔。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會產生這個屬性。

> [!Note]  
> 這個屬性只適用于 Windows 媒體格式 SDK 第8版所建立的檔案。 它會對應至 Windows 媒體格式 SDK 中的 **VBRPeak** 屬性。

 

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

 

 




