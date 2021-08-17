---
description: 指定拓撲載入器是否會啟用拓撲中的 Microsoft DirectX Video 加速 (DXVA) 。
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: 'MF_TOPOLOGY_DXVA_MODE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5462ccf575f94935d100eb70a6d806e139f09762151c2dad8d4e155ca5d1d17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875723"
---
# <a name="mf_topology_dxva_mode-attribute"></a>MF \_ 拓撲 \_ DXVA \_ 模式屬性

指定拓撲載入器是否會啟用拓撲中的 Microsoft DirectX Video 加速 (DXVA) 。

## <a name="data-type"></a>資料類型

**[**MFTOPOLOGY \_以 \_**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** **UINT32** 形式儲存的 DXVA 模式

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>備註

這個屬性的值是 [**MFTOPOLOGY \_ DXVA \_ 模式**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) 列舉常數。 預設值為 **MFTOPOLOGY \_ DXVA \_ default**。

這個屬性會控制哪些 MFTs 會收到 Direct3D 裝置管理員的指標。 若要啟用完整的影片加速，請將值設定為 **MFTOPOLOGY \_ DXVA \_ full**。 值 **MFTOPOLOGY \_ DXVA \_ 預設** 值是針對回溯相容性所定義，它會符合所有舊版 Microsoft 媒體基礎的行為。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Direct3D 裝置管理員](direct3d-device-manager.md)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> </dl>

 

 




