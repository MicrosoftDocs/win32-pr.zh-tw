---
description: 執行完整的 TCP/IP 用戶端和伺服器應用程式範例程式碼。
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: 執行 Winsock 用戶端和伺服器程式碼範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdb5a4b2385c9545410cfc29c913ea81660f6dc2810b92279fad22212781065c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132481"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a>執行 Winsock 用戶端和伺服器程式碼範例

本節包含 TCP/IP 用戶端和伺服器應用程式的完整原始碼：

-   [完成 Winsock 用戶端程式代碼](complete-client-code.md)
-   [完整的 Winsock 伺服器程式碼](complete-server-code.md)

在啟動用戶端應用程式之前，應該先啟動伺服器應用程式。

若要執行伺服器，請編譯完整的伺服器原始程式碼，然後執行可執行檔。 伺服器應用程式會接聽 TCP 通訊埠27015，讓用戶端連接。 一旦用戶端連線之後，伺服器會從用戶端接收資料，並 (傳送) 傳回給用戶端的資料。 當用戶端關閉連線時，伺服器會關閉用戶端通訊端、關閉通訊端並結束。

若要執行用戶端，請編譯完整的用戶端原始程式碼，然後執行可執行檔。 用戶端應用程式需要執行伺服器應用程式之電腦的電腦名稱稱或 IP 位址，在執行用戶端時，會以命令列參數的形式傳遞。 如果在範例電腦上執行用戶端和伺服器，用戶端就可以依照下列方式啟動：

**用戶端 localhost**

用戶端嘗試連接到 TCP 埠27015上的伺服器。 用戶端連接之後，用戶端會將資料傳送到伺服器，並接收從伺服器傳回的任何資料。 用戶端接著會關閉通訊端並結束。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> </dl>

 

 



