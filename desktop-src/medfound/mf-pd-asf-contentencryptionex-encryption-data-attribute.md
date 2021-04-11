---
description: 包含 Advanced 系統格式 (ASF) 檔的加密資料。 這個屬性會對應到 ASF 規格中定義的 ASF 標頭中的擴充內容加密物件。
ms.assetid: 8bf5e7a4-073f-4b2c-8e9c-49f6f11c9093
title: 'MF_PD_ASF_CONTENTENCRYPTIONEX_ENCRYPTION_DATA 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550e75f50a7f09556cd9dd89239b3f33fb74d289
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318800"
---
# <a name="mf_pd_asf_contentencryptionex_encryption_data-attribute"></a>MF \_ PD \_ ASF \_ CONTENTENCRYPTIONEX \_ 加密 \_ 資料屬性

包含 Advanced 系統格式 (ASF) 檔的加密資料。 這個屬性會對應到 ASF 規格中定義的 ASF 標頭中的擴充內容加密物件。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會建立展示描述項，並從擴充內容加密物件標頭產生此屬性。 Blob 的大小等於資料大小欄位。 Blob 中包含的位元組陣列等於 ASF 標頭的擴充內容加密物件中的資料欄位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
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

 

 




