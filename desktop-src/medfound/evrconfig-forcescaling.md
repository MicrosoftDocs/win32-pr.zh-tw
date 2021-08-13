---
description: 強制增強的影片轉譯器 (EVR) 將影片混在小於輸出矩形的矩形內，然後調整結果。
ms.assetid: f85c4114-ac94-4deb-a1cf-896209079f8b
title: 'EVRConfig_ForceScaling 屬性 (Uuid. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd85fa67af3cea27564400b86cf6c8e32e3c15645cbb4f84cc97344fbab9ef60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346198"
---
# <a name="evrconfig_forcescaling-attribute"></a>EVRConfig \_ ForceScaling 屬性

強制增強的影片轉譯器 (EVR) 將影片混在小於輸出矩形的矩形內，然後調整結果。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

您可以在 EVR 媒體接收上設定這個屬性。 若要設定屬性，請使用 **QueryInterface** 來查詢 [**IMFATTRIBUTES**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的 EVR 媒體接收。

設定這個屬性的效果與在 EVR 上設定 **MFVideoRenderPrefs \_ ForceScaling** 旗標相同。 如需此旗標的說明，請參閱 [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) 。

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

 

 




