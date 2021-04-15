---
description: 影片媒體類型的圖元外觀比例。
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: 'MF_MT_PIXEL_ASPECT_RATIO 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511728"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a>MF \_ MT \_ 圖元 \_ 外觀 \_ 比例屬性

影片媒體類型的圖元外觀比例。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="remarks"></a>備註

上方的32位包含圖元外觀比例的分子，而較低的32位則包含分母。 分子是外觀比例的水準元件;分母是垂直的元件。

若要設定此屬性，請使用 [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) 函數。 若要取得這個屬性，請使用 [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) 函數。

圖元外觀比例描述顯示的影片影像中圖元的形狀。 如果影像具有非正方形圖元，請設定此屬性。 若要在具有正方形圖元的顯示裝置上正確顯示，影像必須以影像的圖元外觀比例反轉。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> <dt>

[圖片外觀比例](picture-aspect-ratio.md)
</dt> </dl>

 

 




