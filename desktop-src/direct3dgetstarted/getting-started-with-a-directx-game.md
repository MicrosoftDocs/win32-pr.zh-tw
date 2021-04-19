---
title: 開始使用適用于 Windows 的 DirectX
description: 建立適用于 Windows 的 Microsoft DirectX 遊戲是新開發人員的挑戰。 在這裡，我們將快速審視相關的概念，以及使用 DirectX 和 c + + 開始開發遊戲時必須採取的步驟。
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae09cd127a30401ae0493f5dd770fe1e67607b45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967905"
---
# <a name="get-started-with-directx-for-windows"></a>開始使用適用于 Windows 的 DirectX

建立適用于 Windows 的 Microsoft DirectX 遊戲是新開發人員的挑戰。 在這裡，我們將快速審視相關的概念，以及使用 DirectX 和 c + + 開始開發遊戲時必須採取的步驟。

讓我們開始這次的教學。

## <a name="what-skills-do-you-need"></a>您需要哪些技能？

若要開發適用于 Windows 的 DirectX 遊戲，您必須具備一些基本技巧。 具體來說，您必須能夠：

-   讀寫新式 c + + 程式碼 (c + + 11 提供最) 的功能，並熟悉基本的 c + + 設計原則，以及範本和 factory 模型等模式。 您也必須熟悉通用的 c + + 程式庫，例如標準樣板程式庫，並特別說明轉換運算子、指標類型和標準樣板程式庫資料結構 (例如 std：： vector) 。
-   瞭解基本幾何、三角函數和線性代數。 您在範例中發現的大部分程式碼都假設您瞭解這些形式的數學和其常見規則。
-   熟悉 COM —特別是 [**Microsoft：： WRL：： ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (smart 指標) 。
-   瞭解圖形和圖形技術的基礎，特別是3D 圖形。 雖然 DirectX 本身有自己的術語，但它仍是根據一般3D 圖形原則的完善概念來建立。
-   瞭解訊息迴圈的概念，因為您將會執行接聽 Windows 作業系統的迴圈。

## <a name="and-were-off"></a>而我們已經關閉了！

準備好開始了嗎？ 開始之前，讓我們先複習一下。 您已經：

-   Windows 8.1 的已更新且可運作的安裝。
-   [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs)的安裝。
-   我位勇敢精神以及想要深入瞭解 DirectX 遊戲開發！

## <a name="next-steps"></a>下一步



|                                                                                                    |                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [使用 DirectX 裝置資源](work-with-dxgi.md)                                           | 瞭解如何使用 DXGI 來建立虛擬化圖形裝置，以及建立和設定交換鏈。     |
| [瞭解 Direct3D 11 轉譯管線](understand-the-directx-11-2-graphics-pipeline.md) | 瞭解如何連結至 DirectX 裝置資源類別，並使用 Direct3D 圖形管線進行繪製。 |
| [使用著色器和著色器資源](work-with-shaders-and-shader-resources.md)               | 瞭解如何撰寫適用于 Direct3D 圖形管線階段的 HLSL 著色器程式。                            |



 

 

 