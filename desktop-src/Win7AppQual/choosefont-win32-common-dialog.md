---
description: .
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: ChooseFont () Win32 通用對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e55a31d1f4d5530e04fe455135952eb94cc4bda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986609"
---
# <a name="choosefont-win32-common-dialog"></a>ChooseFont () Win32 通用對話方塊

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-Windows 7  
**伺服器** -Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

**嚴重性** -低  
**頻率** -中型  




## <a name="description"></a>Description

Windows 7 包含 ChooseFont () Win32 通用對話方塊的數項更新。 這些分為兩種類別：

-   對話方塊的視覺效果重新整理
-   新顯示/隱藏字體功能的支援

**對話方塊** 重新整理會更新標準範本，讓對話方塊與 Windows 中的其他對話版面配置更具線。 它會將 WYSIWYG 引進字型顯示清單，以協助使用者選擇字型。 它也包含字型 CPL 的連結，可讓希望自訂其字型清單的使用者輕鬆存取。

**顯示/隱藏** 字型是新的 Windows 7 平臺功能，因此字型挑選清單中預設不會顯示不適合目前使用者語言設定的字型 (輸入方法) 。 使用者可以自訂要顯示在字型 CPL 中的字型，也可以停用此功能。

## <a name="manifestation-of-impact"></a>影響的表現

**對話方塊視覺效果重新整理**

我們在 Windows 7 中引進了兩個新範本 (一個用於載入 comctl32.dll 6 版或更新版本的應用程式，而另一個則適用于載入舊版) 的應用程式。

-   基於應用程式相容性的理由，這些新範本只會針對未攔截 ChooseFont 訊息佇列的應用程式載入。 連結訊息佇列的應用程式將會繼續看到舊的對話版面配置。
-   提供自己範本的應用程式將會繼續使用它們。

未取得新範本的應用程式將不會看到任何來自 Vista 的對話版面配置變更。 但仍應取得新的 WYSIWYG 字型預覽。

**顯示/隱藏字型**

針對所有版本的 ChooseFont，此對話方塊會使用目前使用者的顯示/隱藏字型設定來決定要顯示的字型清單。 這會導致在大部分的情況下顯示較少的字型清單。

## <a name="end-user-mitigation"></a>使用者緩和

**顯示/隱藏字型：** 若要停用字型隱藏，使用者應該移至字型 CPL 中的 [字型設定] 頁面，並取消選取 [

「隱藏以語言設定為基礎的字型」核取方塊

## <a name="developer-mitigation"></a>開發人員緩和

-   **視覺效果** 重新整理：提供專屬範本的應用程式開發人員可能會想要重新整理，使其符合適當的新 Windows 7 範本。 新的範本可在 Font-family 範本檔中使用。

    **注意：** 新發佈的範本包含額外的 SysLink 控制項，可提供快捷方式，讓使用者啟動字型 CPL 以顯示更多字型。 連結控制項需要第6版的 Windows 通用控制項程式庫 (comctl32.dll) 。 開發人員應提供資訊清單或指示詞，以指定使用第6版的 DLL （如果有的話）。 當應用程式使用舊版的通用控制項程式庫時，請改為使用「按鈕」控制項類型。

-   **顯示/隱藏字型：** 開發人員可以停用此功能，方法是 \_ 在 CHOOSEFONT 結構的 flags 成員中提供額外的旗標 (CF INACTIVEFONTS) 。 設定此旗標會使所有已安裝的字型顯示在字型清單中。
-   **顯示/隱藏字型：** 提供 ChooseFont 說明內容的應用程式可能會想要新增內容，以說明為什麼要減少字型清單，並將使用者導向字型 CPL 以自訂其字型清單。

## <a name="compatibility-performance-reliability-and-usability-testing"></a>相容性、效能、可靠性和可用性測試

應用程式掛上 ChooseFont 訊息佇列以自訂對話方塊的開發人員應確認其應用程式保留所有現有的功能。

使用旗標大幅修剪字型清單的應用程式，應該確保顯示的字型清單保持可接受。

 

 



