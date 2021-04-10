---
description: 版本 API 協助程式函式是用來判斷目前正在執行的作業系統版本。 如需詳細資訊，請參閱取得系統版本。
ms.assetid: 1a70b1d9-ed66-4201-9921-4e26e4001020
title: 作業系統版本
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: 73eb9a81880f29f9292713af46c5c79a7e9eb2de
ms.sourcegitcommit: 7ea69db68bca2b1592802e676ada8432a2583410
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/17/2020
ms.locfileid: "104024275"
---
# <a name="operating-system-version"></a>作業系統版本

[版本 API](version-helper-apis.md)協助程式函式是用來判斷目前正在執行的作業系統版本。 如需詳細資訊，請參閱 [取得系統版本](getting-the-system-version.md)。

下表摘要說明最新的作業系統版本號碼。

| 作業系統 | 版本號碼 |
|------------------|----------------|
| Windows 10       | 10.0\*         |
| Windows Server 2019 | 10.0\*      |
| Windows Server 2016 | 10.0\*      |
| Windows 8.1      | 6.3\*          |
| Windows Server 2012 R2 | 6.3\*    |
| Windows 8        | 6.2            |
| Windows Server 2012 | 6.2         |
| Windows 7        | 6.1            |
| Windows Server 2008 R2 | 6.1      |
| Windows Server 2008 | 6.0         |
| Windows Vista    | 6.0            |
| Windows Server 2003 R2 | 5.2      |
| Windows Server 2003 | 5.2         |
| Windows XP 64 位版本 | 5.2   |
| Windows XP | 5.1                  |
| Windows 2000     | 5.0            |

**\*** 適用于已針對 Windows 8.1 或 Windows 10 所列入的應用程式。 未針對 Windows 8.1 或 Windows 10 所找出的應用程式將會傳回 Windows 8 的 OS 版本值 (6.2) 。 若要將您的應用程式 Windows 8.1 或 Windows 10 的資訊清單，請參閱以 [Windows 的應用程式為目標](targeting-your-application-at-windows-8-1.md)。<br/>

識別目前的作業系統，通常並不是判斷特定作業系統功能是否存在的最佳方式。 這是因為作業系統可能已在可轉散發 DLL 中新增新功能。 您可以測試功能本身是否存在，而不是使用 [版本 API](version-helper-apis.md) 協助程式函式來判斷作業系統平臺或版本號碼。

若要判斷測試功能的最佳方式，請參閱感興趣之功能的檔。 下列清單討論功能偵測的一些常見技術：

- 您可以測試與功能相關聯的函式是否存在。 若要測試是否有系統 DLL 中的函式，請呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式以載入 DLL。 然後呼叫 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，判斷是否有感興趣的函式存在於 DLL 中。 使用 **GetProcAddress** 傳回的指標來呼叫函數。 請注意，即使函式存在，也可能是只傳回錯誤碼（例如錯誤 \_ 呼叫未執行）的存根 \_ \_ 。
- 您可以使用 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 函式來判斷某些功能是否存在。 例如，您可以藉由呼叫 **GetSystemMetrics** (SM CMONITORS) 來偵測多個顯示監視器 \_ 。
- 有數個版本的可轉散發 Dll 可執行 shell 和通用控制項功能。 如需判斷您的應用程式執行所在的系統上有哪些版本的相關資訊，請參閱 [Shell 和通用控制項版本](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85))主題。

如果您必須要求特定的作業系統，請務必使用它做為最低支援版本，而不是設計一個作業系統的測試。 如此一來，您的偵測程式碼將繼續在未來的 Windows 版本上運作。

請注意，32位應用程式可以藉由呼叫 [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) 函式，來偵測它是否正在 WOW64 下執行。 它可以藉由呼叫 [**GetNativeSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) 函數來取得額外的處理器資訊。

如需詳細資訊，請參閱 [Windows 10 版本資訊](/windows/release-information/) 和 [Windows 生命週期事實表](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)。

