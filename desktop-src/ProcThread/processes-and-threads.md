---
description: 執行多工處理、排程優先順序，以及處理處理常式、執行緒、執行緒集區、工作物件和纖維。 使用使用者模式排程來排程執行緒。
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: 處理序和執行緒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482f9f394001503350d4e213bd51e441ea43d073aacd8d10a49512e04404ba17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081308"
---
# <a name="processes-and-threads"></a>處理序和執行緒

應用程式是由一或多個進程所組成。 以最簡單的程式 *來說，程式* 是執行中的程式。 一或多個執行緒會在進程的內容中執行。 *執行緒* 是作業系統配置處理器時間的基本單位。 執行緒可以執行程式碼的任何部分，包括目前正在由另一個執行緒執行的元件。

*工作物件* 允許將進程群組作為一個單位來管理。 工作物件是 namable、安全實體、可共用的物件，可控制與其相關聯之進程的屬性。 在工作物件上執行的作業會影響與工作物件相關聯的所有進程。

*執行緒* 集區是工作者執行緒的集合，可代表應用程式有效率地執行非同步回呼。 執行緒集區主要是用來減少應用程式執行緒的數目，並提供工作者執行緒的管理。

*光纖* 是必須由應用程式手動排程的執行單位。 在排程執行緒的執行緒內容中執行纖程。

*使用者模式排程* (UMS) 是一種輕量的機制，可讓應用程式用來排程自己的執行緒。 UMS 執行緒與 [纖維](fibers.md) 不同之處在于，每個 ums 執行緒都有自己的執行緒內容，而不是共用單一執行緒的執行緒內容。

-   [進程和執行緒的新功能](what-s-new-in-processes-and-threads.md)
-   [關於處理序和執行緒](about-processes-and-threads.md)
-   [使用進程和執行緒](using-processes-and-threads.md)
-   [進程和執行緒參考](process-and-thread-reference.md)

 

 



