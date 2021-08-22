---
title: 開發人員總覽
description: 開發人員總覽
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Windows Media Player 外掛程式、視覺效果
- 外掛程式，視覺效果
- 視覺效果，開發人員總覽
- 自訂視覺效果，開發人員總覽
- 視覺效果、COM 控制項
- 自訂視覺效果，COM 控制項
- 視覺效果，音訊輸入
- 自訂視覺效果，音訊輸入
- 視覺效果，圖形化輸出
- 自訂視覺效果，圖形化輸出
- 視覺效果，繪圖工具
- 自訂視覺效果，繪圖工具
- 視覺效果，程式設計語言
- 自訂視覺效果，程式設計語言
- 視覺效果，Visual C++
- 自訂視覺效果，Visual C++
- 視覺效果，外掛程式 wizard
- 自訂視覺效果，外掛程式嚮導
- 外掛程式嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20988a8cf1b7923699ec9cee7990b99840b8acdf9371e74da5940ddb8fc8d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579410"
---
# <a name="developer-overview"></a>開發人員總覽

從開發人員的觀點來看，視覺效果是可取得 Windows Media Player 所提供之音訊資料的軟體程式，並將該資料轉換為可讓使用者注意的圖形。 開發人員必須瞭解才能建立新視覺效果的主要主題如下：

## <a name="visualization-packaging"></a>視覺效果封裝

視覺效果是 Windows Media Player 用來在 Microsoft Windows 中將音訊波形轉換成動畫圖形的 COM 控制項。 COM 控制項會封裝成 Microsoft Windows 動態連結程式庫 (dll) 且必須在 Windows 登錄中註冊。 當 Windows Media Player 執行時，系統會根據 Windows Media Player 正在使用的面板指示載入和查看已註冊的自訂視覺效果。

## <a name="audio-input"></a>音訊輸入

Windows Media Player 會在以秒為單位的時間間隔內，將音訊頻率和波形資料的快照集提供給您的程式碼。 快照間隔是由 Windows Media Player 在內部決定。

## <a name="graphical-output"></a>圖形化輸出

視覺效果的圖形輸出是 Microsoft Windows 裝置內容。 這是標準 Windows 繪圖介面，可讓您在每次提供音訊快照集時繪製。 所有背景 Windows 技術都是由您負責。 您只需要使用所提供的音訊資料來繪製裝置內容。

## <a name="drawing-tools"></a>繪圖工具

您可以使用標準的 Microsoft Windows 圖形裝置介面 (GDI) 函式來繪製裝置內容，並使用畫筆和筆刷來建立以 Windows Media Player 提供給您的音訊資料修改的設計。 GDI 提供一組豐富的繪圖工具，可建立許多種類的視覺效果。

## <a name="programming-language"></a>程式設計語言

Microsoft Visual C++ 6.0 和更新版本是用來建立自訂視覺效果的唯一支援語言。

## <a name="plug-in-wizard"></a>外掛程式嚮導

Windows Media Player 提供可讓您新增至 Visual C++ 的 COM wizard，以產生視覺效果所需的基礎程式碼。 不僅提供所有原始程式檔，還會產生範例面板，讓您輕鬆地測試視覺效果。 產生的程式碼會建立類似于橫條的視覺效果，並提供兩個預設值。 然後您可以修改程式碼，以建立您自己的視覺效果。 也會產生登錄檔案來註冊您的視覺效果，讓 Windows Media Player 可以載入它。

下列主題說明視覺效果程式碼處理音訊資料的方式：

-   [控制項 Flow](flow-of-control.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於自訂視覺效果**](about-custom-visualizations.md)
</dt> </dl>

 

 




