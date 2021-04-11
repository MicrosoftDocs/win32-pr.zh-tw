---
description: 服務控制管理員 (SCM) 維護已安裝之服務和驅動程式服務的資料庫，並提供統一且安全的方式來控制它們。
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: 關於服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87aeec6dfcdc4e2dc0cc0ab3ef084b7927b2c3bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944613"
---
# <a name="about-services"></a>關於服務

[服務控制管理員](service-control-manager.md) (SCM) 維護已安裝之服務和驅動程式服務的資料庫，並提供統一且安全的方式來控制它們。 資料庫包含每個服務或驅動程式服務應如何啟動的資訊。 它也可讓系統管理員自訂每個服務的安全性需求，進而控制服務的存取。

下列類型的程式會使用 SCM 提供的函式。



| 類型                          | Description                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 服務方案               | 為一或多個服務提供可執行程式碼的程式。 服務程式會使用連接至 SCM 的函式，並將狀態資訊傳送至 SCM。                                                                                                                                                                          |
| 服務設定計劃 | 查詢或修改服務資料庫的程式。 服務設定程式使用的函式會開啟資料庫、安裝或刪除資料庫中的服務，以及查詢或修改已安裝服務的設定和安全性參數。 服務設定程式會同時管理服務和驅動程式服務。 |
| 服務控制程式       | 啟動及控制服務和驅動程式服務的程式。 服務控制程式會使用將要求傳送至 SCM 的函式，這會執行要求。                                                                                                                                                                     |



 

本總覽將討論下列主題：

-   [服務控制管理員](service-control-manager.md)
-   [服務程式](service-programs.md)
-   [服務設定程式](service-configuration-programs.md)
-   [服務控制程式](service-control-programs.md)
-   [服務使用者帳戶](service-user-accounts.md)
-   [互動式服務](interactive-services.md)
-   [服務安全性與存取權限](service-security-and-access-rights.md)
-   [對服務進行偵錯](debugging-a-service.md)
-   [服務觸發程式事件](service-trigger-events.md)

 

 



