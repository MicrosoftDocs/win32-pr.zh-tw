---
description: " (API) 適用于 Tablet PC 的程式設計介面，以及 Windows SDK Windows Touch 區段的應用程式開發介面。"
ms.assetid: 4ede7d0e-e826-4b3a-8a46-0f3162c19cb0
title: 平板電腦和觸控範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8562dcc1baa42f44d6ca675344d658b1bf693cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852815"
---
# <a name="tablet-and-touch-samples"></a>平板電腦和觸控範例

本節包含的範例會示範如何使用 C \# 、Microsoft Visual Basic .net 和 c + + 來開發應用程式，以使用筆墨和觸控。

根據預設，範例安裝在 <system drive> ： \\ Program Files \\ Microsoft TABLET pc Platform sdk 範例（ \\ \\ 安裝 Tablet pc SDK 時）。

> [!Note]  
> 安裝 Windows SDK、Windows Server SDK 或 .NET Framework SDK 時，範例會安裝在該特定 SDK 的預設路徑中。

 

## <a name="available-samples"></a>可用的範例



| 範例                                                                           | 描述                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Advanced 辨識](advanced-recognition-sample.md)                          | 示範一些更先進的辨識功能，例如明確的辨識器選擇、factoids 等等。<br/>                                                                                                                                                             |
| [自動宣告表單](auto-claims-form-sample.md)                                  | 示範如何使用兩個筆墨控制項： [InkEdit](/previous-versions/ms552265(v=vs.100)) 控制項和 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項。<br/>                                                                                                        |
| [基本身份識別](basic-recognition-sample.md)                                | 示範如何使用 [RecognizerCoNtext](/previous-versions/ms828542(v=msdn.10)) 物件來建立簡單的手寫辨識應用程式。<br/>                                                                                                                     |
| [C + + 事件接收器](c---event-sinks-sample.md)                                    | 示範 c + + 中適用于所有 Tablet 平臺事件的範本，這些事件可以進行子類別化，或複製和貼上並當做範本程式碼使用。<br/>                                                                                                                                   |
| [字元自動完成](character-autocomplete-sample.md)                      | 示範如何使用辨識 Api，以日文執行字元自動完成。<br/>                                                                                                                                                                                 |
| [筆墨 Blog Web 範例](ink-blog-web-sample.md)                                   | 示範如何建立具有筆墨功能的 managed 使用者控制項，以及在 Internet Explorer 中控制的主機<br/>                                                                                                                                                         |
| [筆墨剪貼簿](ink-clipboard-sample.md)                                        | 示範使用剪貼簿的筆墨互通性。<br/>                                                                                                                                                                                                                          |
| [筆墨集合](ink-collection-sample.md)                                      | 示範使用 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件來收集筆跡的簡單 Windows form 應用程式。<br/>                                                                                                                                     |
| [筆墨分隔線](ink-divider-sample.md)                                            | 示範如何使用 [分界線](/previous-versions/ms839398(v=msdn.10)) 物件來執行筆墨分析。<br/>                                                                                                                                                                            |
| [筆跡清除](ink-erasing-sample.md)                                            | 示範如何在 Windows form 應用程式中刪除筆跡筆觸，此應用程式會使用 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件來收集筆跡。<br/>                                                                                                             |
| [筆墨點擊測試](ink-hit-test-sample.md)                                          | 示範兩種點擊測試筆墨的方式。<br/>                                                                                                                                                                                                                                       |
| [筆跡辨識](ink-recognition-sample.md)                                    | 示範如何建立簡單的手寫辨識應用程式。<br/>                                                                                                                                                                                                    |
| [筆跡序列化](ink-serialization-sample.md)                                | 示範如何將筆墨序列化為 (ISF) 的筆墨序列化格式。<br/>                                                                                                                                                                                                           |
| [筆墨 Web 控制項範例](ink-web-control-sample.md)                             | 示範如何建立可在網頁瀏覽器中使用的筆墨控制項。<br/>                                                                                                                                                                                                             |
| [筆墨縮放](ink-zoom-sample.md)                                                  | 示範如何在應用程式中適當地縮放筆墨。<br/>                                                                                                                                                                                                                        |
| [多個辨識器範例](multiple-recognizers-sample.md)                   | 示範如何從各種已安裝的辨識器中進行選取，然後使用選取的辨識器。<br/>                                                                                                                                                                        |
| [無觸控部署 Web 範例](no-touch-deployment-web-sample.md)             | 示範如何使用 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件，讓文字輸入至您的表單應用程式更簡單。 擴充自動宣告表單範例。<br/>                                                                                      |
| [PenInputPanel](peninputpanel-sample.md)                                        | 示範如何使用 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件，讓文字輸入至您的表單應用程式更簡單。 擴充自動宣告表單範例。<br/>                                                                                      |
| [RealTimeStylus 筆墨集合範例](realtimestylus-ink-collection-sample.md) | 示範使用 RealTimeStylus 的筆墨收集。<br/>                                                                                                                                                                                                                           |
| [RealTimeStylus 外掛程式範例](realtimestylus-plug-in-sample.md)               | 示範如何使用 RealTimeStylus。<br/>                                                                                                                                                                                                                                       |
| [掃描的紙張表單範例](scanned-paper-form-sample.md)                       | 示範如何使用以點陣圖形式掃描的表單，並將其指定為表單頂端 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項的背景影像。 已針對筆墨集合啟用數個區域 (或指定為 "inkable" ) 。<br/> |
| [Tablet PC 平臺資訊範例](tablet-pc-platform-info-sample.md)             | 示範如何使用 GetSystemMetrics () Windows API 函數，判斷應用程式是否在 Tablet PC 上執行。<br/>                                                                                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[辨識器 DLL 範例範本](recognizer-dll-sample-template.md)
</dt> </dl>

 

