---
description: 允許增強型影片轉譯器 (EVR) 將其輸出限制為符合 GPU 頻寬。
ms.assetid: d591af2e-d47d-4220-a4f6-968f2ac45284
title: 'EVRConfig_AllowDropToThrottle 屬性 (Uuid. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97cbab6fae6644b3c0187d09edb59ab2538012e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026036"
---
# <a name="evrconfig_allowdroptothrottle-attribute"></a>EVRConfig \_ AllowDropToThrottle 屬性

允許增強型影片轉譯器 (EVR) 將其輸出限制為符合 GPU 頻寬。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

您可以在 EVR 媒體接收上設定這個屬性。 若要設定屬性，請使用 **QueryInterface** 來查詢 [**IMFATTRIBUTES**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的 EVR 媒體接收。

設定這個屬性的效果與在 EVR 上設定 **MFVideoRenderPrefs \_ AllowOutputThrottling** 旗標相同。 如需此旗標的說明，請參閱 [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) 。

這個屬性的 GUID 常數是從 strmiids 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Uuid。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[EVR 屬性](enhanced-video-renderer-attributes.md)
</dt> <dt>

[影片品質管制](video-quality-management.md)
</dt> </dl>

 

 




