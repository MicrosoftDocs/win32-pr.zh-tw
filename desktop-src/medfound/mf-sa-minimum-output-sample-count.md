---
description: 指定 Microsoft 媒體基礎轉換 (MFT) 在管線中隨時都未完成之輸出樣本的最大數目。
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: 'MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf168158fd6a5f9a173d4d5d25dda3fa5b16d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191628"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a>MF \_ SA \_ 最小 \_ 輸出 \_ 範例 \_ 計數屬性

指定 Microsoft 媒體基礎轉換 (MFT) 在管線中隨時都未完成之輸出樣本的最大數目。

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
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 




