---
description: 指出 NALU 長度資訊將會以 BLOB 的形式傳送至每個壓縮的 h.264 範例。
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: 'MF_NALU_LENGTH_SET 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f409cb3c1846667ac21e7d46c559eefb0afc4fe4efbce1f454454d286733157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104384"
---
# <a name="mf_nalu_length_set-attribute"></a>MF \_ NALU \_ LENGTH \_ SET 屬性

指出 NALU 長度資訊將會以 **BLOB** 的形式傳送至每個壓縮的 h.264 範例。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

在 MEDIASUBTYPE H264 的輸入媒體類型上設定此屬性 \_ 。

\_ \_ \_ 在輸入媒體類型的 h.264 解碼器上設定 MF NALU 長度，指出每個輸入範例都有可用的 NALU 長度，而每個輸入範例都包含一個完整的主要圖片。

您可以從輸入範例上的 [MF \_ NALU \_ 長度 \_ 資訊](mf-nalu-length-information.md)屬性，取出包含 NALU 長度資訊的 **BLOB** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




