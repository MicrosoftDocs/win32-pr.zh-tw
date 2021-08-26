---
description: 指定是否啟用 pan/掃描模式。
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: 'MF_MT_PAN_SCAN_ENABLED 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e78c38cd15f5d735d49b5689905a40d74614b46817a8621ce1dabcdc5a1b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955488"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>\_ \_ 已啟用 MF MT PAN \_ 掃描的 \_ 屬性

指定是否啟用 pan/掃描模式。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

如果此屬性為 **TRUE**，則只會顯示影片的移動流覽/掃描區域。 「移動流覽/掃描」區域是由 [**MF \_ MT \_ pan \_ 掃描 \_ 光圈**](mf-mt-pan-scan-aperture-attribute.md) 屬性所指定。

如果這個屬性為 **FALSE** 或未設定，則會顯示影片的整個顯示光圈。 顯示光圈是由 [**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**](mf-mt-minimum-display-aperture-attribute.md) 屬性所指定。

如果您將此屬性設定為 **TRUE**，也請設定 [ [**MF MT 移動 \_ \_ \_ 流覽 \_**](mf-mt-pan-scan-aperture-attribute.md) ] 屬性的值。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[圖片外觀比例](picture-aspect-ratio.md)
</dt> </dl>

 

 




