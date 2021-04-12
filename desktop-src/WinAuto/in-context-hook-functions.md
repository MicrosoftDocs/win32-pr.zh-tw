---
title: In-Context 攔截函式
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 深入瞭解： In-Context 攔截函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe25bd64234cfbfd92f054565aa7c675328b435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195237"
---
# <a name="in-context-hook-functions"></a>In-Context 攔截函式

下列清單概述內容攔截函式的主要層面：

-   內容內攔截函式必須位於動態連結程式庫 (DLL) ，系統會將該程式庫對應到伺服器的位址空間中。
-   內容中攔截函式與伺服器共用位址空間。
-   當伺服器觸發事件時，系統會呼叫攔截函式，而不需要封送處理 (封裝和傳送跨進程界限) 的介面參數。
-   內容攔截函式通常非常快速，而且會以同步的方式接收事件通知，因為沒有封送處理。
-   某些事件可以跨進程傳遞，即使您要求使用 NEW-WINEVENT INCONTEXT 旗標) 來傳遞同進程 (也是一樣 \_ 。 您可能會看到與64位和32位應用程式互通性問題以及 Windows 主控台事件有關的這種情況。

 

 




