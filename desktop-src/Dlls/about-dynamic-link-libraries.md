---
description: 動態連結可讓模組只包含在載入時間或執行時間尋找匯出的 DLL 函式所需的資訊。
ms.assetid: df2a8e4c-7ad0-46ea-9643-1528a9ea1503
title: 關於 Dynamic-Link 程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62e6a6a23315e915bd4a5a7fe6e2dcb54a9a2ebfbd66bf5d4ba7a2519a04576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815907"
---
# <a name="about-dynamic-link-libraries"></a>關於 Dynamic-Link 程式庫

動態連結可讓模組只包含在載入時間或執行時間尋找匯出的 DLL 函式所需的資訊。 動態連結不同于較熟悉的靜態連結，連結器會將程式庫函式的程式碼複製到呼叫它的每個模組。

## <a name="types-of-dynamic-linking"></a>動態連結的類型

有兩種方法可以在 DLL 中呼叫函數：

-   在 *載入時間動態連結* 中，模組會對匯出的 DLL 函式發出明確的呼叫，就像它們是區域函數一樣。 這需要您將模組與包含函式之 DLL 的匯入程式庫連結。 匯入程式庫會提供系統載入 DLL 所需的資訊，並在載入應用程式時找出匯出的 DLL 函式。
-   在 *執行時間動態連結* 中，模組會使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函數，在執行時間載入 DLL。 載入 DLL 之後，模組會呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式來取得匯出的 dll 函式的位址。 模組會使用 **GetProcAddress** 傳回的函式指標來呼叫匯出的 DLL 函式。 這樣就不需要匯入程式庫。

## <a name="dlls-and-memory-management"></a>Dll 和記憶體管理

載入 DLL 的每個進程都會將其對應至其虛擬位址空間。 在進程將 DLL 載入其虛擬位址之後，它就可以呼叫匯出的 DLL 函式。

系統會為每個 DLL 維護每個進程的參考計數。 當執行緒載入 DLL 時，參考計數會遞增一。 當進程結束時，或當參考計數變成零 (執行時間動態連結) 時，會從進程的虛擬位址空間卸載 DLL。

如同任何其他函式，匯出的 DLL 函式會在呼叫它的執行緒內容中執行。 因此，下列條件適用：

-   呼叫 DLL 之進程的執行緒可以使用 DLL 函式所開啟的控制碼。 同樣地，呼叫進程的任何執行緒所開啟的控制碼都可以在 DLL 函數中使用。
-   DLL 會使用呼叫執行緒的堆疊，以及呼叫進程的虛擬位址空間。
-   DLL 會從呼叫進程的虛擬位址空間配置記憶體。

如需 Dll 的詳細資訊，請參閱下列主題：

-   [動態連結的優點](advantages-of-dynamic-linking.md)
-   [動態連結程式庫建立](dynamic-link-library-creation.md)
-   [動態連結程式庫 Entry-Point 函式](dynamic-link-library-entry-point-function.md)
-   [載入時間動態連結](load-time-dynamic-linking.md)
-   [執行時間動態連結](run-time-dynamic-linking.md)
-   [動態連結程式庫搜尋順序](dynamic-link-library-search-order.md)
-   [動態連結程式庫資料](dynamic-link-library-data.md)
-   [動態連結程式庫重新導向](dynamic-link-library-redirection.md)
-   [動態連結程式庫更新](dynamic-link-library-updates.md)
-   [動態連結程式庫安全性](dynamic-link-library-security.md)
-   [AppInit Dll 和安全開機](secure-boot-and-appinit-dlls.md)

 

 
