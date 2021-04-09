---
description: 由於使用者帳戶控制 (Windows Vista 中的 UAC) 在安裝期間會限制許可權，因此 Windows Installer 套件的開發人員不應假設其安裝一律可存取系統的所有部分。
ms.assetid: 8e3b4ad8-b978-4e27-b060-1d023846718f
title: 封裝的指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db228c2dff443d421ddc089074f0fcce6ae93e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850207"
---
# <a name="guidelines-for-packages"></a>封裝的指導方針

由於 [*使用者帳戶控制*](u-gly.md) (Windows Vista 中的 UAC) 在安裝期間會限制許可權，因此 Windows Installer 套件的開發人員不應假設其安裝一律可存取系統的所有部分。

在大部分情況下，可以透過 [群組原則](/previous-versions/windows/desktop/Policy/group-policy-start-page) 成功部署至標準使用者的安裝程式套件，在大部分情況下也適用于 Windows Vista 中的 UAC。 如果 [InstallUISequence 資料表](installuisequence-table.md) 包含 [LaunchConditions 動作](launchconditions-action.md) ，或 [LaunchCondition 資料表](launchcondition-table.md) 包含以特殊 [許可權屬性](privileged.md)為基礎的條件，就會發生這種例外狀況。 因此 Windows Installer 套件開發人員應該遵循下列指導方針，以確保其套件適用于 UAC 和 Windows Vista。

-   當您在 [InstallUISequence 資料表](installuisequence-table.md)中包含具有動作的 [*安裝內容*](i-gly.md)條件時，請根據具有特殊許可權的 [屬性](privileged.md)來使用條件陳述式。 請勿使用以 [**AdminUser**](adminuser.md) 屬性為基礎的條件。
-   包含安裝啟動條件的安裝內容時，請在[InstallExecuteSequence 資料表](installexecutesequence-table.md)中使用[自訂動作類型 19](custom-action-type-19.md) ，並在具有特殊[許可權的屬性](privileged.md)上進行自訂動作的條件。 請勿將 [LaunchCondition 資料表](launchcondition-table.md) 中的動作與以 [AdminUser 屬性](adminuser.md) 或許可權屬性為基礎的條件一起使用。
-   若要讀取或修改系統組態，請在[InstallExecuteSequence 資料表](installexecutesequence-table.md)中使用[延後執行自訂動作](deferred-execution-custom-actions.md)。 請勿使用 [InstallUISequence 資料表](installuisequence-table.md) 中的立即執行自訂動作來修改系統組態。
-   若要修改非使用者特定系統的元件，請在 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中使用延遲的自訂動作。 您應該在自訂動作類型中包含 msidbCustomActionTypeNoImpersonate 位。
-   從 [ [**字數統計**](word-count-summary.md) 摘要] 屬性的值省略 Bit 3，表示封裝可能需要提高許可權。 除非需要提高的許可權，才能安裝此封裝，否則請勿包含此位。
-   包含具有應用程式所要求之執行層級的資訊清單。
-   在原始封裝的 [MsiPatchCertificate](msipatchcertificate-table.md) 資料表中包含憑證，並使用相同的憑證簽署所有修補程式。
-   如果安裝 Windows Installer 封裝需要較高的許可權，則套件的作者應該包含用來啟動安裝之[按鈕控制項](pushbutton-control.md)的[ElevationShield](elevationshield-attribute.md)屬性。 這會提醒使用者按一下按鈕會顯示 UAC 對話方塊，要求系統管理員授權才能繼續安裝。
-   將 [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) 屬性設定為1，表示已撰寫並測試封裝的 Windows Installer，以符合 Windows Vista 中的 UAC。 如果未設定此屬性，安裝程式會判斷套件是否符合 UAC。

在 [群組原則](/previous-versions/windows/desktop/Policy/group-policy-start-page)之外，下列 UAC 合規性檢查可用於 Windows XP。

**若要檢查群組原則之外的 UAC 合規性**

1.  以系統管理員身分登入電腦。
2.  針對每部電腦安裝公告套件：

    **msiexec/jm** *package.msi*

3.  登出電腦。
4.  以標準使用者的身份登入電腦。
5.  嘗試安裝已公告的封裝：

    **msiexec/i** *package.msi*

6.  在大部分情況下，如果安裝成功，套件就會符合 UAC 規範。
7.  將封裝中的 [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) 屬性設定為1。
8.  使用 Windows Vista 測試封裝的正確安裝。

 

 
