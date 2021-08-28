---
title: 執行32位應用程式
description: 使用 WOW64 x86 模擬器在64位 Windows 上順暢地執行32以 Windows 為基礎的應用程式。 同時瞭解登錄 director、檔案系統重新導向器、64位系統上的應用程式安裝，以及偵錯工具。
ms.assetid: ac75c5af-86e8-4282-9a8e-8db3c22cbda0
keywords:
- WOW64 64 位 Windows 程式設計
- WOW64 64 位 Windows 程式設計，關於
- 64位上的32位應用程式 Windows 64 位 Windows 程式設計
- 64位 Windows 程式設計手冊64位 Windows 程式設計，wow64 請參閱 wow64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1da192f4109afe09133f036d5fff88e772bbcc2c7d20ceb456e3233ab2b60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132821"
---
# <a name="running-32-bit-applications"></a>執行32位應用程式

WOW64 是 x86 模擬器，可讓以32位 Windows 為基礎的應用程式順暢地在64位 Windows 上執行。 如此一來，就能讓32位 (x86) Windows 應用程式順暢地在64位 (x64) Windows 中執行，以及32位 (x86) 和32位 (ARM) Windows (的應用程式可在 64) Windows ARM64 中順暢地執行。 WOW64 是隨作業系統提供，不需要明確啟用。 如需詳細資訊，請參閱 [WOW64 執行詳細資料](wow64-implementation-details.md)。

系統會隔離32位應用程式與64位應用程式，其中包括防止檔案和登錄衝突。 支援主控台、GUI 及服務應用程式。 系統會為剪下和貼上和 COM 等案例提供32/64 界限之間的互通性。 但是，32位進程無法載入64位 Dll 來執行，而且64位進程無法載入32位 Dll 來執行。 此限制不適用於載入為資料檔案或映射資源檔的 Dll;如需詳細資訊，請參閱 [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa)。

32位應用程式可以藉由呼叫 [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)函式來偵測它是否在 WOW64 下執行， (在以 Windows 10) 為目標時使用 [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) 。 應用程式可以使用 [**GetNativeSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) 函式來取得處理器的其他相關資訊。

請注意，64位 Windows 不支援執行以16位 Windows 為基礎的應用程式。 主要原因是控制碼在64位 Windows 上具有32的有效位。 因此，無法將控制碼截斷並傳遞至16位應用程式，而不會遺失資料。 嘗試啟動16位應用程式失敗，並出現下列錯誤： **錯誤 \_ 的 \_ EXE \_ 格式錯誤**。

## <a name="in-this-section"></a>本章節內容

-   [WOW64 下的效能和記憶體耗用量](performance-and-memory-consumption.md)
-   [WOW64 執行詳細資料](wow64-implementation-details.md)
-   [登錄重新導向程式](registry-redirector.md)
-   [檔案系統重新導向程式](file-system-redirector.md)
-   [記憶體管理](memory-management.md)
-   [處理器相似性](processor-affinity.md)
-   [處理序間通訊](interprocess-communication.md)
-   [應用程式安裝](application-installation.md)
-   [調試 WOW64](debugging-wow64.md)

 

 