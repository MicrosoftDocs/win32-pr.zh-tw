---
description: 下列程式碼示範如何呼叫 SymFromAddr 函數。
ms.assetid: 63dfadea-b0c4-4050-add8-d1f3aef7a495
title: 依位址抓取符號資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6484327117e66826402dc97abb09f58813e528599c69bd97054528f5cfe89aba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076382"
---
# <a name="retrieving-symbol-information-by-address"></a>依位址抓取符號資訊

下列程式碼示範如何呼叫 [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) 函數。 此函數會填入 [**符號 \_ 資訊**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) 結構。 因為名稱是變數的長度，所以您必須提供夠大的緩衝區，以容納儲存在 **符號 \_ 資訊** 結構結尾的名稱。 此外， **MaxNameLen** 成員必須設定為名稱所保留的位元組數目。 在此範例中， *dwAddress* 是要對應至符號的位址。 **SymFromAddr** 函數會將符號開頭的位移儲存至 *dwDisplacement* 中的位址。 此範例假設您已使用 [初始化符號處理常式](initializing-the-symbol-handler.md)中的程式碼，初始化符號處理常式。


```C++
DWORD64  dwDisplacement = 0;
DWORD64  dwAddress = SOME_ADDRESS;

char buffer[sizeof(SYMBOL_INFO) + MAX_SYM_NAME * sizeof(TCHAR)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromAddr(hProcess, dwAddress, &dwDisplacement, pSymbol))
{
    // SymFromAddr returned success
}
else
{
    // SymFromAddr failed
    DWORD error = GetLastError();
    printf("SymFromAddr returned error : %d\n", error);
}
```



若要取得指定位址的源程式碼號，應用程式可以使用 [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)。 此函式需要 [**Imagehlp.dll \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) 結構的指標，才能接收對應至指定之程式碼位址的原始程式檔名稱和行號。 請注意，只有在使用 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)函數設定 **SYMOPT \_ 載入 \_ 行** 時，符號處理常式才能取出行號資訊。 載入模組之前，必須先設定這個選項。 DwAddress 參數包含原始程式檔名稱和行號所在的程式碼位址。


```C++
DWORD64  dwAddress;
DWORD  dwDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
dwAddress = 0x1000000; // Address you want to check on.

if (SymGetLineFromAddr64(hProcess, dwAddress, &dwDisplacement, &line))
{
    // SymGetLineFromAddr64 returned success
}
else
{
    // SymGetLineFromAddr64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromAddr64 returned error : %d\n"), error);
}
```



 

 



