---
description: 指定與拓撲節點相關聯的轉換是否支援 (DXVA) 的 DirectX Video 加速。
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: 'MF_TOPONODE_D3DAWARE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d94d06f2834092159fb813ecffd69ec8a157c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469492"
---
# <a name="mf_toponode_d3daware-attribute"></a>MF \_ TOPONODE \_ D3DAWARE 屬性

指定與拓撲節點相關聯的轉換是否支援 (DXVA) 的 DirectX Video 加速。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

這個屬性會套用至 (**MF \_ 拓撲 \_ 轉換 \_ 節點**) 的轉換節點。

應用程式通常不會直接使用此屬性。 當基礎媒體基礎轉換具有 [**MF \_ SA \_ D3D \_ 感知**](mf-sa-d3d-aware-attribute.md) 屬性時，媒體會話會在轉換節點上設定此屬性。

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

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> </dl>

 

 




