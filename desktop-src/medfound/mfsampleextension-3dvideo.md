---
description: 指定媒體範例是否包含3D 影片框架。
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: 'MFSampleExtension_3DVideo 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb959accfb3326e90068a26247eeab25e9aeaddacb720a0dfd64aa6e5b237a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722798"
---
# <a name="mfsampleextension_3dvideo-attribute"></a>MFSampleExtension \_ 3DVideo 屬性

指定媒體範例是否包含3D 影片框架。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

如果此屬性為 **TRUE**，則媒體範例包含具有兩個或更多 stereoscopic views 的影片畫面。 預設值為 **FALSE**。

產生3D 影片框架的元件應該在包含3D 框架的每個媒體範例上，將此屬性設定為 **TRUE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




