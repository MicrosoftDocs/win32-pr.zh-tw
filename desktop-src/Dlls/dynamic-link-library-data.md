---
description: Dynamic-Link 程式庫 (DLL) 可以包含全域資料或本機資料。
ms.assetid: b1f6811e-c413-4124-9ccb-ea59b7a8a7ff
title: Dynamic-Link 程式庫資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8902eb6388624d958c7176a14b8893f8e2245ddd9370f6ba2ac71605b2379cf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048438"
---
# <a name="dynamic-link-library-data"></a>Dynamic-Link 程式庫資料

Dynamic-Link 程式庫 (DLL) 可以包含全域資料或本機資料。

## <a name="variable-scope"></a>變數範圍

編譯器和連結器會將在 DLL 原始程式碼檔中宣告為全域變數的變數視為全域變數，但每個載入指定 DLL 的進程會取得自己的 DLL 全域變數複本。 靜態變數的範圍僅限於宣告靜態變數的區塊。 因此，每個進程預設都有自己的 DLL 全域和靜態變數實例。

> [!Note]  
> 您的開發工具可讓您覆寫預設行為。 例如，Visual C++ 編譯器支援 **\# pragma 區段**，而連結器支援/SECTION 選項。 如需詳細資訊，請參閱您的開發工具隨附的檔。

 

## <a name="dynamic-memory-allocation"></a>動態記憶體配置

當 DLL 使用任何記憶體配置函式來配置記憶體時 ([**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc)、 [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)、 [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)和 [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)) ，記憶體會配置在呼叫進程的虛擬位址空間中，且只有該進程的執行緒才能存取。

DLL 可以使用檔案對應來配置可在進程間共用的記憶體。 如需如何使用檔案對應來建立命名共用記憶體的一般討論，請參閱檔案 [對應](/windows/desktop/Memory/file-mapping)。 如需使用 [**DllMain**](dllmain.md) 函式來設定使用檔案對應之共用記憶體的範例，請參閱 [使用 Dynamic-Link 程式庫中的共用記憶體](using-shared-memory-in-a-dynamic-link-library.md)。

## <a name="thread-local-storage"></a>執行緒區域儲存區

執行緒區域儲存 (TLS) 函數可讓 DLL 配置索引，以針對多執行緒進程的每個執行緒儲存和取得不同的值。 例如，每次使用者開啟新的試算表時，試算表應用程式都可以建立相同執行緒的新實例。 提供各種試算表作業之函式的 DLL，可以使用 TLS 來儲存每個試算表目前狀態的相關資訊 (資料列、資料行等等) 。 如需執行緒區域儲存區的一般討論，請參閱[執行緒區域儲存體](/windows/desktop/ProcThread/thread-local-storage)。 如需使用 [**DllMain**](dllmain.md)函數來設定執行緒區域儲存區的範例，請參閱 [Dynamic-Link 程式庫中的使用執行緒區域儲存體](using-thread-local-storage-in-a-dynamic-link-library.md)。

**Windows Server 2003 和 Windows XP：** Visual C++ 編譯器支援可讓您宣告執行緒區域變數的語法： **\_ declspec (執行緒)**。 如果您在 DLL 中使用此語法，您將無法 Windows 在 Windows Vista 之前，使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)明確地載入 dll。 如果您的 DLL 將明確載入，您必須使用執行緒區域儲存函式，而不是 **\_ declspec (執行緒)**。

 

 
