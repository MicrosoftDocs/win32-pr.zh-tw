---
description: 通訊端網路應用程式有兩種不同的類型：伺服器和用戶端。
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: 關於伺服器和用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a951d23ba1c6ad4f0f5ffd1f674b056a36c3f8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989914"
---
# <a name="about-servers-and-clients"></a>關於伺服器和用戶端

通訊端網路應用程式有兩種不同的類型：伺服器和用戶端。

伺服器和用戶端有不同的行為;因此，建立它們的程式不同。 接下來是建立串流 TCP/IP 伺服器和用戶端的一般模型。

## <a name="server"></a>伺服器

1.  初始化 Winsock。
2.  建立通訊端。
3.  系結通訊端。
4.  在用戶端上接聽通訊端。
5.  接受來自用戶端的連接。
6.  接收和傳送資料。
7.  中斷連線。

## <a name="client"></a>用戶端

1.  初始化 Winsock。
2.  建立通訊端。
3.  連接至伺服器。
4.  傳送和接收資料。
5.  中斷連線。

> [!Note]  
> 用戶端和伺服器的部分步驟是相同的。 這些步驟的執行方式幾乎完全相同。 本指南中的某些步驟將會特定于所建立的應用程式類型。

 

第一個步驟： [建立基本 Winsock 應用程式](creating-a-basic-winsock-application.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> </dl>

 

 



