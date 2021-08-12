---
title: 從應用程式偵測 Windows Media Player
description: 從應用程式偵測 Windows Media Player
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Windows Media Player，從應用程式偵測
- 從應用程式偵測 Windows Media Player
- 登錄，從應用程式偵測 Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5267dc6c3202d9ecf894377899dfb34cf02ad42dfee05f8d42896c39ae48fc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579484"
---
# <a name="detecting-windows-media-player-from-an-application"></a>從應用程式偵測 Windows Media Player

您可以藉由檢查下列登錄機碼來判斷安裝的 Windows Media Player 版本：

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Active Setup \\ 已安裝的元件**

針對 Windows Media Player 6.4，請查看金鑰 **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**。

針對 Windows Media Player 7 或更新版本，請查看金鑰 **{6BF52A52-394A-11d3-B153-00C04F79FAA6}**。

在上述任一機碼下，如果 **IsInstalled**<dl> <dt>

資料類型
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

資料類型
</dt> <dd>字串</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**轉散發 Windows Media Player 軟體**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




