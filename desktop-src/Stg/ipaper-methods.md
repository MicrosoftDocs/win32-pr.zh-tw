---
title: IPaper 方法
description: 提供主要由其原生 IPaper 介面控制的 COPaper 物件。
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84153c9fcec021d9084807d73d46198e3a56482
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184047"
---
# <a name="ipaper-methods"></a>IPaper 方法

**StoServe** 會提供主要由其原生 **IPaper** 介面控制的 COPaper 物件。

下表列出來自 IPAPER 的 **IPaper** 方法。在 [中] \\ inc. 目錄中的 H。



| 方法    | 描述                                                         |
|-----------|---------------------------------------------------------------------|
| InitPaper | 初始化紙張物件並建立筆墨資料陣列。                 |
| 鎖定      | 提供紙張的用戶端控制權，並鎖定其他用戶端。      |
| Unlock    | 紙張的會讓出用戶端控制。                           |
| 載入      | 從用戶端的複合檔案載入紙張內容，並通知接收。 |
| 儲存      | 將紙張內容儲存至用戶端的複合檔案。                      |
| InkStart  | 開始色彩筆墨繪圖至紙張表面。                      |
| InkDraw   | 將筆墨資料點放在電子紙張表面上。               |
| InkStop   | 停止筆墨繪圖至紙張表面。                             |
| 清除     | 清除目前的紙張內容，並通知接收。                 |
| 調整大小    | 調整繪圖紙張的矩形大小，並通知接收。        |
| 重 繪    | 重新繪製紙張物件的內容，並通知接收。                |



 

這個程式碼範例在複合檔案上的相關方法是 [**載入**](ipaper--load.md)、 [**儲存**](ipaper--save.md)和 [**重繪**](ipaper--redraw.md)。

[**InkStart**](inkstart-method.md)、 [**InkDraw**](inkdraw-method.md)和 [**InkStop**](cguipaper-methods.md) 是用戶端用來記錄筆墨繪圖順序之命令 COPaper 的方法。 用戶端通常會在 \_ COPaper 上呼叫 **InkStart** ，以回應 WM LBUTTONDOWN 訊息作為筆墨繪圖順序的開頭。 當使用者將滑鼠或畫筆移至按住左按鈕時，用戶端將會 \_ 使用對應的 **InkDraw** 呼叫來回應重複的 WM MOUSEMOVE 訊息。 當使用者放開滑鼠左鍵時，用戶端會使用 InkStop 的呼叫來回應 WM \_ LBUTTONUP 訊息，此訊息會標示筆墨繪圖順序的結尾。

[**InkStart**](inkstart-method.md) 會在用戶端視窗座標中告訴 COPaper 繪圖順序的開始位置。 它也會傳遞目前選取的筆墨色彩和寬度。 用戶端會維護這些選項;COPaper 只會在進行 **InkStart** 呼叫時記錄它們。 重複呼叫 [**InkDraw**](inkdraw-method.md) ，以指示 COPaper 連續的視窗座標，代表滑鼠或畫筆的繪製動作。 [**InkStop**](cguipaper-methods.md) 會指示 COPaper 標示繪圖順序的結尾。

 

 




