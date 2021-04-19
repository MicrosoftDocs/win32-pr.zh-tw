---
title: 使用工作排程器
description: 本節包含的程式碼範例說明如何使用工作排程器 API，以及示範如何在工作排程器架構中定義工作的 XML 範例。
ms.assetid: 6346cbd3-b584-47b4-8313-7830f7fd77b3
keywords:
- 觸發程式工作排程器、範例
- 啟動工作工作排程器
- 建立工作工作排程器
- 工作排程器工作排程器，使用
- 工作排程器範例工作排程器
- 工作排程器工作排程器範例，請參閱工作排程器範例工作排程器
- 範例工作排程器請參閱工作排程器範例工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f81dda9551917b8f6345248a316bd5941de53f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965964"
---
# <a name="using-the-task-scheduler"></a>使用工作排程器

本節包含的程式碼範例說明如何使用工作排程器 API，以及示範如何在工作排程器架構中定義工作的 XML 範例。 大部分的範例都是獨立程式碼，可以獨立執行，或貼入較大的應用程式，並修改為應用程式的需求。

下表列出本節中包含工作排程器2.0 範例。



| 範例                                                                                                    | 描述                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [在特定時間啟動可執行檔](starting-an-executable-at-a-spcific-time.md)                  | 定義在指定的時間啟動 [記事本] 的工作。                                |
| [每天啟動可執行檔](starting-an-executable-daily.md)                                           | 定義每天啟動「記事本」的工作。                                              |
| [在系統開機時啟動可執行檔](starting-an-executable-on-system-boot.md)                         | 定義啟動系統時啟動「記事本」的工作。                          |
| [每週啟動可執行檔](starting-an-executable-weekly.md)                                         | 定義每週啟動「記事本」的工作。                                  |
| [在工作註冊時啟動可執行檔](starting-an-executable-when-a-task-is-registered.md)   | 定義工作在註冊時啟動 [記事本]。                        |
| [當使用者登入時啟動可執行檔](starting-an-executable-when-a-user-logs-on.md)               | 定義在使用者登入時啟動「記事本」的工作。                                |
| [列舉工作和顯示工作資訊](enumerating-tasks-and-displaying-task-information.md) | 列舉本機電腦上的所有工作，並顯示每個工作的狀態。 |



 

下表列出本節中包含工作排程器1.0 範例。 

| 範例                                                                                    | 描述                                                                                   |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [使用 NewWorkItem 範例建立工作](creating-a-task-using-newworkitem-example.md) | 建立新的工作。                                                                           |
| [列舉工作範例](enumerating-tasks-example.md)                                 | 列舉本機電腦上的所有工作。                                               |
| [啟動工作範例](starting-a-task-example.md)                                     | 啟動已知的工作。                                                                          |
| [使用屬性頁編輯工作專案](editing-a-work-item-using-property-pages.md)   | 顯示要編輯之工作的屬性頁。                                            |
| [正在抓取工作專案屬性範例](retrieving-work-item-property-examples.md)       | 一組範例，示範如何取得套用至所有工作專案類型的屬性。 |
| [設定工作專案屬性範例](setting-work-item-property-examples.md)             | 一組範例，示範如何設定套用至所有工作專案類型的屬性。      |
| [正在抓取工作屬性範例](retrieving-task-property-examples.md)                 | 一組範例，示範如何抓取工作的唯一屬性。                       |
| [設定工作屬性範例](setting-task-property-examples.md)                       | 一組範例，示範如何設定工作的唯一屬性。                            |
| [正在抓取工作頁面範例](retrieving-a-task-page-example.md)                       | 捕獲並顯示已知工作的一般工作頁面。                                 |
| [建立新的觸發程式](creating-a-new-trigger.md)                                       | 為已知的工作建立新的觸發程式。                                                       |
| [建立閒置觸發程式範例](creating-an-idle-trigger-example.md)                   | 為已知的工作建立以事件為基礎的閒置觸發程式。                                         |
| [終止工作範例](terminating-a-task-example.md)                               | 當工作正在執行時終止。                                                        |
| [正在抓取觸發字串範例](retrieving-trigger-strings-example.md)               | 抓取與已知工作相關聯之所有觸發程式的觸發程式字串。                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[關於工作排程器](about-the-task-scheduler.md)
</dt> </dl>

 

 




