---
description: 僅限64位
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: 僅限64位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d896fcaf4b8c4ebeadf7cfd5a5c22e511cb659
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088806"
---
# <a name="64-bit-only"></a>僅限64位

## <a name="affected-platforms"></a>受影響的平臺

**伺服器** -Windows Server 2008 R2  



## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -高  






## <a name="description"></a>Description

Windows Server 2008 R2 僅隨附64位 SKU;伺服器版本的作業系統沒有32位 SKU 可用。 不過，Windows 7 用戶端仍可繼續使用32位 SKU。

## <a name="manifestation-of-impact"></a>影響的表現

這會影響三個區域：

-   32位驅動程式
-   32位外掛程式
-   16位可執行檔

## <a name="solution-for-32-bit-drivers"></a>32位驅動程式的解決方案

將32位驅動程式重新編譯為帶正負號的64位驅動程式。

## <a name="solution-for-32-bit-plug-ins"></a>32位外掛程式的解決方案

WoW64 是 x86 模擬器，可讓32位的 Windows 應用程式順暢地在64位 Windows 上執行。 WoW64 現在是選用的功能，如果需要執行32位程式碼，則必須安裝此功能。

系統會隔離32位應用程式與64位應用程式，其中包括防止檔案和登錄衝突。 支援主控台、GUI 及服務應用程式。 系統會為剪下和貼上和 COM 等案例提供32/64 界限之間的互通性。 但是，32位進程無法載入64位的 Dll，而64位進程無法載入32位 Dll。 在針對 Windows 檔案總管所撰寫的 shell 外掛程式中，我們通常會看到這種情況。

32位應用程式可以藉由呼叫 IsWow64Process 函式，來偵測它是否正在 WOW64 下執行。 應用程式可以使用 GetNativeSystemInfo 函式來取得處理器的其他相關資訊

請注意，64位 Windows 不支援執行以16位 Windows 為基礎的應用程式。 主要原因是控制碼在64位的 Windows 上具有32的有效位。 因此，無法將控制碼截斷並傳遞至16位應用程式，而不會遺失資料。 嘗試啟動16位應用程式失敗，並出現下列錯誤：錯誤 \_ 的 \_ EXE \_ 格式錯誤。

## <a name="solution-for-16-bit-executables"></a>16位可執行檔的解決方案

64位 Windows 會辨識有限數量的特定16位安裝程式，並替代已移植的32位版本。 替代清單會儲存在登錄中的下列機碼底下： HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion NtVdm64 內 \\ 建支援數個安裝程式引擎，包括 InstallShield 5.x 安裝程式。 請注意，64位的 Windows Installer 可以在64位的 Windows 上順暢地安裝32位的 MSI 應用程式。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [執行32位應用程式](/windows/desktop/WinProg64/running-32-bit-applications)
-   [效能和記憶體耗用量](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [WOW64 執行詳細資料](/windows/desktop/WinProg64/wow64-implementation-details)
-   [登錄重新導向程式](/windows/desktop/WinProg64/registry-redirector)
-   [檔案系統重新導向程式](/windows/desktop/WinProg64/file-system-redirector)
-   [記憶體管理](/windows/desktop/WinProg64/memory-management)
-   [處理器相似性](/windows/desktop/WinProg64/processor-affinity)
-   [處理序間通訊](/windows/desktop/WinProg64/interprocess-communication)
-   [64位系統上的應用程式安裝](/windows/desktop/WinProg64/application-installation)
-   [調試 WOW64](/windows/desktop/WinProg64/debugging-wow64)
-   [**IsWow64Process 函式**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [**GetNativeSystemInfo 函式**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
