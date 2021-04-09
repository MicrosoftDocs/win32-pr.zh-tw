---
description: 媒體基礎 DV 影片解碼是可解碼 DV 影片的媒體基礎轉換。
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: DV 影片解碼
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689307"
---
# <a name="dv-video-decoder"></a>DV 影片解碼

媒體基礎 DV 影片解碼是可解碼 DV 影片的 [媒體基礎轉換](media-foundation-transforms.md) 。

DV 影片解碼支援下列輸入類型：



| Subtype                 | Description                  |
|-------------------------|------------------------------|
| **MFVideoFormat \_ DVC**  | DVC/DV 影片                 |
| **MFVideoFormat \_ DVHD** | HD-DVCR (1125-60 或 1250-50)  |
| **MFVideoFormat \_ DVSD** | SDL-DVCR (525-60 或 625-50)   |
| **MFVideoFormat \_ DVSL** | SD-DVCR (525-60 或 625-50)    |



 

它支援單一輸出類型：



| Subtype             | Description |
|---------------------|-------------|
| MFVideoFormat \_ YUY2 | YUY2 影片  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[影片媒體類型](video-media-types.md)
</dt> </dl>

 

 




