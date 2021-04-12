---
title: 調整授權取得對話方塊的大小
description: 調整授權取得對話方塊的大小
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Windows Media Player，重設授權取得的大小對話方塊
- Windows Media Player，授權取得對話方塊
- Windows Media Player，DRM_LicenseAcqURL 屬性
- 調整授權取得大小對話方塊
- 取得授權對話方塊
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372390"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a>調整授權取得對話方塊的大小

您可以將查詢字串參數附加至您為 **DRM \_ LicenseAcqURL** 屬性提供的 URL，以指定 Windows Media Player 10 或更新版本的授權取得對話方塊的大小。 下表列出參數。



| 參數 | Description                                        |
|-----------|----------------------------------------------------|
| *DlgX*    | 指定對話方塊的寬度（以圖元為單位）。  |
| *DlgY*    | 指定對話方塊的高度（以圖元為單位）。 |



 

例如，下列授權取得 URL 會導致 [授權取得] 對話方塊開啟，大小為800乘以600圖元：


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



對話方塊的大小上限絕不會超過目前的螢幕尺寸減去20圖元。 大小下限為 333 x 210 圖元 (預設大小) 。

這項功能需要 Windows Media Player 10 或更新版本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




