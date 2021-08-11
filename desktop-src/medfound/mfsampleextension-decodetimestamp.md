---
description: 包含範例 (DTS) 的解碼時間戳記。
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: 'MFSampleExtension_DecodeTimestamp 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0d72ea69f487efe24148fa8ce60ad05eb7a124673f02a78e70c67f604a51bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241479"
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
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[範例屬性](sample-attributes.md)
</dt> </dl>

 

 




