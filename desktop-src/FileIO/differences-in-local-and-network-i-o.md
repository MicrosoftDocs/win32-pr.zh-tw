---
description: Windows 上的本機 i/o 和網路 i/o 之間的差異。
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: 本機和網路 i/o 的差異
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987600"
---
# <a name="differences-in-local-and-network-io"></a>本機和網路 i/o 的差異

在 Windows 上的本機 i/o 和網路 i/o 之間有一些顯著的差異：

-   網路 i/o 支援取決於重新導向程式和網路通訊協定。
-   網路 i/o 效能取決於正在進行的網路 i/o 作業數目，以及網路連線的速度。 您的應用程式必須能夠處理可能比本機電腦更快或更慢的伺服器的網路 i/o 作業，以及網路容量的暫時性變更。 在這些情況下，您的應用程式可能需要等待更多時間才能完成作業。
-   您用來執行本機檔案 i/o 的函式在網路上可能會有不同的行為。 例如，需要很長時間才能完成的網路 i/o 作業可能會超時。在某些情況下，檔案控制代碼可能會無限期地保持開啟狀態。 另一個範例是，函式可能會傳回錯誤碼，讓您的應用程式能夠處理網路 i/o 特定的程式碼。

 

 



