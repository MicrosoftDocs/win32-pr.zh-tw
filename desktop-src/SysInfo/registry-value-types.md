---
description: 登錄值可以儲存各種格式的資料。
ms.assetid: 5fd828d6-4d62-4823-a2f1-15782b5cd28c
title: 登錄數值型別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed2bc73e03d9aab8d39bdda31ab308af1749f22315a262ceb4ae28ec743c8c69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885009"
---
# <a name="registry-value-types"></a>登錄數值型別

登錄值可以儲存各種格式的資料。 當您在登錄值下儲存資料時（例如，藉由呼叫 [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) 函式），您可以指定下列其中一個值來表示要儲存的資料類型。 當您取得登錄值時，如 [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) 的函式會使用這些值來指出抓取的資料類型。

下列登錄數值型別定義于 Winnt. h 中。



| 值                                 | 類型                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REG \_ 二進位檔<br/>                | 任何形式的二進位資料，<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| REG \_ DWORD<br/>                 | 32位數位。<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG DWORD 位元組由大到 \_ \_ 小 \_<br/> | 以位元組由大到小的格式的32位數位。<br/> Windows 是設計用來在以位元組由小到大的電腦架構上執行。 因此，在 Windows 標頭檔中，此值會定義為 REG \_ DWORD。<br/>                                                                                                                                                                                                                          |
| REG \_ DWORD \_ BIG \_ ENDIAN<br/>    | 以位元組由大到小的格式的32位數位。<br/> 某些 UNIX 系統支援位元組由大到小的架構。<br/>                                                                                                                                                                                                                                                                                                                         |
| REG \_ EXPAND \_ SZ<br/>            | 以 null 終止的字串，其中包含環境變數的未展開參考 (例如 "% PATH%" ) 。 它將會是 Unicode 或 ANSI 字串，取決於您使用的是 Unicode 或 ANSI 函數。 若要展開環境變數參考，請使用 [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) 函數。<br/>                                                                                 |
| REG \_ 連結<br/>                  | 以 null 終止的 Unicode 字串，其中包含以 REG [](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) \_ OPTION \_ CREATE link 呼叫 RegCreateKeyEx 函式所建立之符號連結的目標路徑 \_ 。<br/>                                                                                                                                                                                                                          |
| REG \_ 多重 \_ SZ<br/>             | 以 null 結束的字串序列，以空字串 (\\ 0) 結束。<br/> 以下是一個範例：<br/> *String1* \\0 *String2* \\ 0 *String3* \\ 0 *LastString* \\ 0 \\ 0<br/> 第一個 \\ 0 會終止第一個字串，最後一個0到最後一個字串的第二個會結束 \\ 最後一個字串，最後0則會 \\ 結束序列。 請注意，最後的結束字元必須考慮到字串的長度。<br/> |
| REG \_ 無<br/>                  | 沒有定義的實值型別。<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| REG \_ QWORD<br/>                 | 64位數位。<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ QWORD 位元組由大到 \_ 小 \_<br/> | 以位元組由大到小的格式的64位數位。<br/> Windows 是設計用來在以位元組由小到大的電腦架構上執行。 因此，在 Windows 標頭檔中，此值會定義為 REG \_ QWORD。<br/>                                                                                                                                                                                                                          |
| REG \_ SZ<br/>                    | null 終止的字串。 這會是 Unicode 或 ANSI 字串，取決於您使用的是 Unicode 或 ANSI 函數。<br/>                                                                                                                                                                                                                                                                                       |



 

## <a name="string-values"></a>字串值

如果資料具有 REG \_ sz、reg \_ 多重 \_ SZ 或 reg \_ EXPAND \_ sz 型別，則字串可能尚未以適當的終止 null 字元儲存。 因此，從登錄讀取字串時，您必須確定字串在使用之前已正確地終止;否則，它可能會覆寫緩衝區。  (請注意，REG \_ 多重 \_ SZ 字串應該有兩個結束的 null 字元。 ) 

將字串寫入登錄時，您必須指定字串的長度，包括結束的 null 字元 (\\ 0) 。 常見的錯誤是使用 **strlen** 函式來判斷字串的長度，但請記住， **strlen** 只會傳回字串中的字元數，不包括終止的 null。 因此，應計算字串的長度，如下所示： `strlen( string ) + 1`

REG \_ 多重 \_ SZ 字串的結尾為長度為0的字串。 因此，序列中不能包含長度為零的字串。 空的序列定義如下： \\ 0。

下列範例會逐步解說 REG \_ 多重 \_ SZ 字串。


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void SampleSzz(PTSTR pszz)
{
   _tprintf(_TEXT("\tBegin multi-sz string\n"));
   while (*pszz) 
   {
      _tprintf(_TEXT("\t\t%s\n"), pszz);
      pszz = pszz + _tcslen(pszz) + 1;
   }
   _tprintf(_TEXT("\tEnd multi-sz\n"));
}

int __cdecl main(int argc, char **argv)
{
   // Because the compiler adds a \0 at the end of quoted strings, 
   // there are two \0 terminators at the end. 

   _tprintf(_TEXT("Conventional multi-sz string:\n"));  
   SampleSzz(_TEXT("String1\0String2\0String3\0LastString\0"));

   _tprintf(_TEXT("\nTest case with no strings:\n"));  
   SampleSzz(_TEXT(""));

   return 0;
}
```



## <a name="byte-formats"></a>位元組格式

以 *位元組* 由小到大的格式來說，多位元組的值會儲存在記憶體中的最小位元組 (「小端」 ) 到最高的位元組。 例如，值0x12345678 會儲存為 (0x78 0x56 0x34 0x12) 以位元組由小到大格式表示。

以 *位元組由大* 到小的格式來說，多重位元組值會儲存在記憶體中，從最高的位元組 ("big end" ) 到最小的位元組。 例如，值0x12345678 會以位元組由大到小的格式儲存為 (0x12 0x34 0x56 0x78) 。

 

