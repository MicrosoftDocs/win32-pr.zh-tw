---
description: 除了處理虛擬封鎖的函式以外，windows 通訊端2繼續支援所有的 Windows 通訊端1.1 語義和函式呼叫。
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Windows 通訊端相容性問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191733"
---
# <a name="windows-sockets-compatibility-issues"></a>Windows 通訊端相容性問題

除了處理虛擬封鎖的函式以外，windows 通訊端2繼續支援所有的 Windows 通訊端1.1 語義和函式呼叫。 由於 Windows 通訊端2只會在32位、事先排程的環境中執行，因此不需要執行 Windows 通訊端1.1 中所找到的虛擬封鎖。 這表示將永遠不會指出 WSAEINPROGRESS 錯誤碼，且 Windows 通訊端2應用程式無法使用下列 Windows 通訊端1.1 功能：

-   WSACancelBlockingCall
-   WSAIsBlocking
-   WSASetBlockingHook
-   WSAUnhookBlockingHook

為了利用虛擬封鎖而撰寫的 Windows 通訊端1.1 程式，將會繼續正常運作，因為它們會連結到 Winsock.dll 或 Wsock32.dll。 這兩種功能都能繼續支援一組完整的 Windows 通訊端1.1 函式。 為了讓程式成為 Windows 通訊端2應用程式，必須進行一些修改程式碼。 在大部分的情況下，可以使用執行緒的明智用法來容納使用封鎖攔截函式完成的處理。

 

 



