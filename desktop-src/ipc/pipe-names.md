---
description: 每個具名管道都有唯一的名稱，可在命名物件的系統清單中區分它與其他具名管道。 當管道伺服器呼叫 CreateNamedPipe 函式來建立具名管道的一或多個實例時，會指定該管道的名稱。
ms.assetid: 8f7e717a-648b-421e-ab79-a4abbae670be
title: 管道名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e470a09fa4cfe1b2f259ca3fd5b53f79045787fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000176"
---
# <a name="pipe-names"></a>管道名稱

每個具名管道都有唯一的名稱，可區別系統的命名物件清單中的其他具名管道。 當管道伺服器呼叫 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) 函式來建立具名管道的一或多個實例時，會指定該管道的名稱。 管道用戶端會在呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 或 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 函式以連接到具名管道的實例時，指定管道名稱。

在 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)、 [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)或 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 函數中指定管道的名稱時，請使用下列格式：

\\\\*ServerName* \\管道 \\ *PipeName*

其中 *ServerName* 是遠端電腦的名稱或句號，以指定本機電腦。 *PipeName* 指定的管道名稱字串可以包含反斜線以外的任何字元，包括數位和特殊字元。 整個管道名稱字串的長度最多可達256個字元。 管道名稱不區分大小寫。

管道伺服器無法在另一部電腦上建立管道，因此 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) 必須使用句點做為伺服器名稱，如下列範例所示。

\\\\.\\管道 \\ *PipeName*

管道伺服器可以提供管道用戶端的管道名稱，讓它們可以連接到管道。 管道用戶端會從某個持續性來源（例如登錄專案、檔案或其他應用程式）探索管道名稱。 否則，用戶端必須知道編譯時期的管道名稱。

 

 
