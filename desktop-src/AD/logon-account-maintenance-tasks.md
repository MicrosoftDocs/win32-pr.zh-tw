---
title: 登入帳戶維護工作
description: 本主題說明與登入帳戶維護工作相關的問題。
ms.assetid: 528be433-58ef-400b-ba9a-d114f3f94ec6
ms.tgt_platform: multiple
keywords:
- 登入帳戶維護工作 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0f11f69d9a974fd666871833029eda0e059329
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104374925"
---
# <a name="logon-account-maintenance-tasks"></a>登入帳戶維護工作

本主題說明與登入帳戶維護工作相關的問題。

有兩個主要問題涉及登入帳戶維護工作：

-   更新在使用者帳戶下執行之服務實例的帳戶密碼。 如需詳細資訊，請參閱 [變更服務之使用者帳戶的密碼](changing-the-password-on-a-serviceampaposs-user-account.md)。
-   處理服務實例之登入帳戶的變更。

後者是很罕見的情況，但可能發生。 系統提供 [電腦管理] 系統管理工具，可讓您變更服務登入帳戶。 此外，其他應用程式也可以使用 [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) 函數，為已安裝的服務指定新的登入帳戶。 依預設，需要本機系統管理員許可權才能變更服務帳戶。 如果發生這種情況，可能會以兩種方式影響您的服務：

-   如果您已)  (Spn 註冊服務主體名稱，這些名稱會在錯誤的帳戶中註冊。
-   如果您設定 Ace 來授與服務的存取權，他們現在會將存取權授與錯誤的帳戶。

其中一個方法是讓服務安裝程式為主電腦上登錄中的每個服務實例儲存註冊的 Spn。 您可以在 \_ \_ 用來儲存服務 SCP 之系結字串的 HKEY 本機電腦下使用相同的登錄機碼。 當服務啟動時，它會呼叫 [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) 函式來判斷其登入帳戶，然後查詢 Active Directory 伺服器，以判斷 spn 是否已在該帳戶的目錄物件上註冊。 如果 Spn 未註冊，或已在錯誤的帳戶中註冊，則服務會拒絕啟動，並顯示一則訊息，指出網域系統管理員必須執行服務的設定程式來更新登入帳戶設定。 請注意，這項重新設定必須由系統管理員完成，因為服務帳戶不應該有存取權來更新自己的 SPN。 也請注意，必須從舊帳戶移除 Spn，否則 Spn 將無法用於驗證，因為它們在樹系中並不是唯一的。

 

 