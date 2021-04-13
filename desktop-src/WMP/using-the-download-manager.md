---
title: 使用下載管理員
description: 使用下載管理員
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player 線上商店，下載管理員
- 線上商店、下載管理員
- 輸入2個線上商店、下載管理員
- Windows Media Player，下載管理員
- Windows Media Player 下載管理員
- 下載管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372641"
---
# <a name="using-the-download-manager"></a>使用下載管理員

Windows Media Player SDK 包含範例網頁，示範如何使用下載管理員將檔下載至使用者的電腦。 您可以在安裝 SDK 的名稱為網頁的資料夾中找到範例。 檔案的名稱是範例 .asp。 此範例提供下列功能：

-   建立 **DownloadManager** 物件。
-   建立 **DownloadCollection** 物件。
-   當使用者按一下 [ **下載**] 時，就會開始下載五個檔案。 範例中提供預設檔案路徑。 您應該以您自己的伺服器上的檔案位置取代這些預設路徑。 您可以藉由變更指派給名為 g sFiles 之全域陣列的值來變更路徑 \_ 。
-   顯示使用者選取時的下載狀態資訊。
-   提供用來暫停、繼續、取消和移除下載專案的控制項。
-   使用 cookie 維護會話之間的下載集合相關資訊。 這點很重要，因為使用者可以隨時關閉播放程式。 此外，如果使用者在播放玩家切換工作窗格，線上商店會話就會結束。
-   預設會使用即時下載。 您可以變更名為 g sDLType 的變數值，將行為變更為背景下載 \_ 。 背景下載可用於 Microsoft Windows XP 作業系統。
-   將背景色彩與播放機色彩同步處理。 您可以使用這項功能，在使用者選擇變更播放程式的色彩時，讓您的線上商店變更外觀。

下列各節提供詳細資訊：

-   [初始化頁面](initializing-the-page.md)
-   [開始下載](starting-the-downloads.md)
-   [正在抓取狀態資訊](retrieving-status-information.md)
-   [維護會話資訊](maintaining-session-information.md)
-   [頁面的調試](debugging-the-page.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Type 2 線上商店的程式設計指南**](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




