---
description: 下列範例會使用 RegQueryInfoKey、RegEnumKeyEx 和 RegEnumValue 函式來列舉所指定機碼的子機碼。
ms.assetid: 3730180a-52bc-4382-83ca-39f162273ba5
title: 列舉登錄子機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 629e86b0ee763571af8b19f07a259bd8478a44e0311d0f82199fa9baf7e39050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117958621"
---
# <a name="enumerating-registry-subkeys"></a>列舉登錄子機碼

下列範例會使用 [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya)、 [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa)和 [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) 函式來列舉所指定機碼的子機碼。 傳遞至每個函式的 hKey 參數是開啟索引鍵的控制碼。 此索引鍵必須在函式呼叫之前開啟，並且在之後關閉。


```C++
// QueryKey - Enumerates the subkeys of key and its associated values.
//     hKey - Key whose subkeys and values are to be enumerated.

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define MAX_KEY_LENGTH 255
#define MAX_VALUE_NAME 16383
 
void QueryKey(HKEY hKey) 
{ 
    TCHAR    achKey[MAX_KEY_LENGTH];   // buffer for subkey name
    DWORD    cbName;                   // size of name string 
    TCHAR    achClass[MAX_PATH] = TEXT("");  // buffer for class name 
    DWORD    cchClassName = MAX_PATH;  // size of class string 
    DWORD    cSubKeys=0;               // number of subkeys 
    DWORD    cbMaxSubKey;              // longest subkey size 
    DWORD    cchMaxClass;              // longest class string 
    DWORD    cValues;              // number of values for key 
    DWORD    cchMaxValue;          // longest value name 
    DWORD    cbMaxValueData;       // longest value data 
    DWORD    cbSecurityDescriptor; // size of security descriptor 
    FILETIME ftLastWriteTime;      // last write time 
 
    DWORD i, retCode; 
 
    TCHAR  achValue[MAX_VALUE_NAME]; 
    DWORD cchValue = MAX_VALUE_NAME; 
 
    // Get the class name and the value count. 
    retCode = RegQueryInfoKey(
        hKey,                    // key handle 
        achClass,                // buffer for class name 
        &cchClassName,           // size of class string 
        NULL,                    // reserved 
        &cSubKeys,               // number of subkeys 
        &cbMaxSubKey,            // longest subkey size 
        &cchMaxClass,            // longest class string 
        &cValues,                // number of values for this key 
        &cchMaxValue,            // longest value name 
        &cbMaxValueData,         // longest value data 
        &cbSecurityDescriptor,   // security descriptor 
        &ftLastWriteTime);       // last write time 
 
    // Enumerate the subkeys, until RegEnumKeyEx fails.
    
    if (cSubKeys)
    {
        printf( "\nNumber of subkeys: %d\n", cSubKeys);

        for (i=0; i<cSubKeys; i++) 
        { 
            cbName = MAX_KEY_LENGTH;
            retCode = RegEnumKeyEx(hKey, i,
                     achKey, 
                     &cbName, 
                     NULL, 
                     NULL, 
                     NULL, 
                     &ftLastWriteTime); 
            if (retCode == ERROR_SUCCESS) 
            {
                _tprintf(TEXT("(%d) %s\n"), i+1, achKey);
            }
        }
    } 
 
    // Enumerate the key values. 

    if (cValues) 
    {
        printf( "\nNumber of values: %d\n", cValues);

        for (i=0, retCode=ERROR_SUCCESS; i<cValues; i++) 
        { 
            cchValue = MAX_VALUE_NAME; 
            achValue[0] = '\0'; 
            retCode = RegEnumValue(hKey, i, 
                achValue, 
                &cchValue, 
                NULL, 
                NULL,
                NULL,
                NULL);
 
            if (retCode == ERROR_SUCCESS ) 
            { 
                _tprintf(TEXT("(%d) %s\n"), i+1, achValue); 
            } 
        }
    }
}

int __cdecl _tmain()
{
   HKEY hTestKey;

   if( RegOpenKeyEx( HKEY_CURRENT_USER,
        TEXT("SOFTWARE\\Microsoft"),
        0,
        KEY_READ,
        &hTestKey) == ERROR_SUCCESS
      )
   {
      QueryKey(hTestKey);
   }
   
   RegCloseKey(hTestKey);
}
```



 

 



