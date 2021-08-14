---
title: 選取服務登入帳戶的指導方針
description: 以 Win32 為基礎的服務可以在本機使用者帳戶、網域使用者帳戶或 LocalSystem 帳戶的安全性內容中執行。
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- 選取服務登入帳戶 AD 的指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a976927130a3585be2e6130dbb71b37fa0c69660b6ae953e28909fad3db570f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188672"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a>選取服務登入帳戶的指導方針

以 Win32 為基礎的服務可以在本機使用者帳戶、網域使用者帳戶或 LocalSystem 帳戶的安全性內容中執行。 若要決定要使用哪個帳戶，系統管理員應該使用執行服務作業所需的最少許可權集來安裝服務。 在一般啟用目錄的服務中，這表示服務安裝程式應該建立服務的網域使用者帳戶，並將服務在執行時間所需的特定存取權和許可權授與該帳戶。 如果服務需要系統管理許可權，或必須做為本機電腦上作業系統的一部分，則服務應該只在 LocalSystem 帳戶下執行。

請注意，根據預設，服務安裝程式應該將服務設定為以網域使用者帳戶執行。 若要在 LocalSystem 帳戶下執行服務，服務安裝程式應查詢系統管理員，以取得執行此動作的許可權。

如需每種帳戶類型的描述、優點和缺點的詳細資訊，請參閱：

-   [本機使用者帳戶](local-user-accounts.md)。
-   [網域使用者帳戶](domain-user-accounts.md)。
-   [LocalSystem 帳戶](the-localsystem-account.md)。

 

 




