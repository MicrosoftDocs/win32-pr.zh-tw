---
description: 指定緩衝區是否包含 Advanced 系統格式的開頭 (ASF) 封包。
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: 'MFASFSPLITTER_PACKET_BOUNDARY 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997096"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a>MFASFSPLITTER 封 \_ 包 \_ 界限屬性

指定緩衝區是否包含 Advanced 系統格式的開頭 (ASF) 封包。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

如果媒體緩衝區透過 **QueryInterface** 公開 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面，且這個屬性的值為非零值，則 ASF 分隔器會將緩衝區視為新封包的開頭。

如果您使用 ASF 分隔器來剖析 ASF 資料，則會套用此屬性。 如果您的 ASF 資料具有可變的封包長度，您必須在傳遞給 [**IMFASFSplitter：:P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) 方法的媒體緩衝區上設定此屬性。 如果緩衝區包含新封包的開頭，請將屬性設定為 **TRUE** 。 如果緩衝區包含前一個封包的接續，請將屬性設定為 **FALSE**。 緩衝區無法跨越多個封包。

若為具有固定封包大小的 ASF 資料，則不需要此屬性，而且緩衝區可以橫跨多個封包。

請注意，媒體基礎提供的標準 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 不會公開 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)。 若要使用此屬性，您必須提供您自己的 **IMFMediaBuffer** 實值;例如，藉由包裝 [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer)所傳回的緩衝區。

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

[ASF 屬性](asf-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




