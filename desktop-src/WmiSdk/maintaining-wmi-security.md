---
description: WMI 安全性著重在保護對命名空間資料的存取。 WMI 會先將存取權授與 WMI 控制和 DCOM 設定所指定的使用者群組，然後提供者判斷使用者是否應該具有命名空間資料的存取權。
ms.assetid: 88a2538a-ae30-4a1a-9d16-f0cd9419b2ed
ms.tgt_platform: multiple
title: 維護 WMI 安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79467b3baffd030cae1022f65bc0b8a97242c5e8bbe2f870753a3d3794b8705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118818416"
---
# <a name="maintaining-wmi-security"></a>維護 WMI 安全性

WMI 安全性著重在保護對命名空間資料的存取。 WMI 會先將存取權授與 [*Wmi 控制*](gloss-w.md) 和 DCOM 設定所指定的使用者群組，然後提供者判斷使用者是否應該具有命名空間資料的存取權。

本主題將討論下列各節：

-   [命名空間安全性](#namespace-security)
-   [分散式元件物件模型 (DCOM) 安全性設定。](#distributed-component-object-model-dcom-security-settings)
-   [WMI、共用服務主機和驗證](#wmi-shared-service-hosts-and-authentication)
-   [WMI 用戶端腳本和應用程式的安全性](#security-for-wmi-client-scripts-and-applications)
-   [相關主題](#related-topics)

## <a name="namespace-security"></a>命名空間安全性

命名空間安全性相依于標準 Windows 使用者 [*安全識別碼 (SID)*](gloss-s.md)以及 WMI 命名空間的 [*安全描述項*](gloss-s.md)。

您可以藉由執行下列動作來設定命名空間安全性：

-   使用 WMI 控制或建立命名空間時，授與或拒絕使用者命名空間的存取權限。 如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md) 以及建立 [命名空間時設定命名空間安全性](setting-namespace-security-when-the-namespace-is-created.md)。
-   使用 WMI 控制 [安全性] 索引標籤來建立安全性審核。 安全性審核會在使用者失敗或成功時，產生事件記錄專案，例如將資料寫入至 WMI 物件或讀取安全描述項。 如需詳細資訊，請參閱 [WMI 命名空間的存取](access-to-wmi-namespaces.md)。
-   使用定義命名空間的 MOF 檔案，要求使用者建立加密的連接。 如需詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。

## <a name="distributed-component-object-model-dcom-security-settings"></a>分散式元件物件模型 (DCOM) 安全性設定。

DCOM 安全性需要驗證設定和模擬設定。 驗證表示一個進程會將本身識別為另一個進程。 模擬會識別用戶端授與伺服器以呼叫不同進程的授權單位。 在安全性檢查期間，伺服器會模擬用戶端。 如需詳細資訊，請參閱 [保護 c + + 用戶端和提供者](securing-c---clients-and-providers.md) ，或 [保護腳本用戶端](securing-scripting-clients.md)。

腳本和 C/c + +/C # 應用程式會在連線至 WMI 命名空間時建立驗證和模擬層級，或使用預設設定。 遠端電腦的連線需要與本機電腦上的 WMI 命名空間不同的設定。 如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。

## <a name="wmi-shared-service-hosts-and-authentication"></a>WMI、共用服務主機和驗證

WMI 存在於共用服務主機中，有數個其他服務在 NetworkService 帳戶下執行。 在 Svchost 進程中，WMI 與主機中的其他進程共用相同的驗證。

從 WMI 將提供者 Dll 載入至不同的服務主機進程。 代表提供者之 [**\_ \_ Win32Provider**](--win32provider.md)系統類別中的 **HostingModel** 屬性會指定提供者執行時所使用的系統帳戶。 設定這個屬性會使提供者載入具有指定許可權層級的共用主機進程中。 如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。

## <a name="security-for-wmi-client-scripts-and-applications"></a>WMI 用戶端腳本和應用程式的安全性

腳本和應用程式必須建立正確的安全性，以連接到本機和遠端電腦上的 WMI 命名空間。 如需詳細資訊，請參閱 [保護 c + + 用戶端和提供者](securing-c---clients-and-providers.md)、 [保護腳本用戶端](securing-scripting-clients.md)安全，以及 [保護 WMI 事件](securing-wmi-events.md)。

下表列出有關維護 WMI 安全性的主題。



| 主題                                                                                              | 描述                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [保護 WMI 命名空間](securing-wmi-namespaces.md)                                             | 您可以透過 WMI 控制項，將命名空間資料存取限制為已授權的使用者。                                                                                      |
| [保護您的提供者](securing-your-provider.md)                                               | 撰寫安全提供者的相關資訊。                                                                                                                           |
| [保護 c + + 用戶端和提供者](securing-c---clients-and-providers.md)                       | C + + 提供者和用戶端應用程式都必須執行許多相同的作業來維護 WMI 安全性。                                                         |
| [保護腳本用戶端](securing-scripting-clients.md)                                       | 腳本和 Visual Basic 應用程式 (automation 用戶端) 必須設定適當的安全性，以存取 WMI 資料和事件。                                        |
| [保護 WMI 事件](securing-wmi-events.md)                                                     | WMI 事件是由事件提供者傳遞給暫時或永久的取用者。 事件是以事件類別實例的形式傳遞。               |
| [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md) | 使用適當的許可權，您可以在 WMI 物件上呼叫方法，這些物件代表可讀取或變更安全物件安全描述項的安全物件。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WMI](using-wmi.md)
</dt> </dl>

 

 



