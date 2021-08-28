---
description: 指定建立的 Advanced Systems 格式 (ASF) 檔的日期和時間。
ms.assetid: 97f80584-9d74-4ba5-80f4-ddb6f2bc4625
title: 'MF_PD_ASF_FILEPROPERTIES_CREATION_TIME 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1a015e251e04c706e2d36b7ab85cac4e8038ad2083c9e0089fbe847d835227a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104354"
---
# <a name="mf_pd_asf_fileproperties_creation_time-attribute"></a>MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 建立 \_ 時間屬性

指定建立的 Advanced Systems 格式 (ASF) 檔的日期和時間。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。 屬性的值是一個 **FILETIME** 結構，在 Windows SDK 中記載。

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

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF 標頭物件](asf-file-structure.md)
</dt> <dt>

[簡報描述項](presentation-descriptors.md)
</dt> </dl>

 

 




