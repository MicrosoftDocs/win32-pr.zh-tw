---
title: 64位考慮
description: 隨著64位 Windows 的可用性增加，使用者預期的輸入方法（例如各種語言的國際鍵盤或輸入法編輯器） (Ime) 東亞語言，以符合32位和64位的應用程式。
ms.assetid: 6a99ad45-202c-4fbb-9707-341bc9fde21e
keywords:
- 文字服務架構 (TSF) 、64位 Windows
- TSF (文字服務架構) ，64位 Windows
- 文字服務，64位 Windows
- 64 位元 Windows
- '文字服務架構 (TSF) 、輸入法編輯器 (IME) '
- 'TSF (文字服務架構) ，輸入法編輯器 (IME) '
- '文字服務、輸入法編輯器 (IME) '
- 輸入法 (IME)
- '輸入法 (輸入法編輯器) '
- 文字服務架構 (TSF) ，國際鍵盤
- TSF (文字服務架構) ，國際鍵盤
- 文字服務，國際鍵盤
- 國際鍵盤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045ec699c7a433f15b92467e3072d30acbf01936
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375645"
---
# <a name="64-bit-considerations"></a>64位考慮

隨著64位 Windows 的可用性增加，使用者預期的輸入方法（例如各種語言的國際鍵盤或輸入法編輯器） (Ime) 東亞語言，以符合32位和64位的應用程式。 開發 Microsoft Windows 的輸入方法元件或文字服務時，請務必將64位 Windows 視為產品的潛在目標平臺。

因為以文字服務架構) 為基礎的 Ime 和文字服務 (通常會實作為動態連結程式庫 (Dll) ，所以請務必注意，Dll 是專門針對32位環境或64位環境中的使用而建立的，64位應用程式不能使用針對32位環境所建立的 DLL，反之亦然。

> [!Note]  
> WOW64 無法減少此位特定的 DLL 限制。 如需 WOW64 的詳細資訊，請參閱執行 [32 位應用程式](/windows/desktop/WinProg64/running-32-bit-applications)。

 

本主題將討論在64位 Windows 上開發 Ime 和文字服務的重要設計考慮。

## <a name="64-bit-considerations-for-imes"></a>64位的 Ime 考慮

本章節說明建立與64位 Windows 搭配使用之 Ime 時所牽涉到的特殊考慮。 如需有關輸入法的詳細資訊，請參閱 [輸入法編輯器](/previous-versions/windows/desktop/dnacc/input-method-editor-and-text-services-framework-accessibility)。

## <a name="building-32-bit-and-64-bit-versions-of-an-ime"></a>建立 IME 的32位和64位版本

由於先前提及 Dll 的32位/64 位相容性問題，因此必須採取一些預防措施，以確保在64位 Windows 上執行的任何應用程式 (32 位或64位) 都能以透明的方式運作。 針對64位平臺上的32位和64位應用程式，讓您的 IME 能以透明方式運作的建議解決方案，是建立並安裝平行的32位和64位版本的 IME DLL。 一般來說，開發人員會藉由調整其組建環境中的目標平臺設定，從單一來源建立平行 Dll。 如需有關單一來源的32位和64位應用程式的詳細資訊，請參閱 [準備取得64位 Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows)。

## <a name="side-by-side-installation-of-64-bit-and-32-bit-input-method-editors"></a>64位和32位輸入方法編輯器的並存安裝

Ime 和文字服務的開發人員應該留意本主題中所述的64位考慮。 幸運的是，這些服務的使用者不需要擔心這些執行特定的詳細資料。 64位 Windows 的一項功能是能夠隱藏使用者的64位和32位特定版本的 IME Dll 需求。 當兩個版本的 IME 都正確地以並存方式安裝時，64位的 Windows 會辨識 IME 的64位和32位版本是否存在，並將這些位特定的 Ime 呈現給終端使用者，作為單一 *邏輯* IME。 當使用者需要使用 IME 時，64位的 Windows 會明確地選擇 (32 位或64位) 的輸入法版本，適用于指定的情況。

若要讓64位和32位 Ime 的並存安裝正常運作 (也就是，若要將兩個平臺特定的 Dll 表示為使用者) 的單一邏輯 IME，必須符合下列條件：

-   開發人員必須建立一個適用于32位 Windows 的平臺特定 (版本，以及一個適用于64位 Windows) 的 IME DLL。
-   32位和64位 Dll 必須共用相同的檔案名。
-   必須遵循安裝目錄需求。 如需詳細資訊，請參閱安裝目錄需求。

32位和64位 IME Dll 的並存安裝會共用相同的登錄機碼來儲存設定資料 (包括 DLL 檔案名) ：


```C++
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts
```



[**ImmInstallIME**](/windows/desktop/api/imm/nf-imm-imminstallimea)函式是用來建立此登錄機碼。 IME 的安裝程式和安裝程式必須呼叫此函式，才能將 IME 註冊為支援的鍵盤配置。 **ImmInstallIME** 函式應該只呼叫一次，不論是從32位或64位版本的 IME DLL。

## <a name="mismatched-ime-dlls"></a>不相符的 IME Dll

建議您在64位 Windows 上只安裝32位版本的輸入法，也不會受到支援。 如果64位應用程式嘗試載入32位的輸入法，則當應用程式嘗試載入相關聯的鍵盤配置時，IME 會無訊息地失敗。

> [!IMPORTANT]
>
> 當發生64位應用程式/32 位的輸入法衝突錯誤時，不會顯示警告對話方塊或訊息。

 

適用于文字服務的64位考慮

本節說明在64位環境中建立文字服務時所牽涉到的特殊考慮。 如需文字服務和文字服務架構的詳細資訊，請參閱 [文字服務架構](text-services-framework.md)。

## <a name="building-32-bit-and-64-bit-text-services"></a>建立32位和64位文字服務

文字服務會實作為元件物件模型， (在 DLL 上公開的 COM) 物件。 因此，在64位 Windows 上安裝的文字服務可能會發生32位/64 位 DLL 衝突。 就像使用 Ime 一樣，可讓您的文字服務在64位平臺上以透明的方式與32位和64位應用程式一起運作的建議解決方案，是建立並安裝平行的32位和64位版本的文字服務 DLL。

## <a name="side-by-side-installation-of-64-bit-and-32-bit-text-services"></a>64位和32位文字服務的並存安裝

若要將32位版本和64位版本的文字服務並行安裝，並以單一的邏輯文字服務的形式呈現給使用者，必須符合下列條件：

-   這兩個版本的文字服務會在向 COM 子系統註冊 (CLSID) 時，指定相同的類別識別碼。
-   這兩個版本的文字服務都是獨立註冊的。 如需詳細資訊，請參閱 [註冊 COM 應用程式](/windows/desktop/com/registering-com-applications)。

當32位文字服務向64位 Windows 註冊時，註冊作業會以透明方式重新導向至下列登錄機碼：


```C++
HKEY_CLASS_ROOT\Wow6432Node\CLSID
```



[登錄重新導向程式](/windows/desktop/WinProg64/registry-redirector)


```C++
HKEY_LOCAL_MACHINE\Software\Microsoft\CTF\TIP
```



[ITfInputProcessorProfiles](/windows/desktop/api/Msctf/nn-msctf-itfinputprocessorprofiles)[文字服務註冊](text-service-registration.md)

64位版本和32位版本的文字服務可能會同時使用。 在兩個版本的文字服務都需要操作任何共用物件的情況下，應該將存取共用物件的協調設計成文字服務。 每個文字服務都負責管理任何已使用或需要的共用物件。

## <a name="installing-only-32-bit-text-services-on-64-bit-windows"></a>在64位 Windows 上僅安裝32位文字服務

不建議在64位 Windows 平臺上安裝32位版本的文字服務，也不會受到建議。 由於註冊對應是在64位 Windows 平臺上完成，因此64位應用程式可以透過 **ITfInputProcessorProfiles** 介面列舉32位文字服務的服務。 不過，如果64位應用程式嘗試載入32位文字服務，則載入會無訊息地失敗。

> [!IMPORTANT]
>
> 當發生64位應用程式/32 位文字服務衝突錯誤時，不會顯示警告對話方塊或訊息。

 

其他考量

## <a name="installation-directory-requirements"></a>安裝目錄需求

本節說明如何安裝 IME 和 text service 二進位檔案的需求。 如果未遵循這些需求，您的文字服務或 IME 可能無法正常運作。

**IME Dll**

在64位的 Windows 平臺上，將32位和64位的 IME Dll 安裝在下列目錄中：

-   在 SysWOW64 系統目錄中安裝32位的 IME Dll;呼叫 [**GetSystemWow64Directory**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya)，或使用 **CSIDL \_ SYSTEMX86** [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) ，以取得此目錄路徑。 或者，如果您使用 [Windows Installer](/windows/desktop/Msi/about-windows-installer)，請使用 [**SystemFolder**](/windows/desktop/Msi/systemfolder) 屬性。
-   在 System32 系統目錄中安裝64位的 IME Dll;呼叫 [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)或 **SHGetFolderPath** 與 [CSIDL \_ 系統](/windows/desktop/shell/csidl) ，以取得此目錄路徑。 或者，針對 Windows Installer，請使用 [**System64Folder**](/windows/desktop/Msi/system64folder) 屬性。

**文字服務 Dll 和相關二進位檔案**

在64位 Windows 平臺上，請在下列目錄中安裝32位和64位文字服務 Dll，以及與您的文字服務或 IME 相關的任何其他二進位檔案：

-   將32位文字服務 Dll 和任何其他32位二進位檔安裝在 Program Files (x86) 目錄的子目錄;使用 **CSIDL \_ PROGRAM \_ FILESX86** 呼叫 **SHGetFolderPath** ，以取得此目錄路徑。 或者，針對 Windows Installer，請使用 [**ProgramFilesFolder**](/windows/desktop/Msi/programfilesfolder) 屬性。
-   在 Program Files 目錄下的子目錄中，安裝64位文字服務 Dll 和任何其他64位二進位檔案;使用 **CSIDL \_ PROGRAM \_ FILES** 呼叫 **SHGetFolderPath** ，以抓取此目錄路徑。 或者，針對 Windows Installer，請使用 [**ProgramFiles64Folder**](/windows/desktop/Msi/programfiles64folder) 屬性。

如果您不是使用 Windows Installer 套件來安裝 IME 或文字服務，則強烈 recommnded 您使用64位安裝應用程式。 WOW64 檔案系統重新導向器可能會導致32位安裝程式將檔案放在錯誤的目錄中 (例如，WOW64 檔案系統重新導向可能會導致要將 System32 目錄的檔案安裝在 SysWOW64 目錄中，而不是) 。 如果您必須使用32位的安裝程式，請在安裝程式期間停用 WOW64 檔案重新導向，以確保檔案重新導向程式服務不會在安裝過程中造成任何非預期的重新導向。 如需 WOW64 檔案系統重新導向器的詳細資訊，請參閱 [檔案系統重定向](/windows/desktop/WinProg64/file-system-redirector)程式。 如需有關如何停用或啟用 WOW64 檔案系統重新導向的詳細資訊，請參閱 [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)。

> [!TIP]
>
> 避免硬式編碼的安裝路徑。 如需詳細資訊，請參閱 [使用未 Hard-Coded 路徑的應用程式設計介面尋找目錄](/previous-versions//ms675638(v=vs.85))

 

> [!IMPORTANT]
>
> 請勿將任何 IME 或文字服務檔案安裝在特殊目錄% WINDIR% \\ IME (預設為 c： \\ Windows \\ IME ) 。 此目錄包含支援文字服務和 Ime 的系統檔案;它不是用來包含任何協力廠商的 IME 或文字服務檔案，而且此目錄不支援 WOW64 檔案系統重新導向。

 

## <a name="dual-ctfmonexe-processes-run-on-64-bit-windows-platforms"></a>在64位 Windows 平臺上執行的雙重 Ctfmon.exe 進程

ctfmon.exe 進程會管理桌面上的文字服務架構，也提供 (UI) 的語言列使用者介面。 在64位的 Windows 上，ctfmon.exe 進程的32位版本和64位版本會同時執行。 64位的 ctfmon.exe 進程會管理64位文字服務，同樣地，32位 ctfmon.exe 進程會管理32位文字服務。

## <a name="display-behavior-for-different-versions-of-the-language-bar-ui"></a>不同版本的語言列 UI 顯示行為

在64位的 Windows 上，只會顯示與64位版本的文字服務相關聯的語言 bar UI。 在32位應用程式使用32位版本的文字服務的情況下，64位的 Windows 會自動為對等的64位文字服務插入語言列 UI。 這可確保32位文字服務不需要任何特殊的工作就會出現在64位版本的語言列中。

## <a name="control-panel-considerations-on-64-bit-windows"></a>64位 Windows 上的主控台考慮

64位 Windows 可讓您透過主控台存取32位和64位版本的文字服務和 Ime。 若要存取特定版本的文字服務或 Ime 主控台設定，請查看下列位置。

-   **32 位文字服務和 ime 的主控台存取：** 開始 > 設定-> 主控台-> 觀看 x86 主控台圖示
-   **64 位文字服務和 ime 的主控台存取：** 開始 > 設定-> 主控台-> 地區及語言選項

在某些情況下，某些設定可能只會透過32位主控台提供。 在這些情況下，請在您的64位設定介面中提供適當的檔或提供 UI 提示，以確定文字服務或 IME 的使用者知道這一點。

 

 