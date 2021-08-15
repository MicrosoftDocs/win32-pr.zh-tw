---
description: 說明必須設定哪個登錄機碼，以防止自動播放。
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: 如何防止元件的自動播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b44817f6803c25bbf506a5f76c8b068c683af4b5d4c7536482c30cd3aee2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859685"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a>如何防止元件的自動播放

說明必須設定哪個登錄機碼，以防止自動播放。

## <a name="instructions"></a>指示


若要避免在回應事件時啟動自動播放，請新增下列 **REG \_ SZ** 值（如本範例所示）。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

值是)  (CLSID 的類別識別碼，可在執行中的物件資料表 (的 ROT) 得知產生事件的元件。 值沒有任何資料。

> [!IMPORTANT]
> 在此機碼下，Clsid 不會以大括弧括住 ( {} ) 。

 

 

 



