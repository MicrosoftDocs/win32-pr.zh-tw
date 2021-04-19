---
description: 指定拓撲載入器是否會啟用轉碼視頻處理器 (XVP) 。 針對轉換，啟用硬體加速色彩轉換。
title: 'MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK 屬性 (Mfidl) '
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981972"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a>MF \_ 拓撲 \_ 啟用 \_ XVP \_ 的 \_ 播放屬性

指定拓撲載入器是否會啟用轉碼視頻處理器 (XVP) 。 針對轉換，啟用硬體加速色彩轉換。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>備註

如果設定此屬性，拓撲載入器會在非轉碼拓撲解析期間，于必要時，提取視頻處理器。 當您使用拓撲來建立自己的 [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) 時，此屬性會告知載入器使用 XVP 進行轉換，而不是使用舊版色彩轉換器，進而啟用硬體加速色彩轉換;舊版色彩轉換器僅限軟體。

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

[Direct3D 裝置管理員](direct3d-device-manager.md)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> </dl>

 

 




