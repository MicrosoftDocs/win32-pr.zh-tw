---
title: 使用本機使用者帳戶做為服務登入帳戶
description: 本機使用者帳戶 (名稱格式 \ 0034;。 \\UserName \ 0034; ) 只存在於主機電腦的 SAM 資料庫中;它沒有 Active Directory Domain Services 中的使用者物件。
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a6d536b83675cc3d4fa9c23db01d8f4137fff228bf72444bec7164a51068ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186853"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a>使用本機使用者帳戶做為服務登入帳戶

本機使用者帳戶 (名稱格式： "。 \\*UserName*") 只存在於主機電腦的 SAM 資料庫中;它沒有 Active Directory Domain Services 中的使用者物件。 這表示網域無法驗證本機帳戶。 因此，在本機使用者帳戶的安全性內容中執行的服務無法存取網路資源 (除了匿名使用者) 之外，它也無法支援用戶端用來驗證服務的 Kerberos 相互驗證。 基於這些理由，本機使用者帳戶通常不適用於啟用目錄的服務。 此外，服務中的 bug 無法損毀系統。 如果您的服務可以在這些限制下執行，則應該如此。

 

 




