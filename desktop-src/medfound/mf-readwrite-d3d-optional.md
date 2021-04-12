---
description: 指定應用程式是否需要來源讀取器或接收寫入器中的 Microsoft Direct3D 支援。
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: 'MF_READWRITE_D3D_OPTIONAL 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c78295dd12e5d187c9be380305dc225d7e8e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194983"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a>MF \_ READWRITE \_ D3D \_ 選用屬性

指定應用程式是否需要 [來源讀取](source-reader.md) 器或 [接收寫入器](sink-writer.md)中的 Microsoft Direct3D 支援。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

只有當應用程式使用 [mf \_ 來源 \_ 讀取器 \_ d3d \_ 管理員](mf-source-reader-d3d-manager.md) 或 [mf \_ 接收 \_ 寫入器 \_ d3d \_ 管理員](mf-sink-writer-d3d-manager.md) 屬性啟用 Direct3D 支援時，才適用此屬性。

如果應用程式啟用 Direct3D 支援，來源讀取器和接收寫入器都會嘗試配置適用于影片的 Direct3D 表面。 如果失敗，而 MF \_ READWRITE \_ D3D \_ 選擇性屬性為 **TRUE**，則來源讀取器/接收寫入器會切換回配置系統記憶體中的影片表面。 否則，如果無法配置 Direct3D 介面，且 MF \_ READWRITE \_ D3D \_ 選用為 **FALSE**，則在處理期間會發生錯誤。

如果應用程式沒有啟用 Direct3D 支援，來源讀取器/接收寫入器會使用系統記憶體，並忽略 MF \_ READWRITE \_ D3D 選擇性的值 \_ 。

此屬性是選擇性的。 預設值為 **FALSE**。 當您建立來源讀取器或接收寫入器時，請設定屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mfreadwrite。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[接收寫入器屬性](sink-writer-attributes.md)
</dt> <dt>

[來源讀取器屬性](source-reader-attributes.md)
</dt> </dl>

 

 




