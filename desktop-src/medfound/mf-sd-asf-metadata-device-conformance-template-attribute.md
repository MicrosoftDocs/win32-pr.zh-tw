---
description: 以 Advanced Systems 格式 (ASF) 檔，指定串流的裝置一致性範本。
ms.assetid: e0bfb393-c8de-47cf-b80a-b0d88722e815
title: 'MF_SD_ASF_METADATA_DEVICE_CONFORMANCE_TEMPLATE 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e0ae20ae02617fab6f9669a50c7b8383b90a9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983525"
---
# <a name="mf_sd_asf_metadata_device_conformance_template-attribute"></a>MF \_ SD \_ ASF \_ 中繼資料 \_ 裝置 \_ 一致性 \_ 範本屬性

以 Advanced Systems 格式 (ASF) 檔，指定串流的裝置一致性範本。

## <a name="data-type"></a>資料類型

寬字元字串

## <a name="remarks"></a>備註

這個屬性會套用至 ASF 內容的資料流程描述項。 如需裝置一致性範本的詳細資訊，請參閱 Windows Media Format SDK 中的「裝置一致性範本參數」主題。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。

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

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[資料流程描述元屬性](stream-descriptor-attributes.md)
</dt> <dt>

[ASF 標頭物件](asf-file-structure.md)
</dt> </dl>

 

 




