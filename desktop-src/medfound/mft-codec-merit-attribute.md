---
description: 包含硬體編解碼器的業績值。
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: 'MFT_CODEC_MERIT_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993019"
---
# <a name="mft_codec_merit_attribute-attribute"></a>MFT \_ 編解碼器的 \_ 業績 \_ 屬性屬性

包含硬體編解碼器的業績值。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

這個屬性是在代表硬體編解碼器的媒體基礎轉換 (MFT) 的啟用物件上設定的。 屬性的值是編解碼器的業績值。

如果設定了 **MFT \_ 列舉 \_ 旗標 \_ SORTANDFILTER** 旗標，則此屬性會控制 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函式列舉編解碼器的順序。 具有值的 MFTs 在清單中會比其他 MFTs 更高。

這個屬性不包含受信任的值。 若要驗證編解碼器的實際值，請呼叫 [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) 函數。

如果 MFT 編解碼器的 [使用規定] 屬性的值 \_ \_ \_ 與 [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit)所抓取的 [使用] 值不符， [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 方法將會失敗，並傳回 **MF \_ E \_ 不正確 \_ 編解碼器 \_**。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 




