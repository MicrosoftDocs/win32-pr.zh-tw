---
description: 允許增強型影片轉譯器 (EVR) 對 Microsoft Direct3D IDirect3DDevice9：:P 重發方法進行批次呼叫。
ms.assetid: 6dbb2839-97ea-4881-8f22-0f8e943a3071
title: 'EVRConfig_AllowBatching 屬性 (Uuid. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1013ca2578d8fd46ea4019035df1ba3397ad629fd27c1901cd92ac8de1bc43af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742377"
---
# <a name="evrconfig_allowbatching-attribute"></a>EVRConfig \_ AllowBatching 屬性

允許增強型影片轉譯器 (EVR) 對 Microsoft Direct3D **IDirect3DDevice9：:P 重發** 方法進行批次呼叫。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

您可以在 EVR 媒體接收上設定這個屬性。 若要設定屬性，請使用 **QueryInterface** 來查詢 [**IMFATTRIBUTES**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的 EVR 媒體接收。

設定這個屬性的效果與在 EVR 上設定 **MFVideoRenderPrefs \_ AllowBatching** 旗標相同。 如需此旗標的說明，請參閱 [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) 。

這個屬性的 GUID 常數是從 strmiids 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Uuid。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[EVR 屬性](enhanced-video-renderer-attributes.md)
</dt> <dt>

[影片品質管制](video-quality-management.md)
</dt> </dl>

 

 




