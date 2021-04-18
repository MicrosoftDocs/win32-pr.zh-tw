---
title: 建立並執行 StoServe 範例
description: 您必須先編譯用戶端範例和其他相關的範例，才能執行用戶端。
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965785"
---
# <a name="create-and-run-stoserve-sample"></a>建立並執行 StoServe 範例

您必須先編譯用戶端範例和其他相關的範例，才能執行用戶端。 如需建立範例的詳細資訊，請參閱 [如何建立範例](how-to-build-samples.md)。 如果您已經建立適當的範例，STOCLIEN.EXE 是執行 **StoServe** 範例的用戶端可執行檔。

## <a name="code-tour"></a>程式碼導覽

下表列出與 **StoServe** 範例相關的檔案。



| 檔案        | Description                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| STOSERVE.TXT | 簡短範例描述                                                                                                  |
| 生成     | 用來建立本課程 STOSERVE.DLL 程式碼範例的一般 makefile。                                            |
| STOSERVE.H   | 在 STOSERVE.DLL 中宣告為已匯入或定義為已匯出服務函數的 include 檔。                 |
| STOSERVE.Cpp | STOSERVE.DLL 的主要執行檔。 具有 DllMain 和 COM 伺服器函數 (例如，DllGetClassObject) 。 |
| STOSERVE.Def | 模組定義檔。 匯出伺服器架函數。                                                             |
| STOSERVE.鋼筋混凝土  | 可執行檔的 DLL 資源定義檔。                                                                      |
| STOSERVE..ICO | 可執行檔的圖示資源。                                                                                     |
| 伺服器。H     | 伺服器控制項 c + + 物件的 include 檔。                                                                       |
| 伺服器。Cpp   | 伺服器控制項 c + + 物件的執行檔。                                                                |
| 廠。H    | 伺服器的 class factory COM 物件的 include 檔。                                                              |
| 廠。Cpp  | 伺服器的 class factory 的執行檔。                                                                 |
| 連接。H    | 連接點列舉值、連接點和連接列舉值類別的 include 檔。                |
| 連接。Cpp  | 連接點列舉值、連接點和連接列舉值物件的執行檔。         |
| 紙。H      | COPaper COM 物件類別的 include 檔。                                                                        |
| 紙。Cpp    | COPaper COM 物件類別和連接點的實檔案。                                       |
| STOSERVE.Dsp | Microsoft Visual Studio 專案檔。                                                                                     |



 

本程式碼教學課程中涵蓋的主要主題如下：

-   [**IPaper**](ipaper-methods.md)介面方法。
-   COPaper 使用 [**IPaperSink**](ipapersink-methods.md) 介面來進行用戶端通知。
-   StoServe 中的 [**結構**](structures---stoserve.md)。
-   [Unicode 考慮事項](unicode-considerations.md)。

 

 




