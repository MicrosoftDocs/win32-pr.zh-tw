---
description: 指定是否允許應用程式存取未壓縮的影片畫面。
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: 'MFPROTECTION_VIDEO_FRAMES 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997512"
---
# <a name="mfprotection_video_frames-attribute"></a>MFPROTECTION \_ 影片 \_ 畫面格屬性

指定是否允許應用程式存取未壓縮的影片畫面。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

值為0表示允許應用程式存取畫面格。 這可能是因為應用程式與使用中的特定內容保護系統之間的私用合約所決定。

如果應用程式提供有效的應用程式憑證，則值為1表示允許應用程式存取框架 (參閱 [**IMFMediaEngineProtectedContent：： SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)) 。

值為0xFFFFFFFF （預設值），表示不允許任何應用程式存取未壓縮的框架。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 UWP 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ UWP 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




