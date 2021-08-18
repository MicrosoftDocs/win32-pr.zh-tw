---
description: 指出 Microsoft 媒體基礎轉換 (MFT) 應該允許在任何指定時間1-12 的漸進樣本數目下限。
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: 'MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48df5262e225b8768d3251f9768cf2156ee2acacb19ca70752ae5bf989b682ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955428"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a>MF \_ SA \_ 最小 \_ 輸出 \_ 範例 \_ 計數 \_ 漸進屬性

指出 Microsoft 媒體基礎轉換 (MFT) 應該允許在任何指定時間1-12 的漸進樣本數目下限。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性只適用于使用迴圈緩衝區配置其專屬輸出範例的 MFTs。 其他 MFTs 會忽略此屬性。

若要設定此屬性：

1.  在解碼器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。
2.  呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) 以加入屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




