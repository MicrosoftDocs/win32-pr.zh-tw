---
description: 服務控制管理員 (SCM) 會在系統開機時啟動。 這是 (RPC) server 的遠端程序呼叫，因此服務設定和服務控制程式都可以操作遠端電腦上的服務。
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: 服務控制管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37d651a96f9685fa82b5ea92ebb3a0b72d80bfc62cd0db80729ec1cb95acc45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889031"
---
# <a name="service-control-manager"></a>服務控制管理員

服務控制管理員 (SCM) 會在系統開機時啟動。 這是 (RPC) server 的遠端程序呼叫，因此服務設定和服務控制程式都可以操作遠端電腦上的服務。

服務函式會為 SCM 所執行的下列工作提供介面：

-   維護已安裝服務的資料庫。
-   在系統啟動時或依需求啟動服務和驅動程式服務。
-   列舉已安裝的服務和驅動程式服務。
-   維護執行中服務和驅動程式服務的狀態資訊。
-   將控制要求傳送至執行中的服務。
-   鎖定和解除鎖定服務資料庫。

下列各節將更詳細地說明 SCM：

-   [已安裝服務的資料庫](database-of-installed-services.md)
-   [自動啟動服務](automatically-starting-services.md)
-   [依需求啟動服務](starting-services-on-demand.md)
-   [服務記錄清單](service-record-list.md)
-   [SCM 控制碼](scm-handles.md)

 

 



