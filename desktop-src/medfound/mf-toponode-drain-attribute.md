---
description: 指定何時清空轉換。
ms.assetid: 68332106-d1fe-467b-8baa-1e592b9cc243
title: 'MF_TOPONODE_DRAIN 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26aa3d813bf92dde1bd22ecbb5615ba26425b381453154239a596193a885f4fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691183"
---
# <a name="mf_toponode_drain-attribute"></a>MF \_ TOPONODE \_ 清空屬性

指定何時清空轉換。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性會套用至 (**MF \_ 拓撲 \_ 轉換 \_ 節點**) 的轉換節點。

屬性的值是 [**MF \_ TOPONODE \_ 清空 \_ 模式**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) 列舉的成員。 如果未設定此屬性，則預設值為 [ **MF \_ TOPONODE \_ 清空 \_ 預設** 值]。

在使用 [**MFT \_ 訊息 \_ 命令 \_ 清空**](mft-message-command-drain.md)訊息的轉換上呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) ，以進行清空。 如需詳細資訊，請參閱 [**MFT \_ 訊息 \_ 類型**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) 列舉。

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

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> </dl>

 

 




