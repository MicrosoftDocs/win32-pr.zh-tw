---
title: 使用 DirectX 進行開發的必要條件
description: 當您開始使用 DirectX 開發 Windows 應用程式時，請記住此頁面上的必要條件。 這包括您在深入探索之前需要知道的技術。
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- DirectX 應用程式，必要條件
- DirectX 應用程式，Windows Store 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5e09484bef67546047214702fab7d2d0a5c48d
ms.sourcegitcommit: 6394972f1e8b01229db602469df6bb137e31d776
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/16/2020
ms.locfileid: "104463976"
---
# <a name="prerequisites-for-developing-with-directx"></a>使用 DirectX 進行開發的必要條件

當您開始使用 DirectX 開發 Windows 應用程式時，請記住此頁面上的必要條件。 這包括您在深入探索之前需要知道的技術。

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a>使用 DirectX 開發 Windows 遊戲應該知道什麼？

在使用 DirectX 開始開發 Windows Store 應用程式之前，您必須知道如何在 Windows 中使用 c + + 進行程式設計。 使用 DirectX 的 Windows 應用程式是以較低層級的程式設計來開發，這表示您會暴露在作業系統的許多功能上。 這些包括記憶體和資源管理，以及圖形裝置本身的介面。 如果您是遊戲或圖形應用程式開發的新手，您可能會發現這是一項挑戰。 但是您也會發現它可獲得獎勵，因為在此層級的學習遊戲開發，可為遊戲和圖形應用程式的設計與開發帶來更多的可能性。

您也必須瞭解2D 和3D 圖形程式設計和數學的基本概念，因為您將使用的許多 Api 都是以這些原則為考慮而開發。 如果您熟悉其參數和結果，您就可以更輕鬆地瞭解它們的參數和結果。

您至少應該要理解下列各項：

-   Windows C/c + + 程式設計。 這表示您瞭解指標和參考、事件和回呼，也可能是一些常見的程式庫（例如 ATL）。
-   Win32 程式設計。 您瞭解 windows 的建立方式，以及如何處理使用者介面事件。 您也會瞭解 COM 和基本 Win32 Api 的一些相關資訊。
-   線性代數和三角函數。 雖然不是必要的，但如果您熟悉這兩個數學專業領域的概念，就會有更多的時間，因為它們是許多3D 圖形程式設計的基礎。
-   基本圖形術語和概念，例如點陣圖、材質、頂點、網格和等區。

## <a name="what-does-directx-provide-me"></a>DirectX 提供的功能為何？

DirectX 是您將用來開發 Windows 遊戲的一組主要圖形 Api。 以下是當您決定如何開發遊戲時，必須熟悉的功能類別。



| 程式庫     | 描述                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D    | 一組強大、以效能為導向、硬體加速的程式庫，用於呈現3D 圖形。                                              |
| Direct2D    | 適用于硬體加速點陣圖和向量2D 繪圖的一組2D 圖形程式庫。                                                           |
| DirectXMath | 2D 和3D 圖形中所使用之常見、優化數學運算的程式庫，例如向量和矩陣作業。                                |
| DirectWrite | 2D 文字轉譯和版面配置 Api 的程式庫。 它支援硬體加速和軟體點陣化。                              |
| XAudio2     | 適用于 Microsoft Windows 的低層級跨平臺音訊 API，可為遊戲開發提供信號處理和音訊混合基礎。 |
| XInput      | 支援各種傳統遊戲控制項的程式庫，並強調 Xbox 360 控制器模型。                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a>使用 DirectX 開發 Windows 遊戲需要哪些工具？

若要開始進行本教學課程，您需要：

-   Windows 8.1 或更高
-   Microsoft Visual Studio 2013 或更高版本

 

 




