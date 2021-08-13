---
description: 這個範例示範如何使用筆墨分析來建立表單填滿應用程式，其中的表單是以掃描的紙張表單為基礎。
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: 筆跡分析掃描的紙張表單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4069efd5ba8763e00e9b3170ffb0a39a4a70c4d66d07d3c8bf08bc3688f57ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718644"
---
# <a name="ink-analysis-scanned-paper-form"></a>筆跡分析掃描的紙張表單

這個範例示範如何使用筆墨分析來建立表單填滿應用程式，其中的表單是以掃描的紙張表單為基礎。

## <a name="features-demonstrated"></a>示範的功能

這個範例應用程式示範筆墨分析 API 的下列功能，以及 Windows Forms 筆墨控制項：

-   正在載入掃描的紙張表單。 此範例會從影像匯入 .png 格式的表單。
-   在掃描的表單上方收集和轉譯筆墨。
-   使用 [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) 物件來剖析手寫。
-   產生 [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) 物件以改善手寫結果。
-   從分析提示填入文字方塊。
-   建立基本文字修正體驗。

## <a name="project-references"></a>專案參考

此範例可作為 Windows Forms 或 Windows Presentation Foundation 應用程式。 Windows Forms 版本參考：

-   Microsoft.Ink.dll
-   Microsoft.Ink.Analysis.dll

除了核心 Windows Presentation Foundation dll 之外，Windows Presentation Foundation 版本參考 IAWinFX.dll。

> [!Note]  
> 此範例的 Windows Presentation Foundation 版本 (可在 XAML 目錄中找到) 必須在系統上安裝 Microsoft Visual Studio 2005 的 Windows Presentation Foundation 延伸模組。

 

## <a name="user-interface"></a>使用者介面

此應用程式的 UI 是由具有兩個相關聯之[TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1)物件的[TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1)所組成：筆墨表單和轉換的文字形式。 [筆跡表單] 索引標籤包含

-   面板，其中包含用來取得電話郵件的掃描紙張表單影像。
-   當選取時，具有應用程式的核取方塊會顯示分析提示界限。
-   一組按鈕、清除和分析，會從表單中清除筆墨，並將筆墨分析初始化。

轉換過的文字形式包含相同的影像，而是應用程式顯示已辨識文字的頁面。 當您按一下 [分析] 時，應用程式會以同步方式執行筆墨分析，而辨識結果會出現在 [已轉換的文字格式] 索引標籤上

## <a name="functionality"></a>功能

此應用程式會使用 [InkOverlay](/previous-versions/ms552322(v=vs.100)) 來啟用寫入。 InkOverlay 物件非常適合用於拍攝和基本 scribbling。 這個物件的主要用途是將筆墨顯示為筆跡。 筆跡分析的主要類別是 [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) 類別。 當您呼叫 InkAnalyzer 物件的 [分析](/previous-versions/ms568971(v=vs.100)) 方法時，筆墨分析會以同步方式進行。

應用程式會初始化兩個數組，一個字串和一個矩形。 字串陣列 `factoidStrings` 是由以[AnalysisHintNode](/previous-versions/ms573018(v=vs.100))物件的形式傳遞至[InkAnalyzer](/previous-versions/ms583671(v=vs.100))中的[智慧](/previous-versions/ms583657(v=vs.100))標記物件所組成。 AnalysisHintNode 物件會針對特定輸入偏差 InkAnalyzer。 此範例會使用日期、時間和電話提示，以及其他部分。

每個 [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) 都與表單的特定區域相關聯。 這些區域會以矩形的陣列表示 `rects` 。 藉由為每個矩形建立 [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) ，此範例會將已辨識的文字輸出到正確的位置。


```C++
        private void InitHints()
        {
            // Instantiate the collection of TextBoxes.
            this.textBoxes = new ArrayList();

            // For each Rectangle in Rectangles
            for (int i = 0; i < rects.Length; i++)
            {

                Rectangle rectangle = rects[i];

                // Create an AnalysisHintNode with the bounds of the Rectangle.  The bounds
                // of an AnalysisHintNode gives clues to the handwriting recognizer about
                // the way Strokes are grouped together.
                AnalysisHintNode hint = this.analyzer.CreateAnalysisHint(rectangle);

                // Set the corresponding Factoid on the AnalysisHintNode.  This gives the 
                // recognizer clues about the meaning of the strokes within the 
                // AnalysisHintNode's region.
                hint.Factoid = factoidStrings[i];

                // Create a corresponding TextBox where the results of the analysis
                // associated with this AnalysisHintNode will be displayed.  Store the reference
                // to the TextBox in the textBoxes Collection.
                this.textBoxes.Add(InitTextBox(hint));
            }
        }
```



之後，只要建立事件處理常式，在使用者按一下 [分析] 時，就會觸發筆墨分析。


```C++
        private void UpdateTextBoxes()
        {
            // Get the AnalysisHintNodes that we previously added to the InkAnalyzer.
            ContextNodeCollection hints = this.analyzer.GetAnalysisHints();

            for (int i = 0; i < hints.Count; i++)
            {
                // Get the recognized string from the AnalysisHintNode
                string analyzedString = ((AnalysisHintNode)hints[i]).GetRecognizedString();

                // If we found a string, set the contents of the TextBox
                // to that string.
                if (analyzedString != null)
                {
                    ((TextBox)this.textBoxes[i]).Text = analyzedString;
                }
            }
        }
```



 

 
