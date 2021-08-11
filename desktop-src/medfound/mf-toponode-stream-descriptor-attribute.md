---
description: 包含媒體來源的資料流程描述元指標。
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: 'MF_TOPONODE_STREAM_DESCRIPTOR 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92517560f0a1f60681afc1209d6d14d3e3c5d663958d365d18b20558c0003199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244322"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a>MF \_ TOPONODE \_ 資料流程 \_ 描述項屬性

包含媒體來源的資料流程描述元指標。

## <a name="data-type"></a>資料類型

**IUnknown\***

## <a name="remarks"></a>備註

這個屬性會套用至 (**MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) 的來源節點。

屬性的值是資料流程描述項之 [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) 介面的指標。 這是必要屬性。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> </dl>

 

 




