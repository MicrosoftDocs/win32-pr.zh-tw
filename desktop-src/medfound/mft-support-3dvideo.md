---
description: 指定媒體基礎轉換 (MFT) 是否支援 3D stereoscopic 影片。
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: 'MFT_SUPPORT_3DVIDEO 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbc7208f9bbcf2c638ae83e988c6e541a4be2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992426"
---
# <a name="mft_support_3dvideo-attribute"></a>MFT \_ 支援 \_ 3DVIDEO 屬性

指定媒體基礎轉換 (MFT) 是否支援 3D stereoscopic 影片。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

若要查詢這個屬性，請呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 MFT 的全域屬性存放區。 如果 **GetAttributes** 成功，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

這個屬性的預設值為 **FALSE**。 將此屬性視為唯讀。 請勿變更值;MFT 會忽略值的任何變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




