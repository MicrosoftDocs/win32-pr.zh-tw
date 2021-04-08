---
title: 建立服務連接點的位置
description: 當安裝 Active Directory Domain Services 的實例時，服務安裝程式會在 Active Directory Domain Services 中 (SCP) 建立服務連接點物件。
ms.assetid: a90566d9-dd68-43e2-be9e-300d57a7fbf4
ms.tgt_platform: multiple
keywords:
- 何處可以建立服務連接點 AD
- active directory，在何處建立服務連接點
- 何處可以建立服務連接點 AD
- 建立服務連接點 AD
- 服務連接點 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf122ebabcfd8085ebad46314ffd1c09f827e783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020819"
---
# <a name="where-to-create-a-service-connection-point"></a>建立服務連接點的位置

當安裝 Active Directory Domain Services 的實例時，服務安裝程式會在 Active Directory Domain Services 中 (SCP) 建立服務連接點物件。 主要目標應該是將複寫流量降到最低，並啟用物件的有效率管理和維護。

請注意，用戶端應用程式會搜尋 SCP 中關鍵字的目錄來尋找 Scp。 SCP 的 **關鍵字** 屬性包含在通用類別目錄中;用戶端可以搜尋通用類別目錄，以在樹系中尋找 Scp。 基於這個理由，用戶端並不會影響發佈 Scp 的位置。

## <a name="minimize-replication-traffic"></a>最小化複寫流量

若要將複寫流量降到最低，請在服務主機電腦之網域的網域分割區中建立 Scp。 例如，您可以將 Scp 建立為安裝服務之電腦物件的子物件。 Active Directory Domain Services 的網域分割（有時也稱為網域命名內容）包含網域特定物件，例如網域的使用者和電腦的物件。 網域分割區中所有物件的完整複本會複寫到網域的每個網域控制站 (DC) ，但不會複寫到其他網域的 Dc。

請勿在設定磁碟分割（也稱為設定命名內容）中建立 Scp，因為設定磁碟分割的變更會複寫到樹系中的每個 DC。 如上所述，整個樹系中的用戶端都可以查詢通用類別目錄來尋找樹系中任何位置的 Scp，因此在設定分割區中建立 Scp 並不會讓用戶端看見它們。它只會產生更多的複寫流量。

## <a name="ease-of-administration"></a>易於管理

針對物件管理，請考慮下列指導方針：

-   使用原則和繼承存取權限，來放置系統管理員可以控制其存取權的特定服務物件。
-   將物件放在系統管理員可以輕鬆找到這些物件的位置。

符合這兩個目標的良好預設位置是在每個服務實例主機電腦的電腦物件下建立 SCP 和其他服務特定物件。 如需詳細資訊，請參閱 [在電腦物件下發行](publishing-under-a-computer-object.md)。

針對未系結至單一主機的服務，最好的替代方法是在網域分割區的系統容器底下建立服務物件的容器。 如需詳細資訊，請參閱 [在網域系統容器中發行](publishing-in-a-domain-system-container.md)。

下圖顯示網域分割的部分預設容器階層。

![預設網域分割容器階層](images/domain-container-heirarchy.png)

下圖顯示 Active Directory Domain Services 包含的預設網域階層。 不過，許多企業會建立組織單位的階層， (OU) 容器來將物件類別（例如使用者和電腦）組成群組，以供管理之用。 然後，系統管理員可以將原則和可繼承的存取控制專案 (Ace) 套用至 OU，以委派 OU 中物件的系統管理授權。 這可讓系統管理員有效率地管理企業，但對於服務程式設計人員有一些結果：

-   服務主機的電腦物件可能不在 [電腦] 容器底下，如下圖所示。 如需有關如何尋找本機電腦之電腦物件的詳細資訊，請參閱 [在電腦物件下發布](publishing-under-a-computer-object.md)。
-   系統管理員可以在組織需要變更時移動物件。 這表示您無法依賴固定位置中剩餘的物件;也就是說，您的服務無法依賴剩餘的物件辨別名稱。 相反地，請使用物件的 **objectGUID** 屬性，如果物件已移動或重新命名，則不會變更。 如需詳細資訊，以及建立 SCP 的程式碼範例，請儲存其 **objectguid**，並于稍後抓取要系結至 SCP 的 **objectguid** ，請參閱 [建立和維護服務連接點](creating-and-maintaining-a-service-connection-point.md)。
-   所有標準服務相關的物件類別以及這些類別的任何子類別，都是 **電腦** 和 **organizationalUnit** 類別的有效子系。 如果您延伸架構來定義您自己的服務專屬類別，請確定 **電腦** 和 **organizationalUnit** 類別都包含在可能的 superiors 中。
-   服務安裝程式會決定用來建立 Scp 的預設位置。 您可能會想要允許安裝服務的系統管理員指定替代的安裝路徑。

不應該在下欄區域中建立服務特定物件：

-   服務不應該直接在網域分割區的 [使用者] 或 [電腦] 容器中發佈物件，也不應該在這些容器中建立新的容器。 不過，無論電腦物件是否儲存在 [電腦] 容器中，服務都可以將物件發佈為電腦物件的子物件。
-   使用 Windows 通訊端註冊和解析 (RnR) 或 RPC 名稱服務的服務， (RpcNs) Api 來通告本身，請在 WinsockServices 和 RpcServices 容器的網域分割區系統容器底下建立適當的物件。 請勿在這些容器中明確建立物件。 這樣做並不會造成直接損害，但對系統管理員來說可能會造成混淆。

 

 




