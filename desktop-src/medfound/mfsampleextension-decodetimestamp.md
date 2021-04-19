---
description: 包含範例 (DTS) 的解碼時間戳記。
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: 'MFSampleExtension_DecodeTimestamp 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996634"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a>MFSampleExtension \_ DecodeTimestamp 屬性

包含範例 (DTS) 的解碼時間戳記。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="remarks"></a>備註

屬性（attribute）的值為 100-毫微秒單位的 DTS。 DTS 是以一些編碼標準（包括 MPEG）來定義。 DTS 會指定編碼圖片應該解碼的時機。 如果編碼的影片包含 B 個框架，則 DTS 可能與展示時間不同，因為 B 圖片在位流中的時態順序不會出現。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[範例屬性](sample-attributes.md)
</dt> </dl>

 

 




