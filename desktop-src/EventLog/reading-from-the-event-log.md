---
description: 事件檢視器應用程式會使用 OpenEventLog 函數來開啟事件來源的事件記錄檔。
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: 從事件記錄檔讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d0756ba7d9609bca285ce33d69738984badf7effff8867fc5c3e1943b09145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151531"
---
# <a name="reading-from-the-event-log"></a>從事件記錄檔讀取

事件檢視器應用程式會使用 [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) 函數來開啟事件來源的事件記錄檔。 然後，事件檢視器可以使用 [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) 函式來讀取記錄檔中的事件記錄。 **ReadEventLog** 會傳回包含 [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) 結構的緩衝區，以及描述所記錄事件的其他資訊。 下圖說明此程序。

![從事件記錄檔讀取](images/readlog.png)

如需範例程式碼，請參閱 [查詢事件資訊](querying-for-event-source-messages.md)。

 

 



