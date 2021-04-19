---
description: 以 Advanced Systems 格式 (ASF) 檔指定資料流程所使用的語言。
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: 'MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2afcf2388d2c0641aede4ff0eaccac9178207fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977985"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a>MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 語言 \_ 識別碼 \_ 索引屬性

以 Advanced Systems 格式 (ASF) 檔指定資料流程所使用的語言。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性會套用至 ASF 內容的資料流程描述項。 值是包含在 [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md) 屬性中的語言清單索引。

這個屬性會對應至擴充資料流程屬性物件中的資料流程語言識別項索引欄位。 如需詳細資訊，請參閱 ASF 規格。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。 應用程式可以藉由呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)，從展示描述項建立資料流程的資料流程描述項。

您也可以藉由查詢適用于 [**MF \_ SD \_ language**](mf-sd-language-attribute.md) 屬性的資料流程描述元來取得語言標記。

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

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[資料流程描述元屬性](stream-descriptor-attributes.md)
</dt> <dt>

[ASF 標頭物件](asf-file-structure.md)
</dt> </dl>

 

 




