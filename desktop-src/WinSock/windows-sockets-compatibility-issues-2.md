---
description: Windows除了處理虛擬封鎖的函式以外，通訊端2繼續支援所有 Windows 通訊端1.1 語義和函式呼叫。
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Windows通訊端相容性問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3fa7aba32ed74f04b04d717e0b2897dc92e0c78079d2a8c20e2c3bcdd85191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051466"
---
# <a name="windows-sockets-compatibility-issues"></a>Windows通訊端相容性問題

Windows除了處理虛擬封鎖的函式以外，通訊端2繼續支援所有 Windows 通訊端1.1 語義和函式呼叫。 由於 Windows 通訊端2只會在32位、事先排程的環境中執行，因此不需要執行 Windows 通訊端1.1 中的虛擬封鎖。 這表示將永遠不會指出 WSAEINPROGRESS 錯誤碼，而且 Windows 通訊端2應用程式無法使用下列 Windows 通訊端1.1 函式：

-   WSACancelBlockingCall
-   WSAIsBlocking
-   WSASetBlockingHook
-   WSAUnhookBlockingHook

Windows為了利用虛擬封鎖而撰寫的通訊端1.1 程式，將會繼續正常運作，因為它們會連結到 Winsock.dll 或 Wsock32.dll。 這兩個功能都能繼續支援一組完整的 Windows 通訊端1.1 函式。 為了讓程式成為 Windows 通訊端2應用程式，必須進行一些修改程式碼。 在大部分的情況下，可以使用執行緒的明智用法來容納使用封鎖攔截函式完成的處理。

 

 



