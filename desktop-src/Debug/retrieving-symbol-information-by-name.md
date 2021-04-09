---
description: 下列程式碼示範如何呼叫 SymFromName 函數。
ms.assetid: d3a9d73e-fb77-4be3-a881-c258bcc587fe
title: 依名稱抓取符號資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f5f4477be4f494383c7d9c1ca462f3beb69690
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110453"
---
# <a name="retrieving-symbol-information-by-name"></a>依名稱抓取符號資訊

下列程式碼示範如何呼叫 [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) 函數。 此函數會填入 [**符號 \_ 資訊**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) 結構。 因為名稱是變數的長度，所以您必須提供夠大的緩衝區，以容納儲存在 **符號 \_ 資訊** 結構結尾的名稱。 此外， **MaxNameLen** 成員必須設定為名稱所保留的位元組數目。 在此範例中，szSymbolName 是儲存所要求符號名稱的緩衝區。 此範例假設您已使用 [初始化符號處理常式](initializing-the-symbol-handler.md)中的程式碼，初始化符號處理常式。


```C++
TCHAR szSymbolName[MAX_SYM_NAME];
ULONG64 buffer[(sizeof(SYMBOL_INFO) +
    MAX_SYM_NAME * sizeof(TCHAR) +
    sizeof(ULONG64) - 1) /
    sizeof(ULONG64)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

_tcscpy_s(szSymbolName, MAX_SYM_NAME, TEXT("WinMain"));
pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromName(hProcess, szSymbolName, pSymbol))
{
    // SymFromName returned success
}
else
{
    // SymFromName failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymFromName returned error : %d\n"), error);
}
```



如果應用程式有模組或原始程式檔的名稱，以及行號資訊，則可以使用 [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) 來取出虛擬程式碼位址。 此函式需要 [**Imagehlp.dll \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) 結構的指標，才能接收虛擬程式碼位址。 請注意，只有在 \_ \_ 使用 [**SYMSETOPTIONS**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) 函數設定 SYMOPT 載入行選項時，符號處理常式才能取出行號資訊。 載入模組之前，必須先設定這個選項。 SzModuleName 參數包含來源模組名稱;它是選擇性的，可以是 **Null**。 SzFileName 參數應包含來原始檔案名，而 dwLineNumber 參數應包含要抓取虛擬位址的行號。


```C++
TCHAR  szModuleName[MAX_PATH];
TCHAR  szFileName[MAX_PATH];
DWORD  dwLineNumber;
LONG   lDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
_tcscpy_s(szModuleName, MAX_PATH, TEXT("MyApp"));
_tcscpy_s(szFileName, MAX_PATH, TEXT("main.c"));
dwLineNumber = 248;

if (SymGetLineFromName64(hProcess, szModuleName, szFileName,
    dwLineNumber, &lDisplacement, &line))
{
    // SymGetLineFromName64 returned success
}
else
{
    // SymGetLineFromName64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromName64 returned error : %d\n"), error);
}
```



 

 



