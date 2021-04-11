---
description: 設定影片防震 MFT 的處理模式。
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: 'MF_VIDEODSP_MODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114012"
---
# <a name="mf_videodsp_mode-attribute"></a>MF \_ VIDEODSP \_ 模式屬性

設定 [**影片防震 MFT**](video-stabilization-mft.md)的處理模式。

## <a name="data-type"></a>資料類型

**MFVideoDSPMode** 儲存為 **UIINT32**

## <a name="remarks"></a>備註

這個屬性的值是 [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) 列舉值。 這個屬性可用來啟用或停用影像穩定，並且可以針對每個輸出範例進行更新。

若要設定此屬性：

1.  在影片穩定的 MFT 上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) ，以取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。
2.  呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) 來設定屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**影片防震 MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




