---
title: 用戶端建立連接的方式
description: 若要與伺服器程式建立用戶端/伺服器通訊會話，具有明確控制碼的用戶端應用程式必須建立系結控制碼。
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5fd8437fb5821c2b52240256a1938e8de31c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021565"
---
# <a name="how-the-client-establishes-a-connection"></a>用戶端建立連接的方式

若要與伺服器程式建立用戶端/伺服器通訊會話，具有明確控制碼的用戶端應用程式必須建立系結控制碼。 在這些情況下，RPC 執行時間程式庫會尋找裝載伺服器程式的電腦。 然後，它會尋找伺服器程式正在接聽的端點，並將呼叫導向該端點。 下圖說明此程序。

![rpc 用戶端建立與 rpc 伺服器的連接](images/clntcon.png)

本節會提供有關用戶端如何連接到伺服器程式，以及如何執行它所提供之遠端程式的資訊。 有許多方法可完成這些步驟;視選擇的設計而定，應用程式可能會選擇一組不同的步驟。 這個範例只是其中一種方法。

討論區分為下列各節：

-   [建立系結控制碼](creating-a-binding-handle.md)
-   [進行遠端程序呼叫](making-a-remote-procedure-call.md)
-   [尋找伺服器程式](finding-the-server-program.md)
-   [傳送呼叫給伺服器程式](sending-the-call-to-the-server-program.md)

 

 




