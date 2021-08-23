---
description: 指出 Microsoft 媒體基礎轉換 (MFT) 需要配置給漸進式內容的樣本數。
ms.assetid: 69F9EA59-41B4-4DE5-A77D-1D0E59BFBF3A
title: 'MF_SA_REQUIRED_SAMPLE_COUNT_PROGRESSIVE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d981535d66c0e6b50b82bc5b59d7096658a775651574cd4dbb26166b3e418a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740049"
---
# <a name="mf_sa_required_sample_count_progressive-attribute"></a>MF \_ SA \_ 必要 \_ 範例 \_ 計數 \_ 漸進屬性

指出 Microsoft 媒體基礎轉換 (MFT) 需要配置給漸進式內容的樣本數。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

如果下一個節點下游有 [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)，就會使用這個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




