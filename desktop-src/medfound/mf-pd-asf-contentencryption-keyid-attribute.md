---
description: 指定加密 Advanced 系統格式 (ASF) 檔的金鑰識別碼。 這個屬性會對應至內容加密標頭的金鑰識別碼欄位，定義于 ASF 規格中。
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: 'MF_PD_ASF_CONTENTENCRYPTION_KEYID 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd49c7a006345cceba01edde7caf76e499323b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112888"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a>MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID 屬性

指定加密 Advanced 系統格式 (ASF) 檔的金鑰識別碼。 這個屬性會對應至內容加密標頭的金鑰識別碼欄位，定義于 ASF 規格中。

## <a name="data-type"></a>資料類型

寬字元字串

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會抓取金鑰識別碼欄位、將它轉換為寬字元字串，然後填入以 null 終止的 **WCHAR** 陣列。 陣列的大小等於內容加密標頭的金鑰識別碼長度欄位。

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

[**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF 標頭物件](asf-file-structure.md)
</dt> <dt>

[簡報描述項](presentation-descriptors.md)
</dt> </dl>

 

 




