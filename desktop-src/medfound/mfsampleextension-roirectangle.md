---
description: 指定感興趣區域的界限，指出需要不同品質的框架區域。
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: 'MFSampleExtension_ROIRectangle 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976822"
---
# <a name="mfsampleextension_roirectangle-attribute"></a>MFSampleExtension \_ ROIRectangle 屬性

指定感興趣區域的界限，指出需要不同品質的框架區域。

## <a name="data-type"></a>資料類型

**[**ROI \_**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** 儲存為 **BLOB** 的區域

## <a name="remarks"></a>備註

將 [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) 成功設定為編碼器 MFT 上的非零值之後，應用程式可以在輸入範例上設定此屬性，並預期它會被接受。

如果 [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) 未設定為非零值，則在 \_ 輸入範例上會忽略 MFSampleExtension ROIRectangle 屬性。

MFSampleExtension \_ ROIRectangle 是在輸入範例上設定的，而且只會套用至目前的輸入範例。

[**ROI \_ 區域**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)結構上的 [ **QPDelta** ] 欄位會從框架的其餘部分，指定指定區域的量化參數差異。 如果 **QPDelta** 是正數，則表示應用程式希望矩形的品質比框架的其餘部分低。

H.264 **/AVC 編碼器：** **QPDelta** 應介於 \[ -25、+ 25 之間 \] 。 編碼器應確定最終的 QP 位於適用于影片標準的有效範圍內。

指定的區域不需要 MB 對齊。 編碼器具有決定實際界限的彈性。 建議您涵蓋整個指定的區域。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




