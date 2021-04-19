---
description: 指出範例中的 NALUs 長度。 這是在對 h.264 解碼器壓縮的輸入範例上設定的 MF BLOB。
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: 'MF_NALU_LENGTH_INFORMATION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992029"
---
# <a name="mf_nalu_length_information-attribute"></a>MF \_ NALU \_ 長度 \_ 資訊屬性

指出範例中的 NALUs 長度。 這是在對 h.264 解碼器壓縮的輸入範例上設定的 MF **BLOB** 。

## <a name="data-type"></a>資料類型

**Blob**

## <a name="remarks"></a>備註

若要設定此屬性，媒體的類型必須是 MEDIASUBTYPE \_ H264，而且必須在 MEDIASUBTYPE H264 的輸入媒體類型上設定 [ [MF \_ NALU \_ 長度] \_ 設定](mf-nalu-length-set.md) 屬性 \_ 。

在 \_ \_ 輸入範例上將 MF NALU 長度資訊設定 \_ 為 **BLOB** ，範例中的每個 NALU 都有一個 DWORD。 例如，如果有 AUD (9 個位元組) ，SPS (25 個位元組) 、PPS (10 個位元組) 、IDR slice1 (50 k) 、IDR 配量 2 (60 k) ，然後在 **BLOB** 中應該會有5個具有值9、25、10、50 k、60 k 的 dword。

以下是設定 **blob** 的一些程式碼，其中 **rgdwNALULengthInfo** 是 DWORD 類型的陣列，而 **UiNaluLengthIdx** 則是設定為 **BLOB** 的有效 NALU 長度。


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




