---
description: 指定來源讀取器是否啟用 (DXVA) 影片解碼器的 DirectX Video 加速。
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: 'MF_SOURCE_READER_DISABLE_DXVA 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320471"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a>MF \_ 來源 \_ 讀取器 \_ 停用 \_ DXVA 屬性

指定 [來源讀取器](source-reader.md) 是否啟用 (DXVA) 影片解碼器的 DirectX Video 加速。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

如果下列條件成立，則適用此屬性：

-   來源讀取器會解碼影片串流。
-   影片解碼支援 DXVA 解碼。
-   應用程式會使用 [MF \_ 來源讀取器的「 \_ \_ D3D \_ 管理員](mf-source-reader-d3d-manager.md) 」屬性來設定來源讀取器上的 [Direct3D 裝置管理員](direct3d-device-manager.md) 。

這個屬性可讓應用程式停用 DXVA，同時仍在對 Direct3D 介面進行解碼。

根據預設，來源讀取器使用 [Direct3D 裝置管理員](direct3d-device-manager.md) 有兩個用途：

-   啟用影片解碼中的 DXVA 解碼。
-   為影片範例配置 Direct3D 介面。

如果 MF \_ 來源讀取器的值 \_ \_ 停 \_ 用 DXVA 屬性為 **TRUE**，則來源讀取器將會停用 DXVA 解碼，不過它仍然會使用 [direct3d 裝置管理員](direct3d-device-manager.md) 來配置 direct3d 表面。

如果未設定 [Mf 來源讀取器] 的 [ [ \_ \_ \_ D3D \_ 管理員](mf-source-reader-d3d-manager.md) ] 屬性，則 \_ 會忽略 [mf 來源讀取器] 停用 \_ \_ \_ DXVA 屬性。

這個屬性的預設值為 **FALSE**，表示 DXVA 解碼會在可用時啟用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mfreadwrite。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[來源讀取程式](source-reader.md)
</dt> <dt>

[來源讀取器屬性](source-reader-attributes.md)
</dt> </dl>

 

 




