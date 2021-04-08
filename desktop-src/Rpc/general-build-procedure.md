---
title: 一般組建程式
description: 使用遠端程序呼叫建立用戶端/伺服器應用程式之進程的流覽頁面 (RPC) 。
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b223bf7482cd7cbb65f5b737c90502a6b6dd3de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021323"
---
# <a name="general-build-procedure"></a>一般組建程式

使用 Microsoft RPC 建立用戶端/伺服器應用程式的程式如下：

-   開發介面。
-   開發執行介面的伺服器。
-   開發使用介面的用戶端。

下圖說明這些步驟。

![使用 microsoft rpc 建立用戶端-伺服器應用程式的流程](images/appdev.png)

同時開發用戶端和伺服器應用程式是可行的。 不過，由於用戶端和伺服器程式都相依于介面，因此必須在開發用戶端和伺服器之前開發它們之間的介面，如上圖所示。

本節討論使用 RPC 建立用戶端/伺服器應用程式所需的步驟。 下列主題將提供此資訊：

-   [開發介面](developing-the-interface.md)
-   [開發伺服器](developing-the-server.md)
-   [開發用戶端](developing-the-client.md)

 

 




