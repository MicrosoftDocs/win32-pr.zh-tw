---
description: Windows Installer 可以使用數位簽章來偵測損毀的資源。
ms.assetid: 68f2c686-cbe0-495d-a448-a7d2ca1df47b
title: 數位簽章和 Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334cf226d683c9b9a658ce72e25bf7bf90145369c315da372bd6c4e9368b796a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692808"
---
# <a name="digital-signatures-and-windows-installer"></a>數位簽章和 Windows Installer

Windows Installer 可以使用數位簽章來偵測損毀的資源。 簽署者憑證可以與要由封裝安裝之外部資源的簽署者憑證進行比較。 如需有關使用數位簽章、數位憑證和 [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)的詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 的 [安全性](https://msdn.microsoft.com/library/cc527452.aspx)一節。

使用 Windows Installer，數位簽章可與 Windows Installer 套件、轉換、修補程式、合併模組和外部封包檔一起使用。 Windows安裝程式與 Microsoft Windows XP 上的軟體限制原則整合。 您可以建立原則，以根據不同的準則（包括特定的簽署者憑證或發行者）來允許或防止安裝。 Windows Installer 可以在安裝 CryptoAPI 2.0 版的所有平臺上執行外部封包檔的簽章驗證。

請注意，Windows Installer SDK 所提供的範例 Setup.exe 啟動程式會在起始安裝之前，對 Windows Installer 套件執行簽章檢查。

執行 [系統管理安裝](administrative-installation.md) 會移除套件中的數位簽章。 系統管理安裝會修改安裝套件，以新增 AdminProperties 資料流程，這會使原始數位簽章失效。 系統管理員可以重新簽署封裝。

將修補程式套用至系統管理安裝也會從套件中移除數位簽章。 原因是這些變更會保存在系統管理安裝的修補安裝套件中。 系統管理員可以重新簽署封裝。

從 Windows Installer 版本3.0 開始， [ (UAC) 修補的使用者帳戶控制](user-account-control--uac--patching.md)可讓非系統管理員使用者修補個別電腦內容中安裝的應用程式。 UAC 修補的啟用方式是在 [MsiPatchCertificate](msipatchcertificate-table.md) 資料表中提供簽署者憑證，並使用相同的憑證簽署修補程式。

如需詳細資訊，請參閱[數位簽章和外部封包](digital-signatures-and-external-cabinet-files.md)檔、 [Windows Installer 和軟體限制原則](windows-installer-and-software-restriction-policy.md)、[撰寫完整驗證的已簽署安裝](authoring-a-fully-verified-signed-installation.md)，以及[以 URL 為基礎的 Windows Installer 安裝範例](a-url-based-windows-installer-installation-example.md)。

 

 
