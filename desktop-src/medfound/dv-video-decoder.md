---
description: 媒體基礎 DV 影片解碼是可解碼 DV 影片的媒體基礎轉換。
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: DV 影片解碼
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd91cf325d9ba715d75aae884e29665d05d449ca39f01c195f9b13e2e1f8c1fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064091"
---
# <a name="dv-video-decoder"></a>DV 影片解碼

媒體基礎 DV 影片解碼是可解碼 DV 影片的 [媒體基礎轉換](media-foundation-transforms.md) 。

DV 影片解碼支援下列輸入類型：



| Subtype                 | 描述                  |
|-------------------------|------------------------------|
| **MFVideoFormat \_ DVC**  | DVC/DV 影片                 |
| **MFVideoFormat \_ DVHD** | HD-DVCR (1125-60 或 1250-50)  |
| **MFVideoFormat \_ DVSD** | SDL-DVCR (525-60 或 625-50)   |
| **MFVideoFormat \_ DVSL** | SD-DVCR (525-60 或 625-50)    |



 

它支援單一輸出類型：



| Subtype             | 描述 |
|---------------------|-------------|
| MFVideoFormat \_ YUY2 | YUY2 影片  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[影片媒體類型](video-media-types.md)
</dt> </dl>

 

 




