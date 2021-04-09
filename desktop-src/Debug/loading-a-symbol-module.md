---
description: 如果應用程式未呼叫 SymInitialize 函式，並將 fInvadeProcess 參數設為 TRUE，它就必須在需要時載入模組的符號。
ms.assetid: 01cee812-d1f2-4459-acee-bce8719a85b2
title: 載入符號模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5182322e62b450333a064069ea5f5de2aa95e912
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110149"
---
# <a name="loading-a-symbol-module"></a>載入符號模組

如果應用程式未呼叫 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 函式，並將 *fInvadeProcess* 參數設為 **TRUE**，它就必須在需要時載入模組的符號。 若要視需要載入符號模組，應用程式可以使用模組名稱的完整路徑來呼叫 [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) 函數。 載入模組時，符號處理常式會立即載入符號或延遲載入，視使用 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) 函式所設定的選項而定。

下列程式碼會載入符號模組。 請注意，它會假設您已使用 [初始化符號處理常式](initializing-the-symbol-handler.md)中的程式碼來初始化符號處理常式。


```C++
TCHAR  szImageName[MAX_PATH] = TEXT("foo.dll");
DWORD64 dwBaseAddr = 0;

if (SymLoadModuleEx(hProcess,    // target process 
                    NULL,        // handle to image - not used
                    szImageName, // name of image file
                    NULL,        // name of module - not required
                    dwBaseAddr,  // base address - not required
                    0,           // size of image - not required
                    NULL,        // MODLOAD_DATA used for special cases 
                    0))          // flags - not required
{
    // SymLoadModuleEx returned success
}
else
{
    // SymLoadModuleEx failed
    DWORD error = GetLastError();
    printf("SymLoadModuleEx returned error : %d\n", error);
}
```



請注意， *szImageName* 可以是任何 ( .exe、.dll、. winspool.drv、sys、.scr、cpl、.com) 的可執行模組的路徑。 此外， *dwBaseAddr* 是要載入之符號模組的基底位址。 如果這個值為0，符號處理常式將會從指定的符號模組取得基底位址。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[卸載符號模組](unloading-a-symbol-module.md)
</dt> </dl>

 

 



