---
description: Windows Installer 符合 Windows Vista 中 (UAC) 的使用者帳戶控制。
ms.assetid: 13955ded-6b7f-475f-bb0f-6530a0b4963f
title: 搭配使用 Windows Installer 與 UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a05dcd2fb33eff24fb17702af1cb306f81002d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114152"
---
# <a name="using-windows-installer-with-uac"></a>搭配使用 Windows Installer 與 UAC

Windows Installer 符合 Windows Vista 中 (UAC) 的 [*使用者帳戶控制*](u-gly.md) 。 透過系統管理員的授權，Windows Installer 可以代表可能不是系統管理員群組成員的使用者來安裝應用程式或修補程式。 這稱為提高 [*許可權*](e-gly.md) 的安裝，因為 Windows Installer 會代表使用者對系統進行變更，而使用者直接進行變更時通常不會允許。

-   在公司環境中使用 Windows Vista 時，可以將應用程式指定為受控應用程式。 系統管理員可以使用應用程式部署和 [群組原則](/previous-versions/windows/desktop/Policy/group-policy-start-page)來鎖定目錄，然後將這些目錄中的受控應用程式指派或發佈給 [*標準使用者*](s-gly.md) ，以進行安裝、修復或移除。 受控應用程式會在 **HKEY \_ 本機 \_ 電腦** 登錄 hive 中註冊。 一旦將應用程式註冊為受控應用程式，後續的安裝作業一律會以較高的許可權執行。 如果使用者是以系統管理員身分執行，則不需要提示以繼續安裝。 如果使用者是以標準使用者的身份執行，而且已指派或發佈該應用程式，則可以在不提示的情況下繼續安裝受控應用程式。
-   在非企業環境中使用 Windows Vista 時，UAC 會處理應用程式安裝的提高許可權。 Windows Installer 4.0 可以 (AIS) 呼叫 [*應用程式資訊服務*](a-gly.md) ，要求系統管理員授權提高安裝的許可權。 在識別為需要系統管理員許可權的安裝之前，UAC 會提示使用者是否同意提升安裝的許可權。 預設會顯示同意提示，即使使用者是本機系統管理員群組的成員，因為系統管理員會以標準使用者身分執行，直到需要系統管理認證的應用程式或系統元件要求執行許可權為止。 此使用者體驗稱為「 [*管理核准模式*](a-gly.md) 」 (AAM) 。 如果標準使用者嘗試安裝應用程式，使用者必須取得具有系統管理員許可權的人員，以提供其系統管理員認證以繼續安裝。 此使用者體驗 [*稱為 (OTS*](o-gly.md)) 認證提示。
-   由於 UAC 會在安裝階段限制許可權，因此 Windows Installer 套件的開發人員不應假設其安裝一律可存取系統的所有部分。 因此 Windows Installer 套件開發人員應遵守套件 [指導](guidelines-for-packages.md) 方針中所述的封裝指導方針，以確保其套件適用于 UAC 和 Windows Vista。 經過撰寫並測試以符合 UAC 的封裝應該包含設定為1的 [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) 屬性。
-   系統管理員也可以使用一節中所述的方法：以非系統管理員的較 [高許可權安裝封裝](installing-a-package-with-elevated-privileges-for-a-non-admin.md) ，讓非系統管理員使用者可以使用提高的系統許可權安裝應用程式。
-   需要許可權才能在每個使用者管理的內容中安裝應用程式，因此後續 Windows Installer 重新安裝或修復應用程式時，安裝程式也會使用較高的許可權來執行。 這表示，只有來自信任來源的修補程式才能以每位使用者管理的狀態套用至應用程式。 從 Windows Installer 3.0 開始，您可以在修補程式註冊為具有更高許可權之後，將修補程式套用至每位使用者的受控應用程式。 如需詳細資訊，請參閱 [修補 Per-User 受控應用程式](patching-per-user-managed-applications.md)。

> [!Note]  
> 當安裝 Windows Installer 封裝時不需要提高許可權時，套件的作者可以隱藏 UAC 顯示的對話方塊，以提示使用者提供系統管理員授權。 如需詳細資訊，請參閱 [撰寫沒有 UAC 的封裝對話方塊](authoring-packages-without-the-uac-dialog-box.md)。

 

 

 
