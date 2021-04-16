---
title: 桌面體驗
description: 全新的 Windows 7 desktop 讓您的應用程式實現生命。
ms.assetid: e706167a-435b-4c32-bb64-87113f368866
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3476f70c46aecceb365e17dba1803b876fd51e8d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "104550058"
---
# <a name="the-desktop-experience"></a>桌面體驗

全新的 Windows 7 desktop 讓您的應用程式實現生命。 應用程式現在更容易探索、資訊和互動。 新式和直覺的使用者介面可讓您更輕鬆地使用 Windows 7 進行開發。 新的桌面和應用程式體驗包含下列各項：

-   增強的工作列引進了互動式縮圖，並可讓應用程式進行最小化的動畫和互動。
-   目的地概念讓使用者只要按一下，就能點擊最常使用的檔案、位置或工作。
-   *功能區* 的新控制項和 api （以 OFFICE 流暢 UI 為基礎）可讓您輕鬆地將 *功能區* 樣式控制項、功能表和資源庫新增至您的應用程式。
-   動畫架構可協助您增強自訂動畫。

小工具平臺的增強功能可讓應用程式在安裝或首次執行體驗期間安裝隨附的小工具。

![顯示 Windows 7 desktop 的螢幕擷取畫面。](images/windows7-6.jpg)

全新的 Windows 7 desktop 將應用程式帶入生活

## <a name="jump-listsgetting-users-into-your-application-quickly"></a>跳躍清單-快速讓使用者進入您的應用程式

跳躍清單可協助使用者進入想要更快的位置。 跳躍清單是在應用程式內開啟的檔案、Url、工作或自訂專案。 [ *開始* ] 功能表和工作列中的新跳躍清單功能表，可讓您只需按一下就能使用一般的目的地和按鍵工作。 [快捷方式清單] 功能表會根據所使用的頻率和最近使用的專案，自動填入。 開發人員可以根據自己的語義提供自訂跳躍清單。 應用程式也可以 *定義要* 出現在功能表中的工作，這些是使用者想要直接存取之應用程式的動作，例如撰寫電子郵件。  (參閱 [工作列擴充](../shell/taskbar-extensions.md) 功能和 [ICustomDestinationList 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)。 ) 

![跳躍清單](images/windows7-7.jpg)

跳躍清單可協助使用者取得他們想要更快執行的位置

## <a name="enhanced-taskbar"></a>增強的工作列

有了 Windows 7 的新工作列之後，應用程式就能以更直覺的方式，為使用者提供更多的資訊。 例如，應用程式可以在其工作列按鈕中顯示進度列，讓使用者可以隨時留意進度，而不需要讓視窗保持可見。 這有助於追蹤耗時的作業，例如檔案複製、下載、安裝或媒體燒錄。 圖示重迭可顯示在應用程式工作列按鈕的右下方區域，用來傳達狀態或通知 (例如新的郵件) 。 新的縮圖 Api 可讓應用程式針對這些視窗定義子視窗和對應的縮圖影像。 縮圖工具列提供了控制一般動作的位置，而不需要進行視窗還原，例如媒體的 *播放/停止* 。  (參閱 [工作列擴充](../shell/taskbar-extensions.md) 功能和 [Windows 7：開發人員資源](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples)。 ) 

## <a name="gadgets-platform"></a>小工具平臺

小工具是 Windows Vista 桌面的常用功能，在 Windows 7 中，應用程式更容易安裝小工具。 在 Windows 7 中，應用程式可以在應用程式安裝期間，以程式設計的方式將小工具新增至 Windows 桌面，或是先執行。 這表示應用程式的現成體驗可以包含簡單的核取方塊，例如，在應用程式準備好可供使用的情況下，立即安裝可在桌面上使用的輔助小工具。  (請參閱 [小工具平臺簡介](/previous-versions/windows/desktop/gadgetplatform/introduction-to-the-gadget-platform)) 。

![windows 小工具](images/windows7-8.jpg)

在 Windows 7 中，應用程式更容易安裝小工具

## <a name="windows-ribbon"></a>Windows 功能區



Windows 功能區控制項可協助開發人員將應用程式最常存取的功能直接公開給使用者，以提升可用性。 功能區可讓使用者更輕鬆地尋找和使用應用程式功能，因為隱藏了較少的功能，進而提高生產力。 功能區是設計成在標準 Windows 應用程式中，功能表、工具列、工作窗格和對話方塊的命令展示模型的意圖型替代方案。

功能區控制項包含一組 Win32APIs，可覆寫最上層的功能表列功能，並改為轉譯功能區樣式的命令 UI。 它類似于 2007 Office system 中 *功能區* 的功能和外觀。 UI 是由數個子控制項所組成，其中包括下列各項：

-   應用程式按鈕 (或 pearl) 
-   快速存取工具列
-   內容索引標籤的 *功能區* 控制項
-   迷你工具列
-   樣式庫

範本和標記撰寫可供開發人員用來快速開發和整合功能區功能。  (參閱 [Windows 功能區架構](../windowsribbon/-uiplat-windowsribbon-entry.md) 和 [Windows 功能區架構：開發人員資源](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsRibbon)。 ) 

![功能區工具列](images/windows7-9.jpg)

功能區控制項可協助開發人員藉由公開應用程式最常存取的功能來改善可用性

## <a name="animation"></a>動畫

平滑動畫是許多圖形化 UI 應用程式的基礎，而 Windows 7 引進了原生動畫架構來管理動畫的排程和執行。 動畫 framework 提供實用數學函式的程式庫，可在一段時間內指定行為，也可讓開發人員提供自己的行為函數。 當多個動畫嘗試同時處理相同值時，此架構可支援複雜的衝突解決。 應用程式可以指定必須先完成一個動畫，才能開始另一個動畫，並可在設定的時間內強制完成。 新的架構也有助於動畫決定適當的持續時間。  (參閱 [Windows 動畫管理員](../uianimation/-main-portal.md)) 。

 

 