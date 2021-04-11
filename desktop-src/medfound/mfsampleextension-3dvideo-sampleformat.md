---
description: 指定3D 影片框架如何儲存在媒體範例中。
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: 'MFSampleExtension_3DVideo_SampleFormat 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115012"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a>MFSampleExtension \_ 3DVideo \_ SampleFormat 屬性

指定3D 影片框架如何儲存在媒體範例中。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性的值是 [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) 列舉的成員。

產生3D 影片框架的元件應該在包含3D 框架的每個媒體範例上，將此屬性設定為 **TRUE** 。 如果 [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) 屬性為 **FALSE** 或未設定，則會忽略屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




