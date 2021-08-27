---
description: 使用者介面 - 高 DPI 感知
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: 使用者介面 - 高 DPI 感知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52c2bb42ad2c54fc1d23e44edf54e4bc88f8ab40a3f3a04f9dbc57b484b55173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994578"
---
# <a name="user-interface---high-dpi-awareness"></a>使用者介面 - 高 DPI 感知

## <a name="affected-platforms"></a>受影響的平臺

 **客戶** 端-Windows XP \| Windows Vista \| Windows 7  

## <a name="feature-impact"></a>功能影響

**嚴重性** -中  
**頻率** -中型  

## <a name="description"></a>描述

目標是鼓勵終端使用者將其顯示器設為原生解析度，並使用 DPI 而非螢幕解析度來變更顯示文字和影像的大小。 Windows 7 可以自動偵測，並在其 oem 設定的電腦上，使用 DPI 設定自動偵測和設定預設的 DPI。 您可以使用一些工具來協助設計高度 DPI 感知的應用程式，以確保最容易閱讀的結果。

我們已將兩個新的高 DPI 功能新增至 Windows 7：

-   每個使用者的 DPI 設定 (先前每一部電腦) 
-   在不重新開機 (登出/登入的情況下，仍需要變更 DPI) 

## <a name="manifestation-of-impact"></a>影響的表現

未處理高 DPI 案例的應用程式可能會顯示視覺構件，包括：

-   由其他 UI 元素剪切 UI 或文字
-   不一致的字型大小
-   螢幕 Ui
-   文字或 UI 的模糊
-   中斷的拖放或其他輸入
-   全螢幕的 DX 應用程式呈現部分關閉畫面

## <a name="solution"></a>解決方案

將您的應用程式設為 DPI 感知：

1.  執行高階功能測試階段，包括在下列設定中安裝和卸載：

    | 設定                                              | 應該檢查哪些狀況                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1024 @ 120 DPI (125% 調整)                     | 這是 ~ 800x600 的有效解析度，因此請尋找在螢幕或版面配置問題中裁剪的 UI。 也請尋找晃動點陣圖 & 圖示。                         |
    | 1600x1200 @144 DPI (150% 調整)                     | 模糊的 UI。 確認所有的滑鼠作業都能正常運作，尤其是拖曳 & drop 作業。 也請確認全螢幕模式是否正常運作。                                     |
    | 已停用 DPI 虛擬化的 1600x1200 @ 144 DPI | 按鈕和 UI 通常不會與較大的文字相對應，& 將會有大量的文字裁剪。 尋找一般 & 晃動 bitmats & 圖示的版面配置問題。 |

    

     

2.  寫下所有找到的問題，包括位置、螢幕解析度和 DPI 設定，以及應用程式在其他 DPI/解析度設定中的行為，以達到完整性
3.  針對常見的 DPI 編碼問題檢查每個問題
4.  評估讓應用程式完全 DPI 感知的成本
5.  建立所需的高 DPI 資產清單 (例如按鈕、圖示) 
6.  完成步驟1中找到的 DPI 問題清單並加以修正
7.  整合步驟5中的新資產
8.  宣告您的應用程式 DPI 感知

## <a name="compatibility-performance-reliability-and-usability-testing"></a>相容性、效能、可靠性和可用性測試

重新執行 DPI 感知評量，並確認問題已修正。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [Windows 上的高 DPI 桌面應用程式開發](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   **接觸技術問題：**<disup@microsoft.com>

 

 
