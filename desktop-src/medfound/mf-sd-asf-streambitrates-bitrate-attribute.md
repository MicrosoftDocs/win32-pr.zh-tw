---
description: 以 Advanced Systems 格式的資料流程指定平均位元速率（以每秒位數為單位）， (ASF) 檔。 這個屬性會對應至在 ASF 規格中定義的資料流程位元速率屬性物件。
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: 'MF_SD_ASF_STREAMBITRATES_BITRATE 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5132ba69f88ce3c0f62160e88d11a6b794b2f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984204"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a>MF \_ SD \_ ASF \_ STREAMBITRATES \_ 位元速率屬性

以 Advanced Systems 格式的資料流程指定平均位元速率（以每秒位數為單位）， (ASF) 檔。 這個屬性會對應至在 ASF 規格中定義的資料流程位元速率屬性物件。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會產生這個屬性，並在資料流程描述項上設定它。 應用程式可以藉由呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)，從展示描述項建立資料流程的資料流程描述項。

屬性值等於資料流程位速率屬性物件中的平均位元速率欄位。

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

 

 




