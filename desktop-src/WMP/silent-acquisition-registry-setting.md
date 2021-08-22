---
title: 無訊息取得登錄設定
description: 無訊息取得登錄設定
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bdab93c58dd92b5f0522f26ea192150cad4a44ae9a6edfbd0bde770f07a0262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507958"
---
# <a name="silent-acquisition-registry-setting"></a>無訊息取得登錄設定

Microsoft Windows Media Player 會使用下列登錄值來判斷是否要啟用無訊息取得，這是當使用者播放或同步受保護的內容時，播放玩家自動下載許可權的狀態。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **MediaPlayer** \\ **喜好** 設定 \\ **SilentAcquisition**

SilentAcquisition 值的格式如下：



| 名稱              | 類型           | 描述                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| SilentAcquisition | **REG \_ DWORD** | 將此值設定為1，以啟用無訊息取得，或將它設定為0以停用無訊息取得。 預設值是 1。 |



 

若要指定值，使用者可以開始 Windows Media Player，開啟 [**選項**] 對話方塊，按一下 [**隱私權**] 索引標籤，然後選取或清除 [**當我播放或同步處理檔案時自動下載許可權**] 核取方塊。 選取此核取方塊會將 SilentAcquisition 設定為 1;清除此核取方塊會將它設定為0。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**登錄設定**](registry-settings.md)
</dt> </dl>

 

 




