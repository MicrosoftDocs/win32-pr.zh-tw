---
description: Windows 驗證套件會為 LSA 提供的 LsaLogonUser 和 LsaCallAuthenticationPackage 函數實作為封裝專屬的功能，藉此提供驗證服務。
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Windows驗證套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8288e54398702994938627b13c745a67f96fbc44dc710e2e5a7ac65a8620685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915077"
---
# <a name="windows-authentication-packages"></a>Windows驗證套件

Windows 驗證套件會為 LSA 提供的 [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser)和 [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage)函數實作為封裝專屬的功能，藉此提供驗證服務。

MSV1 \_ 0 是 Windows [*authentication 套件*](../secgloss/a-gly.md)的範例。 MSV1 \_ 0 封裝可接受使用者名稱和 [*雜湊*](../secgloss/h-gly.md) 密碼，這會在 [*安全性帳戶管理員*](../secgloss/s-gly.md) (SAM) 資料庫中查閱。 MSV1 0 authentication 套件會根據查閱結果來 \_ 接受或拒絕驗證嘗試。

如需 LSA 提供的支援函式清單，讓 Windows 驗證需要系統服務的封裝使用，請參閱[驗證封裝所呼叫的 lsa 函數](authentication-functions.md)。

Windows 驗證套件必須執行一組 LSA 所呼叫的函數。 如需函式的完整清單，請參閱 [驗證封裝所執行](authentication-functions.md)的函式。

 

 
