---
description: 您可以使用下列方法來判斷 Windows Installer 版本：
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: 判斷 Windows Installer 版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a48434fe415084a93158fb3445a36906d8b8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988272"
---
# <a name="determining-the-windows-installer-version"></a><span data-ttu-id="7f4ff-103">判斷 Windows Installer 版本</span><span class="sxs-lookup"><span data-stu-id="7f4ff-103">Determining the Windows Installer Version</span></span>

<span data-ttu-id="7f4ff-104">您可以使用下列方法來判斷 Windows Installer 版本：</span><span class="sxs-lookup"><span data-stu-id="7f4ff-104">You can use the following methods to determine the Windows Installer version:</span></span>

-   <span data-ttu-id="7f4ff-105">呼叫 [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) 函數，並將 *szFilePath* 參數設定為檔案 Msi.dll 的路徑。</span><span class="sxs-lookup"><span data-stu-id="7f4ff-105">Call the [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) function with the *szFilePath* parameter set to the path to the file Msi.dll.</span></span>

    <span data-ttu-id="7f4ff-106">您可以使用 **CSIDL \_ 系統** 常數來呼叫 [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)函數，以取得 Msi.dll 的路徑。</span><span class="sxs-lookup"><span data-stu-id="7f4ff-106">You can call the [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function with the **CSIDL\_SYSTEM** constant to get the path to Msi.dll.</span></span> <span data-ttu-id="7f4ff-107">從 Windows Vista 開始，應用程式應該使用 [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 函式和 **REFKNOWNFOLDERID** 「系統」。</span><span class="sxs-lookup"><span data-stu-id="7f4ff-107">Beginning with Windows Vista, applications should use the [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) function and the **REFKNOWNFOLDERID** "System."</span></span> <span data-ttu-id="7f4ff-108">使用 **SHGetFolderPath** 函式和 **CSIDL** 類型的現有應用程式將會繼續運作。</span><span class="sxs-lookup"><span data-stu-id="7f4ff-108">Existing applications that use the **SHGetFolderPath** function and the **CSIDL** type will continue to work.</span></span>

-   <span data-ttu-id="7f4ff-109">[**安裝程式物件**](installer-object.md)的 [**installer. Version**](installer-version.md)屬性值相當於 Windows Installer 主題的 [發行版本](released-versions-of-windows-installer.md)中所列出的四個欄位字串。</span><span class="sxs-lookup"><span data-stu-id="7f4ff-109">The value of the [**Installer.Version**](installer-version.md) property of the [**Installer Object**](installer-object.md) is equivalent to the four-field strings listed in the [Released Versions of Windows Installer](released-versions-of-windows-installer.md) topic.</span></span>
-   <span data-ttu-id="7f4ff-110">應用程式可以使用 [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc)取得 Windows Installer 版本。</span><span class="sxs-lookup"><span data-stu-id="7f4ff-110">Applications can get the Windows Installer version by using [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span></span>
-   <span data-ttu-id="7f4ff-111">安裝程式會將 [**VersionMsi**](versionmsi.md) 屬性設定為安裝期間執行的 Windows Installer 版本。</span><span class="sxs-lookup"><span data-stu-id="7f4ff-111">The installer sets the [**VersionMsi**](versionmsi.md) property to the version of Windows Installer that is run during the installation.</span></span>

<span data-ttu-id="7f4ff-112">如需詳細資訊，請參閱 [Windows Installer 的發行版本](released-versions-of-windows-installer.md)。</span><span class="sxs-lookup"><span data-stu-id="7f4ff-112">For more information, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

 

 
