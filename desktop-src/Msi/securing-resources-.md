---
description: Windows Installer 設定服務、檔案、建立資料夾和登錄專案的存取權限，可協助讓安裝應用程式更安全。
ms.assetid: a25fcecf-f15f-4772-8f41-d03864484cc9
title: 保護資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415fe7b2df343a54aa0819031f4fd22b05857618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976943"
---
# <a name="securing-resources"></a>保護資源

Windows Installer 設定服務、檔案、建立資料夾和登錄專案的存取權限，可協助讓安裝應用程式更安全。 使用 [MsiLockPermissionsEx](msilockpermissionsex-table.md) 或 [LockPermissions](lockpermissions-table.md) 資料表來保護資源是 [撰寫安全安裝](guidelines-for-authoring-secure-installations.md)的其中一個建議方針。 MsiLockPermissionsEx 資料表可以讓封裝作者保護資源安全，而不需要撰寫 [自訂動作](custom-actions.md)。

從針對 Windows Installer 5.0 開發的封裝開始， [MsiLockPermissionsEx](msilockpermissionsex-table.md) 資料表應取代 [LockPermissions](lockpermissions-table.md) 資料表的使用。 MsiLockPermissionsEx 資料表提供的擴充功能可讓封裝保護 Windows [服務](../services/services.md)、檔案、資料夾和登錄機碼。 封裝不應同時包含 MsiLockPermissionsEx 和 LockPermissions 資料表。

Windows Installer 4.5 及更早版本會忽略 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md)。 從 Windows Installer 5.0 開始，如果封裝同時包含 [LockPermissions 資料表](lockpermissions-table.md) 和 MsiLockPermissionsEx 資料表，則安裝會失敗，並出現錯誤訊息1941。 仍可使用 Windows Installer 5.0 安裝僅包含 LockPermissions 資料表的現有安裝套件。

Windows Installer 5.0 會在執行[InstallFiles](installfiles-action.md)、 [InstallServices](installservices-action.md)、 [WriteRegistryValues](writeregistryvalues-action.md)和[CreateFolders](createfolders-action.md)標準動作時，處理[MsiLockPermissionsEx](msilockpermissionsex-table.md)資料表中的資訊。 您必須安裝或重新安裝安全物件才能受到保護，而且不可能將 [存取控制清單](../secauthz/access-control-lists.md) (ACL) 附加至現有的物件，而不需要重新安裝該物件。

若要指定要保護的服務、檔案、目錄或登錄機碼，請在 [ [MsiLockPermissionsEx](msilockpermissionsex-table.md) ] 資料表的 [LockObject] 和 [資料表] 欄位中輸入識別資訊。 物件是由其在 [ServiceInstall 資料表](serviceinstall-table.md)、檔案 [資料表](file-table.md)、登錄 [資料表](registry-table.md)或 [CreateFolder 資料表](createfolder-table.md)中的主鍵所識別。

若要要求指定的許可權套用至物件，請使用有效的 [安全描述項定義語言](../secauthz/security-descriptor-definition-language.md) (SDDL) ，在 [MsiLockPermissionsEx](msilockpermissionsex-table.md)資料表的 [ *SDDLText* ] 欄位中輸入有效的安全描述項字串。 **MsiLockPermissionsEx** 資料表可以指定拒絕許可權的安全描述項、指定父資源的許可權繼承，或指定新帳戶的許可權。 如需可授與、拒絕或繼承之擁有權限的清單，請參閱 [ACE 字串](../secauthz/ace-strings.md)。 Windows Installer 5.0 會將一組可用的安全識別碼 (Sid 延伸 ) 。如需有效 Sid 的清單，請參閱 [Sid 字串](../secauthz/sid-strings.md)。

> [!NOTE]
> 如果您想要設定父資源的安全描述項，以指定子物件會繼承其許可權，您的安裝程式必須先將許可權套用至父資源，才能建立子物件。 如果您的安裝程式在將可繼承的許可權套用至父資源之前建立子物件，父資源的許可權將不會傳播到子物件。

從 Windows Installer 5.0 開始， [FormattedSDDLText](formattedsddltext.md) 資料類型會擴充 [格式化](formatted.md) 的資料類型。 Windows Installer 會驗證在 [MsiLockPermissionsEx](msilockpermissionsex-table.md) 資料表的 SDDLText 資料行中輸入的 FormattedSDDLText 字串是否符合 [安全描述項字串格式](../secauthz/security-descriptor-string-format.md)。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用 [MsiLockPermissionsEx](msilockpermissionsex-table.md) 資料表和 [FormattedSDDLText](formattedsddltext.md) 資料類型。

 

 
