---
title: RPC-Message 佇列應用程式的系統需求
description: 若要在 RPC 用戶端/伺服器應用程式中使用訊息佇列傳輸，伺服器和用戶端電腦必須安裝適當的作業系統平臺和訊息佇列軟體。
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1274c888506a6868eb7ded5ba96c5f1ea8dc8b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382490"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a>RPC-Message 佇列應用程式的系統需求

若要在 RPC 用戶端/伺服器應用程式中使用訊息佇列傳輸，伺服器和用戶端電腦必須安裝適當的作業系統平臺和訊息佇列軟體。

伺服器電腦的需求如下：

-   Microsoft Windows Server 2003、Windows XP 或 Windows 2000 或更新版本。
-   SQL Server 6.5 版或更新版本。
-   訊息佇列主要企業控制器或主要網站控制器。
-   RPC 伺服器端傳輸 DLL (RpcMqSvr.dll) 。

用戶端電腦的需求如下：

-   Microsoft Windows Server 2003、Windows XP 或 Windows 2000 或更新版本。
-   Microsoft Message Queuing 用戶端。
-   RPC 用戶端傳輸 DLL (RpcMqCl.dll) 。

當 MSMQ 元件安裝在用戶端和伺服器電腦上時，系統登錄會自動設定為包含遠端程序呼叫的 [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq) 訊息佇列傳輸通訊協定。

若要建立您的 RPC MSMQ 應用程式，您需要下列各項：

-   Microsoft Windows Server 2003、Windows XP 或 Windows 2000 或更新版本
-   MIDL 版本3.1.76 或更新版本。

 

 