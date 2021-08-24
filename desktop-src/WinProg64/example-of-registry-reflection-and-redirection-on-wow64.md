---
title: WOW64 上的登錄重新導向範例
description: 下列範例程式碼示範64位 Windows 上登錄重新導向器所提供的不同登錄視圖。
ms.assetid: b3ca2a47-402d-4e91-88bc-ddda6c776468
keywords:
- 範例 64-位 Windows 程式設計
- 64位 Windows 程式設計指南範例64位 Windows 程式設計
- 64位 Windows 程式設計指南範例64位 Windows 程式設計、WOW64 上的登錄重新導向
- 登錄重新導向範例 64-位 Windows 程式設計
- 64位 Windows 程式設計指南64位 Windows 程式設計，範例請參閱64位 Windows 程式設計指南範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83428edb31e53bdd1c70825c7fa5a4d799a36536fa9c17f9ce1c4587ab096048
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680227"
---
# <a name="example-of-registry-redirection-on-wow64"></a>WOW64 上的登錄重新導向範例

下列範例程式碼示範64位 Windows 上登錄重新導向器所提供的不同登錄視圖。 它也會示範如何根據金鑰的共用或重新導向來設定索引鍵的值。 如需詳細資訊，請參閱 [受 WOW64 影響的](shared-registry-keys.md)登錄機碼。

分別針對32位和64位的 Windows 編譯下列程式碼。 在64位 Windows 上執行每個產生的可執行檔，並比較輸出。 這兩個版本的範例輸出列在原始程式碼下方。


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

// Define application constants.
#if defined(_WIN64)

#define VIEW_DATA L"Hello! 64-bit World"
#define ALT_VIEW_DATA L"Hello! 32-bit World"
#define CROSS_ACCESS KEY_WOW64_32KEY

#else

#define VIEW_DATA L"Hello! 32-bit World"
#define ALT_VIEW_DATA L"Hello! 64-bit World"
#define CROSS_ACCESS KEY_WOW64_64KEY

#endif

// Create a registry key and set its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    CreateRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag,
        PBYTE pValue,
        DWORD dwValueSize
        )
{
    DWORD dwDisposition;
    HKEY  hKey;
    DWORD dwRet;

    dwRet = 
        RegCreateKeyEx(
            hKeyParent,
            KeyName,
            0,
            NULL,
            REG_OPTION_NON_VOLATILE,
            rsAccessMask | rsSamViewFlag,
            NULL,
            &hKey,
            &dwDisposition);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening or creating key.\n");
        return FALSE;
    }

    // Attempt to set the value of the key.
    // If the call fails, close the key and return.
    if (ERROR_SUCCESS !=
            RegSetValueEx(
                hKey,
                NULL,
                0,
                REG_SZ,
                pValue,
                dwValueSize))
    {
        printf("Could not set registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    RegCloseKey(hKey);
    return TRUE;
}

// Access a registry key and print its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    AccessRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag
        )
{
    HKEY hKey;
    WCHAR Buffer[MAX_PATH];
    DWORD dwSize = sizeof(Buffer);
    DWORD dwType;
    DWORD dwRet;

    dwRet =
        RegOpenKeyEx(
            hKeyParent,
            KeyName,
            0,
            rsAccessMask | rsSamViewFlag,
            &hKey);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening key!\n");
        return FALSE;
    }

    if (ERROR_SUCCESS !=
            RegQueryValueEx(
                hKey,
                NULL,
                0,
                &dwType,
                (PBYTE)Buffer,
                &dwSize))
    {
        printf("Could not read registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    if (rsSamViewFlag != 0)
    {
        printf("Alternate view:   %S\n", Buffer);
    }
    else
    {
        printf("Default view:     %S\n", Buffer);
    }

    RegCloseKey(hKey);
    return TRUE;
}

int
main()
{
    BOOL Res;

    // Define the list of keys to work with.
    typedef struct {
        HKEY hkRoot;
        LPWSTR szRootName;
        LPWSTR szName;
    }KEYDATA;

    KEYDATA Keys[] =
    {
        { HKEY_LOCAL_MACHINE, L"HKLM", L"Software\\Hello World" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"Hello" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32" }
    };

    // Now create the keys.
    for (int i = 0; i < _countof(Keys); i++)
    {
        // Create the keys in the alternate view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                CROSS_ACCESS,
                (PBYTE)ALT_VIEW_DATA,
                sizeof(ALT_VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in alternate view of the registry.\n");
            return 1; 
       }

        // Create the keys in the default view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                0,
                (PBYTE)VIEW_DATA,
                sizeof(VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in default view of the registry.\n");
            return 1;
        }
    }

    // Access the registry and print key values.
    printf("Application string: %S\n", VIEW_DATA);

    for (int i = 0; i < _countof(Keys); i++)
    {
        printf("%S\\%S\n", Keys[i].szRootName, Keys[i].szName);
        Res = 
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ, 
                0);
        if (Res == FALSE)
        {
            printf("Unable to access default view of registry.\n");
            return 1;
        }

        // Calls with CROSS_ACCESS explicitly access the alternate registry view.
        Res =
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ,
                CROSS_ACCESS);
        if (Res == FALSE)
        {
            printf("Unable to access alternate view of registry.\n");
            return 1;
        }
    }
    return 0;
}
```



當執行此範例的64位版本時，它會產生下列輸出。 **HKCR \\ Hello** 的預設和替代視圖的值都相同，因為這是共用的金鑰。 其他索引鍵的值不同，因為它們會重新導向。

**Windows server 2008、Windows Vista Windows server 2003 和 Windows XP：** 當此範例在這些作業系統上執行時，LocalServer32 索引鍵的預設和替代視圖會有相同的值。 這是因為 LocalServer32 索引鍵會重新導向並 *反映出來*，這會在金鑰的控制碼關閉時，讓其值在登錄的64位和32位的觀點之間進行同步處理。 從 Windows 7 開始，已移除登錄反映。 如需詳細資訊，請參閱登錄 [反映](registry-reflection.md)。

``` syntax
Application string: Hello! 64-bit World
HKLM\Software\Hello World
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\Hello
Default view:     Hello! 64-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
```

當執行此範例的32位版本時，它會產生下列輸出。 針對32位應用程式，登錄的64位視圖是替代的視圖，因此值會反轉，除了 HKCR \\ Hello （共用金鑰）之外。

``` syntax
Application string: Hello! 32-bit World
HKLM\Software\Hello World
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\Hello
Default view:     Hello! 32-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
```

若要檢查使用 regedit 執行此範例的效果，請檢查下列索引鍵的值。 請注意，應用程式應該避免在硬式編碼登錄路徑中使用 Wow6432Node。

**HKLM \\ 軟體 \\ Hello World**  
**HKLM \\ SOFTWARE \\ Wow6432Node \\ Hello World**  
**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**  
**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**  
**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**  
**HKCR \\ HELLO HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**  
**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**  
**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**  
**HKCR \\ Wow6432Node \\ Hello**  


## <a name="related-topics"></a>相關主題

<dl> <dt>

[登錄重新導向程式](registry-redirector.md)
</dt> <dt>

[登錄反映](registry-reflection.md)
</dt> </dl>

 

 




