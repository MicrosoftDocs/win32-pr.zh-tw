---
description: 您可以使用下列方法來判斷 Windows Installer 版本：
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: 判斷 Windows Installer 版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e13907790585356fa4a5bc8376fe87f30793e0e3af71e1b0c113f30cf04b8f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764218"
---
# <a name="determining-the-windows-installer-version"></a>判斷 Windows Installer 版本

您可以使用下列方法來判斷 Windows Installer 版本：

-   呼叫 [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) 函數，並將 *szFilePath* 參數設定為檔案 Msi.dll 的路徑。

    您可以使用 **CSIDL \_ 系統** 常數來呼叫 [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)函數，以取得 Msi.dll 的路徑。 從 Windows Vista 開始，應用程式應該使用 [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)函式和 **REFKNOWNFOLDERID** 「系統」。 使用 **SHGetFolderPath** 函式和 **CSIDL** 類型的現有應用程式將會繼續運作。

-   [**安裝程式物件**](installer-object.md)的 [**installer. Version**](installer-version.md)屬性值相當於 Windows Installer 主題的 [發行版本](released-versions-of-windows-installer.md)中所列出的四個欄位字串。
-   應用程式可以使用 [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc)取得 Windows Installer 版本。
-   安裝程式會將 [**VersionMsi**](versionmsi.md)屬性設定為安裝期間執行的 Windows Installer 版本。

如需詳細資訊，請參閱[Windows Installer 的發行版本](released-versions-of-windows-installer.md)。

 

 
