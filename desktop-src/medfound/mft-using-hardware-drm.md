---
description: 指定 IMFTransform 是否使用硬體 DRM。
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b46760fd5759abdd601269f5905f0649145649713839de5fe6424bc36219c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473548"
---
# <a name="mft_using_hardware_drm-attribute"></a>\_使用 \_ 硬體 \_ DRM 屬性的 MFT

指定 IMFTransform 是否使用硬體 DRM。

## <a name="data-type"></a>資料類型

**UINT32** (視為 **BOOL**) 

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMTransfrom**](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a>備註

如果 MFT decrypter 指定此屬性設定為1，則會使用硬體 DRM。 如果 MFT decrypter 指定此屬性設為0，則不會使用硬體 DRM。 如果 MFT decrypter 未指定此屬性，或將它指定為不同的值，則不會 (或無法) 指出它是否使用硬體 DRM。


這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 102020年4月更新   <br/>                                       |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 




