---
description: 包含加密 Advanced 系統格式的機密資料 (ASF) 檔。 這個屬性會對應至內容加密標頭的秘密資料欄位，定義于 ASF 規格中。
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: 'MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e628bf52aa08074473f14a84ee1d1fe39fe91c130aa9848be687601b864393a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104364"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a>MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ SECRET \_ DATA 屬性

包含加密 Advanced 系統格式的機密資料 (ASF) 檔。 這個屬性會對應至內容加密標頭的秘密資料欄位，定義于 ASF 規格中。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會在位元組陣列中填入 Secret 資料欄位。 陣列的大小等於內容加密標頭的秘密資料長度欄位。

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

 

 




