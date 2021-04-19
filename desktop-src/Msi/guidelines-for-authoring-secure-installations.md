---
description: 若要在軟體安裝期間協助維護安全的環境，請在撰寫 Windows Installer 套件時遵守這些指導方針。
ms.assetid: 04d91a9b-0528-4acb-8e11-fc817009db1f
title: 撰寫安全安裝的指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d18e66c38480149ddad9e381c6461ffe50cf0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980367"
---
# <a name="guidelines-for-authoring-secure-installations"></a>撰寫安全安裝的指導方針

在撰寫 Windows Installer 套件時遵循下列指導方針，可協助您在安裝期間維護安全的環境：

-   系統管理員應將受管理的應用程式安裝到目標安裝資料夾中，而非系統管理員的使用者沒有變更或修改許可權。
-   將任何由使用者設定的屬性設為公用屬性。 使用者與使用者介面互動時，無法變更私用屬性。 如需相關資訊，請參閱 [關於屬性](about-properties.md)。
-   請勿將屬性用於密碼或其他必須保持安全的資訊。 安裝程式可以將撰寫的屬性值寫入至記錄檔或系統登錄 [中，或是](property-table.md)在執行時間建立的屬性值。 如需其他資訊，請參閱 [防止機密資訊寫入至記錄](preventing-confidential-information-from-being-written-into-the-log-file.md)檔。
-   當安裝需要安裝程式使用較 [*高*](e-gly.md) 的許可權時，請使用 [受限制的公用屬性](restricted-public-properties.md) 來限制使用者可變更的公用屬性。 當安裝要求安裝程式需要使用較 *高* 的許可權時，通常需要一些限制才能維護安全的環境。
-   請避免安裝可模擬特定使用者之許可權的服務，因為這可能會將安全性資料寫入至記錄檔或系統登錄。 這會造成安全性問題、密碼衝突或系統重新開機時遺失設定資料的可能性。 如需詳細資訊，請參閱 [ServiceInstall 資料表](serviceinstall-table.md)。
-   使用 [LockPermissions 資料表](lockpermissions-table.md) 和 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md) ，在鎖定的環境中保護服務、檔案、登錄機碼和建立的資料夾。
-   在安裝中新增數位簽章，以確保檔案的完整性。 如需詳細資訊，請參閱 [數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md) ，並 [撰寫經過完整驗證的已簽署安裝](authoring-a-fully-verified-signed-installation.md)。
-   撰寫您的 Windows Installer 套件，如此一來，如果使用者被拒絕存取資源，則安裝程式會以維護安全環境的方式失敗。 檢查使用者的存取權限，並判斷是否有足夠的磁碟空間，然後才開始安裝。 通常，如果目前的使用者是系統管理員，或如果安裝不需要較 [*高*](e-gly.md) 的許可權，安裝程式應該只顯示 [流覽] 對話方塊。 如需詳細資訊，請參閱 [來源復原](source-resiliency.md)。
-   使用 [安全的轉換](secured-transforms.md) 將轉換儲存在使用者電腦本機的安全檔案系統中。 這可防止使用者擁有轉換的寫入權限。
-   如需如何保護受控應用程式之媒體來源的詳細資訊，請參閱 [來源復原](source-resiliency.md)。
-   使用 [ [**安全性摘要**](security-summary.md) ] 屬性來指出是否應該以唯讀方式開啟封裝。 這個屬性應該設為唯讀，建議用於安裝資料庫，並針對轉換或修補程式強制唯讀。
-   安裝程式預設會以使用者權限執行自訂動作，以限制對系統的自訂動作的存取。 如果正在安裝受管理的應用程式，或已針對較高的許可權指定系統原則，則安裝程式可能會以更 [*高*](e-gly.md) 的許可權執行自訂動作。 如需詳細資訊，請參閱 [自訂動作安全性](custom-action-security.md)。
-   使用 [DisablePatch](disablepatch.md) 原則，在必須限制修補的環境中提供安全性。
-   使用 [AppId 資料表](appid-table.md) 來註冊 DCOM 物件的一般安全性和設定。
-   如需相關資訊，請參閱 [保護自訂動作的指導方針](guidelines-for-securing-custom-actions.md)。
-   如需相關資訊，請參閱 [在鎖定的電腦上保護套件安全的指導方針](guidelines-for-securing-packages-on-locked-down-computers.md)。
-   從 Windows Installer 3.0 開始， [ (UAC) 修補的使用者帳戶控制](user-account-control--uac--patching.md) 可讓非系統管理員使用者修補個別電腦內容中安裝的應用程式。 UAC 修補的啟用方式是在 [MsiPatchCertificate](msipatchcertificate-table.md) 資料表中提供簽署者憑證，並使用相同的憑證簽署修補程式。
-   Windows Installer 5.0 的功能來設定服務、檔案、建立資料夾和登錄專案的存取權限，可協助讓安裝應用程式更安全。 如需詳細資訊，請參閱 [保護資源](securing-resources-.md)。

 

 



