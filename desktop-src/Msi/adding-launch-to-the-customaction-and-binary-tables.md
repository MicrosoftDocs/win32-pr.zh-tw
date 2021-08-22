---
description: 將記錄加入至 CustomAction 資料表，以啟動自訂動作。
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: 將啟動新增至 CustomAction 和二進位資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b362259f2ee336a540f396dc05f7745cbc3fde8fb44b8a1c06dabbd6247ba05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145961"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a>將啟動新增至 CustomAction 和二進位資料表

將記錄加入至 [CustomAction 資料表](customaction-table.md) ，以啟動自訂動作。 在 [CustomAction] 資料表的 [動作] 資料行中，輸入自訂動作的名稱。 在 [自訂動作] 資料表的 [類型] 資料行中，輸入啟動65的總計數數值型別。 CustomAction 資料表的 [來源資料行] 會在包含 DLL 之二進位資料的 [二進位資料表](binary-table.md) 記錄中指定索引鍵。 在 CustomAction 資料表的 [來源資料行] 中輸入 Tutorial.dll。 CustomAction 資料表的 [目標] 欄位中指定的進入點必須符合從 DLL 匯出的專案點。 在 CustomAction 資料表的目標資料行中輸入 LaunchTutorial。

[CustomAction 資料表](customaction-table.md)



| 動作 | 類型 | 來源       | 目標         |
|--------|------|--------------|----------------|
| 啟動 | 65   | Tutorial.dll | LaunchTutorial |



 

將您在教學課程中建立的 Tutorial.dll，加入至二進位資料表的二進位資料流程。

[二進位資料表](binary-table.md)



| 名稱         | 資料                          |
|--------------|-------------------------------|
| Tutorial.dll | {*為 DLL 新增的二進位資料*} |



 

繼續在 [安裝結束時新增控制項事件，以執行啟動](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)。

 

 



