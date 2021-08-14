---
title: 桌面視窗管理員
description: 在 Windows Vista 中引進的桌面撰寫功能，基本上改變了應用程式在螢幕上顯示圖元的方式。
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- 桌面視窗管理員 (DWM) ，關於
- DWM (桌面視窗管理員) ，關於
- 桌面視窗管理員 (DWM) ，組合
- DWM (桌面視窗管理員) ，組合
- 桌面電腦群組合
- 組合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8259be171f225cc955546314febdff5395a47318499b830ee855bc8b985b025
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456038"
---
# <a name="desktop-window-manager"></a>桌面視窗管理員

在 Windows Vista 中引進的桌面撰寫功能，基本上改變了應用程式在螢幕上顯示圖元的方式。 啟用桌面組合時，個別的視窗就不再像在舊版 Windows 一樣直接繪製到螢幕或主要顯示裝置。 相反地，它們的繪圖會重新導向至視訊記憶體中的螢幕表面，然後轉譯成桌面影像並顯示在顯示器上。

桌面電腦群組合是由桌面視窗管理員 (DWM) 所執行。 透過桌面電腦群組合，DWM 可在桌面上啟用視覺效果，以及各種功能，例如半透明視窗框架、立體視窗轉換動畫、Windows Flip 和 Windows Flip3D，以及高解析度支援。

桌面視窗管理員會以 Windows 服務的形式執行。 您可以在 [服務] 下的 [系統管理工具] 主控台專案中啟用和停用，如桌面視窗管理員會話管理員。

應用程式可以透過 DWM Api 來控制或存取許多 DWM 功能。 下列檔說明 DWM Api 的功能和需求。

-   [DWM 總覽](desktop-window-manager-overviews.md)
-   [DWM 範例程式碼](dwm-samples.md)
-   [DWM 參考](reference.md)

 

 




