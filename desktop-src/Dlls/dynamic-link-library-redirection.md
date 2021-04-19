---
description: 應用程式可相依于特定版本的共用 DLL，如果另一個應用程式是使用較新或較舊版本的相同 DLL 安裝，就會開始失敗。
ms.assetid: 3b426b6c-1ad5-43b9-81ea-5e6d3c6588c8
title: Dynamic-Link 程式庫重新導向
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b575d566231058cca13c10a067a3c2e20078073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969239"
---
# <a name="dynamic-link-library-redirection"></a>Dynamic-Link 程式庫重新導向

應用程式可相依于特定版本的共用 DLL，如果另一個應用程式是使用較新或較舊版本的相同 DLL 安裝，就會開始失敗。 有兩種方式可確保您的應用程式使用正確的 DLL： DLL 重新導向和並存元件。 開發人員和系統管理員應針對現有的應用程式使用 DLL 重新導向，因為它不需要對應用程式進行任何變更。 如果您要建立新的應用程式或更新應用程式，並想要將應用程式與潛在問題隔離，請建立 [並存元件](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)。

若要啟用整個電腦的 DLL 重新導向，您必須建立新的登錄機碼。 在 **HKLM\Software\Microsoft\Windows nt\currentversion\image file execution 檔執行選項** 中建立名為 **DEVOVERRIDEENABLE** 的新 DWORD 金鑰，並將它設定為1。 之後，您必須重新開機電腦以查看效果。

若要使用 DLL 重新導向， *請為您的應用* 程式建立重新導向檔案。 重新導向檔案的命名方式必須如下： *應用程式 \_ 名稱*。 local。 例如，如果應用程式名稱是 Editor.exe，則重新導向檔案應該命名為 Editor.exe. local。 您必須在應用程式目錄中安裝本機檔案。 您也必須在應用程式目錄中安裝 Dll。

系統會忽略重新導向檔案的內容，但它的目前狀態會導致 Windows 在每次載入 DLL 時檢查應用程式目錄，不論指定的路徑為 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)。 如果在應用程式目錄中找不到 DLL，則這些函式會使用其一般搜尋順序。 例如，如果應用程式 c： \\ myapp \\myapp.exe 使用下列路徑來呼叫 **LoadLibrary** ：

c： \\ program files \\ common files \\ system \\mydll.dll

而且，如果 c： \\ myapp \\myapp.exe. local 和 c： \\ myapp \\mydll.dll 存在， [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 會載入 c： \\ myapp \\mydll.dll。 否則， **LoadLibrary** 會將 c： \\ program files \\ common files \\ systemmydll.dll 載入 \\ 。

或者，如果名稱為 c： \\ myappmyapp.exe 的目錄 \\ 存在，並且包含 mydll.dll， [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 會載入 c： \\ myapp \\myapp.exe。本機 \\mydll.dll。

如果應用程式具有資訊清單，則會忽略任何的本機檔案。

如果您使用 DLL 重新導向，但應用程式沒有搜尋順序中所有磁片磁碟機和目錄的存取權， [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 會在拒絕存取時立即停止搜尋。  (如果您未使用 DLL 重新導向， **LoadLibrary** 會略過無法存取的目錄，然後繼續搜尋。 ) 

最好的作法是在包含應用程式的相同目錄中安裝應用程式 Dll，即使您不是使用 DLL 重新導向也是一樣。 這可確保安裝應用程式不會覆寫 DLL 的其他複本，並導致其他應用程式失敗。 此外，如果您遵循這項良好的做法，其他應用程式不會覆寫您的 DLL 複本，並導致您的應用程式失敗。

 

 
