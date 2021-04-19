---
description: Windows Installer 可以使用交易處理來安裝多個封裝。
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Multiple-Package 安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65fa30893f353d6661a7f77fe23fe55b4c9b22c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977264"
---
# <a name="multiple-package-installations"></a>Multiple-Package 安裝

Windows Installer 可以使用 [*交易處理*](t-gly.md)來安裝多個封裝。 從 Windows Installer 4.5 開始，可以使用這項功能。 安裝程式將會安裝屬於多封裝交易的所有封裝，或不安裝任何套件。 如果無法順利安裝交易中的所有封裝，或如果使用者取消安裝，Windows Installer 可以復原變更，並將電腦還原為其原始狀態。

多套件安裝封裝可以包含 [MsiEmbeddedChainer 資料表](msiembeddedchainer-table.md) ，該資料表會參考使用 [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona)、 [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)和 [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) 函數的使用者定義函數。

[MsiPackageCertificate 資料表](msipackagecertificate-table.md)會列出數位簽章憑證，用來驗證進行多套件安裝之安裝套件的身分識別。 您可以使用此表格來減少多套件安裝在需要系統管理員回應的 (UAC) 提示字元中，顯示 [*使用者帳戶控制*](u-gly.md) 的次數。

下列 Windows Installer 功能可在 Windows Installer 安裝、修復、更新或移除應用程式時，對使用者的電腦進行變更。 從 Windows Installer 4.5 開始，安裝程式可以在多套件安裝的 [*交易處理*](t-gly.md) 期間復原這些函數所做的變更：

<dl>

[**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)  
[**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)  
[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)  
[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)  
[**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)  
[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)  
[**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)  
[**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)  
[**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)  
[**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)  
[**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)  
[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)  
[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)  
[**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)  
[**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)  
[**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)  
[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)  
</dl>

如果 Windows Installer 遇到屬於包含 [ForceReboot](forcereboot-action.md) 或 [ScheduleReboot](schedulereboot-action.md) 動作之多套件安裝的封裝，就會發生例外狀況。 在此情況下，Windows Installer 不會安裝該套件。 您可以安裝屬於多套件安裝的其他套件，而這些套件不包含 ForceReboot 或 ScheduleReboot 動作。

**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：不支援多個封裝 Windows Installer 安裝的 [*交易處理*](t-gly.md) 。 這些版本的 Windows Installer 無法將多個封裝的安裝復原成單一交易。

**啟用 [遠端桌面服務](../termserv/terminal-services-portal.md) 角色的 Windows Server 2008 R2：** 不支援。 如果啟用[遠端桌面服務](../termserv/terminal-services-portal.md)角色，使用[MsiEmbeddedChainer 資料表](msiembeddedchainer-table.md)的多個套件安裝將會失敗。

 

 
