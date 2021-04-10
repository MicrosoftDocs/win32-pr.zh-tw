---
description: 網路監視器 SDK 包含建立專家所需的函式和範例程式碼。 不過，您也可以使用現有的工具，包括對話方塊編輯器。
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: 設計專家
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115345"
---
# <a name="programming-an-expert"></a>設計專家

網路監視器 SDK 包含建立專家所需的函式和範例程式碼。 不過，您也可以使用現有的工具，包括對話方塊編輯器。

## <a name="minimum-requirements-to-run-an-expert"></a>執行專家的最低需求

下表列出您必須用來建立專家的 DLL 進入點和專家功能。



| 名稱                                                 | 類型               | 必要項？                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [**DllMain**](dllmain-expert.md)                    | DLL 輸入函式 | Yes                                             |
| [**註冊專家**](register-expert.md)           | DLL 輸入函式 | Yes                                             |
| [**執行**](run.md)                                   | DLL 輸入函式 | Yes                                             |
| [**設定**](configure.md)                       | DLL 輸入函式 | 只有當專家提供使用者設定。 |
| [**ExpertIndicateStatus**](expertindicatestatus.md) | 專家功能    | Yes                                             |
| [**ExpertSubmitEvent**](expertsubmitevent.md)       | 專家功能    | Yes                                             |



 

請參閱網路監視器 SDK 中的專家和剖析器參考主題，以更新您的原始程式碼，然後使用這些主題中提供的範例程式碼和程式：

-   [打造專家](building-an-expert.md)
-   [安裝專家](installing-an-expert-to-network-monitor-2-1.md)
-   [錯專家](debugging-an-expert.md)

因為函式是透過使用覆迭的函式指標來呼叫，所以專家 Dll 需要 C，而不是 c + + 的呼叫慣例。 透過一組專門的專家功能，專家可以存取 capture 中的框架。 專家可以使用大部分的網路監視器 API 來操作傳回的資料。 當專家找到要傳送給使用者的資訊時，它會封裝事件資料結構中的資訊，並將其提交給網路監視器，然後在專家輸出視窗中顯示資訊。 專家必須定期更新網路監視器，其中包含 [**ExpertIndicateStatus**](expertindicatestatus.md) 函式所提供的百分比-完成狀態資訊。

專家匯出的函式的呼叫如下：

-   當網路監視器正在建立要提供給使用者的專家清單時，網路監視器會呼叫 [**註冊專家**](register-expert.md) 功能。
-   **註冊註冊** 之後，如果專家可以設定，網路監視器會呼叫 [**Configure**](configure.md)函數。
-   當網路監視器使用者按一下 [ **執行專家**] 時，網路監視器會呼叫 [**run**](run.md) 函數。

當專家分析要求的畫面並找出問題時，他們會使用 [**ExpertSubmitEvent**](expertsubmitevent.md) 來提交包含問題相關資訊的事件。 網路監視器會將事件發佈至標準 (共用) 事件檢視器或 (如果專家註冊) 至私用事件檢視器。

 

 



