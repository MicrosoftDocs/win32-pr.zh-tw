---
title: LocalService
description: 將物件安裝為服務應用程式。
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- LocalService 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842795"
---
# <a name="localservice"></a>LocalService

將物件安裝為服務應用程式。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a>備註

除了以本機伺服器可執行檔的形式執行 (EXE) ，COM 物件也可以選擇將本身封裝成在本機或遠端用戶端啟動時，以服務應用程式的形式執行。 服務支援許多有用和 UI 整合的管理功能，包括本機和遠端啟動、停止、暫停和重新開機，以及能夠建立伺服器以在特定使用者帳戶和視窗工作站上執行。

藉由建立 **LocalService** 值並執行標準服務安裝，會安裝寫入為服務的物件以供 COM 使用。 **LocalService** 值必須設定為 **HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Services** 中所設定的服務名稱，作為預設的 **REG \_ SZ** 值。

設定 **LocalService** 時，任何指派給 [**ServiceParameters**](serviceparameters.md) 的字串都會作為命令列引數傳遞至服務，因為它正在啟動中。

在許多情況下，在本機和遠端服務管理 Api 和使用者介面的功能可能對物件提供的服務很有用時，就會偏好使用服務設定。 例如，如果物件的存留期很長，或是很容易支援啟動、停止、重設或暫停等概念，利用服務架構的現有系統管理架構應該是很明顯的選擇。

服務可以動態設定，並可設定為在電腦開機時自動執行，或在用戶端應用程式要求時啟動。

如果您要將類別實作為服務，您應該注意下列幾點：

-   本機和遠端啟用 requestsâ的 [**LocalServer32**](localserver32.md) 金鑰偏好使用此值。如果 **LocalService** 存在且參考有效的服務，則會忽略 **LocalServer32** 索引鍵。
-   目前，只有服務應用程式的單一實例可以在電腦上的指定時間執行。 因此，COM 服務必須在啟動時使用 REGCLS MULTIPLEUSE 註冊其類別物件 \_ ，以支援多個用戶端。
-   若要正確啟動和初始化，設定為在電腦開機時自動執行的 COM 服務必須在其相依服務清單中包含 RPCSS。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> <dt>

[**ServiceParameters**](serviceparameters.md)
</dt> <dt>

[服務](/windows/desktop/Services/services)
</dt> </dl>

 

 