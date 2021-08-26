---
description: 指定媒體基礎轉換 (MFT) 應該如何輸出 3D stereoscopic 影片串流。
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: 'MF_ENABLE_3DVIDEO_OUTPUT 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed361ef53d628e0970ffa35f9920750c9d3b0f7efbe81a0ef8759e8ba00a45ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013168"
---
# <a name="mf_enable_3dvideo_output-attribute"></a>MF \_ 啟用 \_ 3DVIDEO \_ 輸出屬性

指定媒體基礎轉換 (MFT) 應該如何輸出 3D stereoscopic 影片串流。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

屬性的值是 [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) 列舉的成員。

只有當 MFT [ \_ 支援 \_ 3DVIDEO](mft-support-3dvideo.md)屬性的 **值為 TRUE** 時，才會套用此屬性。

若要取得或設定此屬性，請呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 MFT 的全域屬性存放區。

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

 

 




