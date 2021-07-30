---
description: 應用程式可以藉由指定完整路徑或使用其他機制（例如資訊清單），來控制載入 DLL 的位置。 如果未使用這些方法，系統會在載入時搜尋 DLL，如本主題中所述。
ms.assetid: 44228cf2-6306-466c-8f16-f513cd3ba8b5
title: Dynamic-Link 程式庫搜尋順序
ms.topic: article
ms.date: 09/11/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 73c90e176983aa542ec524c2bfa32623821c2f21
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991835"
---
# <a name="dynamic-link-library-search-order"></a>Dynamic-Link 程式庫搜尋順序

系統可以將相同動態連結程式庫的多個版本包含 (DLL) 。 應用程式可以藉由指定完整路徑或使用其他機制（例如資訊清單），來控制載入 DLL 的位置。 如果未使用這些方法，系統會在載入時搜尋 DLL，如本主題中所述。

-   [影響搜尋的因素](#factors-that-affect-searching)
-   [UWP 應用程式的搜尋順序](#search-order-for-uwp-apps)
    -   [UWP 應用程式的標準搜尋順序](#standard-search-order-for-uwp-apps)
    -   [UWP 應用程式的替代搜尋順序](#alternate-search-order-for-uwp-apps)
-   [桌面應用程式的搜尋順序](#search-order-for-desktop-applications)
    -   [桌面應用程式的標準搜尋順序](#standard-search-order-for-desktop-applications)
    -   [桌面應用程式的替代搜尋順序](#alternate-search-order-for-desktop-applications)
    -   [使用載入連結 **\_ 庫 \_ 搜尋** 旗標搜尋順序](#search-order-using-load_library_search-flags)
-   [相關主題](#related-topics)

## <a name="factors-that-affect-searching"></a>影響搜尋的因素

下列因素會影響系統是否搜尋 DLL：

-   如果已在記憶體中載入具有相同模組名稱的 DLL，則系統只會檢查重新導向和資訊清單，然後再解析成載入的 DLL，而不論其所在的目錄為何。 系統不會搜尋 DLL。
-   如果 dll 是在執行應用程式之 Windows 版本的已知 dll 清單上，則系統會使用其已知 dll (和已知 dll 的相依 dll 的複本（如果有) 的話），而不是搜尋 DLL。 如需目前系統上已知 Dll 的清單，請參閱下列登錄機碼： **HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLLs**。
-   如果 DLL 具有相依性，系統就會搜尋相依的 Dll，如同它們是以其模組名稱載入一樣。 即使是藉由指定完整路徑來載入第一個 DLL，也是如此。

## <a name="search-order-for-uwp-apps"></a>UWP 應用程式的搜尋順序

當 Windows 10 (的 UWP 應用程式或適用于 Windows 8 的商店應用程式) 透過呼叫 [**>loadpackagedlibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)函式來載入封裝的模組時，DLL 必須在進程的封裝相依性圖形中。 如需詳細資訊，請參閱 **>loadpackagedlibrary**。 當 UWP 應用程式以其他方式載入模組，但未指定完整路徑時，系統會在載入時搜尋 DLL 和其相依性，如本節所述。

在系統搜尋 DLL 之前，它會檢查下列各項：

-   如果已在記憶體中載入具有相同模組名稱的 DLL，系統就會使用載入的 DLL，而不論其所在的目錄為何。 系統不會搜尋 DLL。
-   如果 dll 是在執行應用程式之 Windows 版本的已知 dll 清單上，則系統會使用其已知 dll 的複本 (以及已知 dll 的相依 dll （如果有任何) ）。 系統不會搜尋 DLL。 如需目前系統上已知 Dll 的清單，請參閱下列登錄機碼： **HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLLs**。

如果系統必須搜尋模組或其相依性，即使相依性不是 UWP 應用程式程式碼，它一律會使用 UWP 應用程式的搜尋順序。

### <a name="standard-search-order-for-uwp-apps"></a>UWP 應用程式的標準搜尋順序

如果模組尚未載入或在已知 Dll 的清單上，系統會依下列順序搜尋這些位置：

1.  進程的封裝相依性圖形。 這是應用程式的套件，以及 `<PackageDependency>` 在 `<Dependencies>` 應用程式套件資訊清單區段中指定的任何相依性。 系統會依資訊清單中出現的順序來搜尋相依性。
2.  從中載入呼叫進程的目錄。
3.  系統目錄 (% SystemRoot% \\ system32) 。

如果 DLL 具有相依性，系統就會搜尋相依的 Dll，如同它們是以其模組名稱載入一樣。 即使是藉由指定完整路徑來載入第一個 DLL，也是如此。

### <a name="alternate-search-order-for-uwp-apps"></a>UWP 應用程式的替代搜尋順序

如果模組變更標準搜尋順序，方法是使用已 **\_ \_ 改變 \_ 搜尋 \_ 路徑的載入** 來呼叫 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)函式，系統會在目錄中搜尋指定模組的載入來原始目錄，而不是呼叫進程的目錄。 系統會依下列順序搜尋這些位置：

1.  進程的封裝相依性圖形。 這是應用程式的套件，以及 `<PackageDependency>` 在 `<Dependencies>` 應用程式套件資訊清單區段中指定的任何相依性。 系統會依資訊清單中出現的順序來搜尋相依性。
2.  從中載入指定模組的目錄。
3.  系統目錄 (% SystemRoot% \\ system32) 。

## <a name="search-order-for-desktop-applications"></a>桌面應用程式的搜尋順序

桌面應用程式可以藉由指定完整路徑、使用 [DLL](dynamic-link-library-redirection.md)重新導向或使用 [資訊清單](/windows/desktop/SbsCs/manifests)，來控制載入 DLL 的位置。 如果未使用這些方法，系統會在載入時搜尋 DLL，如本節所述。

在系統搜尋 DLL 之前，它會檢查下列各項：

-   如果已在記憶體中載入具有相同模組名稱的 DLL，系統就會使用載入的 DLL，而不論其所在的目錄為何。 系統不會搜尋 DLL。
-   如果 dll 是在執行應用程式之 Windows 版本的已知 dll 清單上，則系統會使用其已知 dll 的複本 (以及已知 dll 的相依 dll （如果有任何) ）。 系統不會搜尋 DLL。 如需目前系統上已知 Dll 的清單，請參閱下列登錄機碼： **HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLLs**。

如果 DLL 具有相依性，系統就會搜尋相依的 Dll，如同它們是以其模組名稱載入一樣。 即使是藉由指定完整路徑來載入第一個 DLL，也是如此。

> [!IMPORTANT]
> 如果攻擊者取得所搜尋之其中一個目錄的控制權，就可以在該目錄中放置 DLL 的惡意複本。 如需協助防止這類攻擊的方法，請參閱 [動態連結程式庫安全性](dynamic-link-library-security.md)。

### <a name="standard-search-order-for-desktop-applications"></a>桌面應用程式的標準搜尋順序

系統所使用的標準 DLL 搜尋順序取決於是否啟用或停用安全 DLL 搜尋模式。 保管庫DLL 搜尋模式會將使用者的目前目錄放在搜尋順序的後面。

保管庫預設會啟用 DLL 搜尋模式。 若要停用此功能，請建立 **HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Session Manager** \\ **SafeDllSearchMode** 登錄值，並將它設定為0。 呼叫 [**SetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-setdlldirectorya) 函式會在指定目錄位於搜尋路徑中時，有效地停用 **SafeDllSearchMode** ，並變更搜尋順序，如本主題中所述。

如果已啟用 **SafeDllSearchMode** ，則搜尋順序如下所示：

1.  應用程式載入的來原始目錄。
2.  系統目錄。 使用 [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) 函式來取得此目錄的路徑。
3.  16位系統目錄。 沒有可取得此目錄路徑的函式，但會進行搜尋。
4.  Windows 目錄。 使用 [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) 函式來取得此目錄的路徑。
5.  目前的目錄。
6.  PATH 環境變數中所列的目錄。 請注意，這不包括 **應用程式路徑** 登錄機碼所指定的每個應用程式路徑。 計算 DLL 搜尋路徑時，不會使用 **應用程式路徑** 索引鍵。

如果 **SafeDllSearchMode** 已停用，則搜尋順序如下所示：

1.  應用程式載入的來原始目錄。
2.  目前的目錄。
3.  系統目錄。 使用 [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) 函式來取得此目錄的路徑。
4.  16位系統目錄。 沒有可取得此目錄路徑的函式，但會進行搜尋。
5.  Windows 目錄。 使用 [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) 函式來取得此目錄的路徑。
6.  PATH 環境變數中所列的目錄。 請注意，這不包括 **應用程式路徑** 登錄機碼所指定的每個應用程式路徑。 計算 DLL 搜尋路徑時，不會使用 **應用程式路徑** 索引鍵。

### <a name="alternate-search-order-for-desktop-applications"></a>桌面應用程式的替代搜尋順序

藉由呼叫 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函式與 **\_ 具有 \_ 改變 \_ 搜尋 \_ 路徑的載入**，即可變更系統所使用的標準搜尋順序。 您也可以藉由呼叫 [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) 函數來變更標準搜尋順序。

> [!NOTE]
> 進程的標準搜尋順序也會受到影響，方法是在目前進程開始之前，先在父進程中呼叫 [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) 函數。

如果您指定替代的搜尋策略，其行為會持續，直到所有相關聯的可執行檔模組都已找到為止。 系統開始處理 DLL 初始化常式之後，系統會還原為標準搜尋策略。

如果呼叫指定 **\_ 具有 \_ 改變 \_ 搜尋 \_ 路徑的載入**，而 *LpFileName* 參數指定絕對路徑，則 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)函式支援替代搜尋順序。

請注意，標準搜尋策略和 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 所指定的其他搜尋策略，與具有 **改變之 \_ \_ \_ 搜尋 \_ 路徑的負載有** 不同之處：標準搜尋開始于呼叫應用程式的目錄中，而替代搜尋則是在 **LoadLibraryEx** 載入的可執行模組的目錄中開始。

如果已啟用 **SafeDllSearchMode** ，則替代搜尋順序如下所示：

1.  *LpFileName* 所指定的目錄。
2.  系統目錄。 使用 [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) 函式來取得此目錄的路徑。
3.  16位系統目錄。 沒有可取得此目錄路徑的函式，但會進行搜尋。
4.  Windows 目錄。 使用 [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) 函式來取得此目錄的路徑。
5.  目前的目錄。
6.  PATH 環境變數中所列的目錄。 請注意，這不包括 **應用程式路徑** 登錄機碼所指定的每個應用程式路徑。 計算 DLL 搜尋路徑時，不會使用 **應用程式路徑** 索引鍵。

如果 **SafeDllSearchMode** 已停用，則替代搜尋順序如下所示：

1.  *LpFileName* 所指定的目錄。
2.  目前的目錄。
3.  系統目錄。 使用 [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) 函式來取得此目錄的路徑。
4.  16位系統目錄。 沒有可取得此目錄路徑的函式，但會進行搜尋。
5.  Windows 目錄。 使用 [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) 函式來取得此目錄的路徑。
6.  PATH 環境變數中所列的目錄。 請注意，這不包括 **應用程式路徑** 登錄機碼所指定的每個應用程式路徑。 計算 DLL 搜尋路徑時，不會使用 **應用程式路徑** 索引鍵。

如果 *lpPathName* 參數指定路徑， [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)函式支援替代搜尋順序。 替代搜尋順序如下所示：

1.  應用程式載入的來原始目錄。
2.  [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)的 *lpPathName* 參數所指定的目錄。
3.  系統目錄。 使用 [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) 函式來取得此目錄的路徑。 此目錄的名稱為 System32。
4.  16位系統目錄。 沒有可取得此目錄路徑的函式，但會進行搜尋。 此目錄的名稱為 System。
5.  Windows 目錄。 使用 [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) 函式來取得此目錄的路徑。
6.  PATH 環境變數中所列的目錄。 請注意，這不包括 **應用程式路徑** 登錄機碼所指定的每個應用程式路徑。 計算 DLL 搜尋路徑時，不會使用 **應用程式路徑** 索引鍵。

如果 *lpPathName* 參數是空字串，則呼叫會從搜尋順序中移除目前的目錄。

當指定的目錄在搜尋路徑中時， [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)會有效地停用安全 DLL 搜尋模式。 若要根據 **SafeDllSearchMode** 登錄值還原安全的 DLL 搜尋模式，並將目前的目錄還原到搜尋順序，請以 *lpPathName* 為 Null 來呼叫 **SetDllDirectory** 。

### <a name="search-order-using-load_library_search-flags"></a>使用載入連結 **\_ 庫 \_ 搜尋** 旗標搜尋順序

應用程式可以使用一或多個 **載入連結 \_ 庫 \_ 搜尋** 旗標搭配 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函式來指定搜尋順序。 應用程式也可以使用 **載入連結 \_ 庫 \_ 搜尋** 旗標搭配 [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) 函式來建立進程的 DLL 搜尋順序。 應用程式可以使用 [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) 或 [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) 函式，指定進程 DLL 搜尋順序的其他目錄。

搜尋的目錄取決於使用 [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)所指定的旗標。 如果使用一個以上的旗標，則會以下列順序搜尋對應的目錄：

1.  包含 DLL (**載入連結 \_ 庫 \_ 搜尋 \_ dll \_ 載入 \_ 目錄**) 的目錄。 此目錄只會搜尋要載入之 DLL 的相依性。
2.  應用程式目錄 (**載入連結 \_ 庫 \_ 搜尋 \_ 應用程式 \_** 目錄) 。
3.  使用 [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) 函式明確新增的路徑 (**載入連結 \_ 庫 \_ 搜尋 \_ 使用者 \_ 目錄**) 或 [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) 函數。 如果新增了一個以上的路徑，則不會指定搜尋路徑的順序。
4.  系統目錄 (**載入連結 \_ 庫 \_ 搜尋 \_ SYSTEM32**) 。

如果應用程式未使用任何 **載入連結 \_ 庫 \_ 搜尋** 旗標來呼叫 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) ，或建立進程的 dll 搜尋順序，系統會使用標準搜尋順序或替代搜尋順序來搜尋 dll。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)
</dt> <dt>

[應用程式註冊](/windows/desktop/shell/app-registration)
</dt> <dt>

[動態連結程式庫重新導向](dynamic-link-library-redirection.md)
</dt> <dt>

[動態連結程式庫安全性](dynamic-link-library-security.md)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
</dt> <dt>

[**>loadpackagedlibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)
</dt> <dt>

[**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)
</dt> <dt>

[**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)
</dt> <dt>

[並存元件](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)
</dt> </dl>

 

 
