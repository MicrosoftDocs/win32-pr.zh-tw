---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiPolicy.vbs。 此範例說明如何使用腳本來管理系統策略。 系統管理員可以使用群組原則編輯器 (GPE) 來設定原則。
ms.assetid: 17cfed46-503f-4124-9f0e-1655fda153d0
title: 管理原則設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1261c48ec7cc7e51a8556b7565075fa9e92bd60481da08f4f311a3de995a91f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945603"
---
# <a name="manage-policy-settings"></a>管理原則設定

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiPolicy.vbs。 此範例說明如何使用腳本來管理 [系統原則](system-policy.md)。 系統管理員可以使用群組原則編輯器 (GPE) 來設定原則。

此範例示範 Windows Installer 原則。

使用此範例需要 Windows 腳本主機的 CScript.exe 或 WScript.exe 版本。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiPolicy.vbs \[ 原則 \] \[ 值\]**

如果在命令列上未指定任何引數，此範例會傳回目前的原則設定。 使用下列識別碼代碼指定要設定的原則。 指定原則的新值。 若要傳回原則的目前值，請將值指定為空字串 ""。



| CODE | 描述                                                                                                                                  |
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| LM   | 記錄模式。 如需詳細資訊，請參閱 [記錄](logging.md) 。                                                                            |
| DO   | Debug 模式。 如需詳細資訊，請參閱 [Debug](debug.md)。                                                                                   |
| DI   | 停用 Windows Installer 模式。 如需詳細資訊，請參閱 [DisableMsi](disablemsi.md)。                                                      |
| WT.   | 在沒有活動的情況下，以秒為單位的等候時間。 **HKLM** \\**軟體** \\**原則** \\**Microsoft** \\**Windows** \\**安裝程式** \\**Timeout** |
| DB   | 停用使用者流覽來源位置。 如需詳細資訊，請參閱 [DisableBrowse](disablebrowse.md)。                                     |
| DP   | 停用修補。 如需詳細資訊，請參閱 [DisablePatch](disablepatch.md)。                                                                |
| UC   | 傳送給安裝服務的公用屬性。 如需詳細資訊，請參閱 [EnableUserControl](enableusercontrol.md)。                             |
| SS   | 從瀏覽器編寫腳本的安全安裝程式。 如需詳細資訊，請參閱 [SafeForScripting](safeforscripting.md)。                               |
| EM   |  (HKLM) 的系統許可權。 如需詳細資訊，請參閱 [AlwaysInstallElevated](alwaysinstallelevated.md)。                                      |
| EU   |  (HKCU) 的系統許可權。 如需詳細資訊，請參閱 [AlwaysInstallElevated](alwaysinstallelevated.md)。                                      |
| DR   | 停用回復原則。 如需詳細資訊，請參閱 [DisableRollback](disablerollback.md)。                                                   |
| TS   | 在來源映射的根目錄中找出轉換。 如需詳細資訊，請參閱 [TransformsAtSource 原則](transformsatsource-policy.md)。             |
| TP   | 在用戶端快取中釘選安全會將。 如需詳細資訊，請參閱 [TransformsSecure 原則](transformssecure-policy.md)。                 |
| SO   | 來源類型的搜尋順序。 如需詳細資訊，請參閱 [SearchOrder](searchorder.md)。                                                      |



 

如需其他腳本範例，請參閱[Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows 腳本主機的範例公用程式，請參閱[Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



