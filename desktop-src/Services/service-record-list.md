---
description: 由於每個服務專案都是從已安裝服務的資料庫讀取，因此 SCM 會建立服務的服務記錄。
ms.assetid: c0ee43e2-af9b-4578-9017-46a5ed50b938
title: 服務記錄清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef0bdebed5e302b1dc59bea6494fd812ec506e7e6d2531634b2a6686b86bc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888852"
---
# <a name="service-record-list"></a>服務記錄清單

由於每個服務專案都是從已安裝服務的資料庫讀取，因此 SCM 會建立服務的服務記錄。 服務記錄包含：

-   服務名稱
-   啟動類型 (自動啟動或需求-開始) 
-   服務狀態 (查看 [**服務 \_ 狀態**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) 結構)  <dl> 類型  
    目前狀態  
    可接受的控制碼  
    結束碼  
    Wait 提示  
    </dl>
-   Pointer to dependency list

安裝服務時，會指定帳戶的使用者名稱和密碼。 SCM 會將使用者名稱儲存在登錄中，並將密碼儲存在本機安全機構 (LSA) 的安全部分。 系統管理員可以建立密碼永遠不會過期的帳戶。 或者，系統管理員可以建立具有密碼的帳戶，藉由定期變更密碼來過期及管理帳戶。

SCM 會保留使用者帳戶密碼的兩個複本，也就是目前的密碼和備份密碼。 第一次安裝服務時指定的密碼會儲存為目前的密碼，且不會初始化備份密碼。 當 SCM 嘗試在使用者帳戶的安全性內容中執行服務時，會使用目前的密碼。 如果成功使用目前的密碼，也會另存為備份密碼。 如果使用 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 函式或 [服務] 控制台公用程式來修改密碼，則新密碼會儲存為目前的密碼，而先前的密碼會儲存為備份密碼。 如果 SCM 嘗試啟動服務，但目前的密碼失敗，則會使用備份密碼。 如果成功使用備份密碼，則會儲存為目前的密碼。

當服務使用 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 函數傳送狀態通知時，SCM 會更新服務狀態。 SCM 會藉由查詢 i/o 系統來維護驅動程式服務的狀態，而不是從服務收到狀態通知。

服務可以藉由呼叫 [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits) 函數來註冊其他類型資訊。 [**NetServerGetInfo**](/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo)和 [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum)函數會取得支援的服務類型。

 

 
