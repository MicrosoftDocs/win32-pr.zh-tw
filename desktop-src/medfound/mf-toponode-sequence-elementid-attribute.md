---
description: 指定包含此來源節點的元素。
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: 'MF_TOPONODE_SEQUENCE_ELEMENTID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972279"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a>MF \_ TOPONODE \_ 序列 \_ ELEMENTID 屬性

指定包含此來源節點的元素。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性會套用至 (**MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) 的來源節點。

媒體管線會使用這個屬性來探索媒體來源是否屬於相同元素的一部分。 管線會將屬於相同元素的所有來源節點視為具有相同的時鐘。

當管線將包含來源節點的新拓撲排入佇列，而這些來源節點屬於先前拓撲中的元素時，管線會將這些來源節點視為與先前拓撲中該專案的來源節點相同的時鐘。

> [!Note]  
> 媒體管線不會以不同的頻率速率來更正來源節點的時間戳記。

 

可提供拓撲的媒體來源應該會執行 [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) 介面或 [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) 介面。 提供拓撲的媒體來源應該在其所建立的每個來源節點上設定 **MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID** 屬性。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> <dt>

[Sequencer 來源](sequencer-source.md)
</dt> </dl>

 

 




