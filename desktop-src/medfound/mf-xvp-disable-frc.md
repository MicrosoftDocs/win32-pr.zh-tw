---
description: 停用視頻處理器 MFT 中的畫面播放速率轉換。
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: 'MF_XVP_DISABLE_FRC 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e82c60438a91111ffce6cc80c71fa76231b8e00d85644f4f56f1b496202d62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940328"
---
# <a name="mf_xvp_disable_frc-attribute"></a>MF \_ XVP \_ 停用 \_ FRC 屬性

停用 [**視頻處理器 MFT**](video-processor-mft.md)中的畫面播放速率轉換。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

如果此屬性為 **TRUE**，則視頻處理器不會執行畫面播放速率轉換。 根據預設，視頻處理器會將畫面播放速率轉換成符合輸出媒體類型。

若要設定此屬性：

1.  在視頻處理器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 。
2.  呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

開始串流之前，請設定屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




