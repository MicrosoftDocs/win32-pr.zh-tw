---
description: 指定當資料流程的格式變更時，媒體會話是否嘗試修改拓撲。
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: 'MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468988"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a>MF \_ 拓撲 \_ 動態 \_ 變更 \_ 不 \_ 允許屬性

指定當資料流程的格式變更時，媒體會話是否嘗試修改拓撲。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>備註

如果串流期間的資料流程格式有所變更，則此屬性會控制媒體會話的回應方式。

如果格式變更，而 [MF \_ 拓撲 \_ 動態 \_ 變更 \_ 不 \_ 允許] 屬性為 **FALSE**，則媒體會話可能會將新節點插入拓撲中，以符合新的格式。 例如，如果影片大小變更，媒體會話可能會新增媒體基礎轉換 (MFT) 調整影片的大小。 否則，如果屬性為 **TRUE**，則媒體會話不會修改拓撲。

這個屬性的預設值為 **FALSE**。 建議的值為 **FALSE**。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> </dl>

 

 




