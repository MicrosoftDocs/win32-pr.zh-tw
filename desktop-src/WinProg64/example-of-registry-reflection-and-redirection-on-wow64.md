---
title: WOW64 上的登錄重新導向範例
description: 下列範例程式碼示範64位 Windows 上登錄重新導向器所提供的不同登錄視圖。
ms.assetid: b3ca2a47-402d-4e91-88bc-ddda6c776468
keywords:
- 範例 64-位 Windows 程式設計
- 64位 Windows 程式設計指南範例64位 Windows 程式設計
- 64位 Windows 程式設計指南範例64位 Windows 程式設計，WOW64 上的登錄重新導向
- 登錄重新導向範例 64-位 Windows 程式設計
- 64位 Windows 程式設計指南64位 Windows 程式設計，範例請參閱64位 Windows 程式設計指南範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff37b077137e9802e6716319623fe8e372941500
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "104383149"
---
# <a name="example-of-registry-redirection-on-wow64"></a><span data-ttu-id="06f5e-108">WOW64 上的登錄重新導向範例</span><span class="sxs-lookup"><span data-stu-id="06f5e-108">Example of Registry Redirection on WOW64</span></span>

<span data-ttu-id="06f5e-109">下列範例程式碼示範64位 Windows 上登錄重新導向器所提供的不同登錄視圖。</span><span class="sxs-lookup"><span data-stu-id="06f5e-109">The following example code demonstrates the separate views of the registry provided by the registry redirector on 64-bit Windows.</span></span> <span data-ttu-id="06f5e-110">它也會示範如何根據金鑰的共用或重新導向來設定索引鍵的值。</span><span class="sxs-lookup"><span data-stu-id="06f5e-110">It also demonstrates how the values of keys are set depending on whether a key is shared or redirected.</span></span> <span data-ttu-id="06f5e-111">如需詳細資訊，請參閱 [受 WOW64 影響的](shared-registry-keys.md)登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="06f5e-111">For more information, see [Registry Keys Affected by WOW64](shared-registry-keys.md).</span></span>

<span data-ttu-id="06f5e-112">分別針對32位和64位 Windows 編譯下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="06f5e-112">Compile the following code separately for both 32-bit and 64-bit Windows.</span></span> <span data-ttu-id="06f5e-113">在64位的 Windows 上執行每個產生的可執行檔，並比較輸出。</span><span class="sxs-lookup"><span data-stu-id="06f5e-113">Run each resulting executable file on 64-bit Windows and compare the output.</span></span> <span data-ttu-id="06f5e-114">這兩個版本的範例輸出列在原始程式碼下方。</span><span class="sxs-lookup"><span data-stu-id="06f5e-114">Sample output for both versions is listed below the source code.</span></span>


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



<span data-ttu-id="06f5e-115">當執行此範例的64位版本時，它會產生下列輸出。</span><span class="sxs-lookup"><span data-stu-id="06f5e-115">When the 64-bit version of the example is run, it produces the following output.</span></span> <span data-ttu-id="06f5e-116">**HKCR \\ Hello** 的預設和替代視圖的值都相同，因為這是共用的金鑰。</span><span class="sxs-lookup"><span data-stu-id="06f5e-116">The values of both the default and alternate views of **HKCR\\Hello** are the same because this key is shared.</span></span> <span data-ttu-id="06f5e-117">其他索引鍵的值不同，因為它們會重新導向。</span><span class="sxs-lookup"><span data-stu-id="06f5e-117">The values of the other keys differ because they are redirected.</span></span>

<span data-ttu-id="06f5e-118">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 當此範例在這些作業系統上執行時，LocalServer32 索引鍵的預設和替代視圖會有相同的值。</span><span class="sxs-lookup"><span data-stu-id="06f5e-118">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** When this example is run on these operating systems, the default and alternate views of the LocalServer32 key have the same value.</span></span> <span data-ttu-id="06f5e-119">這是因為 LocalServer32 索引鍵會重新導向並 *反映出來*，這會在金鑰的控制碼關閉時，讓其值在登錄的64位和32位的觀點之間進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="06f5e-119">This is because the LocalServer32 key is redirected and *reflected*, which causes its value to be synchronized between the 64-bit and 32-bit views of the registry as soon as the handle to the key is closed.</span></span> <span data-ttu-id="06f5e-120">從 Windows 7 開始，已移除登錄反映。</span><span class="sxs-lookup"><span data-stu-id="06f5e-120">Registry reflection was removed starting with Windows 7.</span></span> <span data-ttu-id="06f5e-121">如需詳細資訊，請參閱登錄 [反映](registry-reflection.md)。</span><span class="sxs-lookup"><span data-stu-id="06f5e-121">For more information, see [Registry Reflection](registry-reflection.md).</span></span>

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

<span data-ttu-id="06f5e-122">當執行此範例的32位版本時，它會產生下列輸出。</span><span class="sxs-lookup"><span data-stu-id="06f5e-122">When the 32-bit version of the example is run, it produces the following output.</span></span> <span data-ttu-id="06f5e-123">針對32位應用程式，登錄的64位視圖是替代的視圖，因此值會反轉，除了 HKCR \\ Hello （共用金鑰）之外。</span><span class="sxs-lookup"><span data-stu-id="06f5e-123">For a 32-bit application, the 64-bit view of the registry is the alternate view so the values are reversed, except for HKCR\\Hello, which is a shared key.</span></span>

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

<span data-ttu-id="06f5e-124">若要檢查使用 regedit 執行此範例的效果，請檢查下列索引鍵的值。</span><span class="sxs-lookup"><span data-stu-id="06f5e-124">To examine the effect of running this example with regedit, inspect the values of the following keys.</span></span> <span data-ttu-id="06f5e-125">請注意，應用程式應該避免在硬式編碼登錄路徑中使用 Wow6432Node。</span><span class="sxs-lookup"><span data-stu-id="06f5e-125">Note that applications should avoid using Wow6432Node in hard-coded registry paths.</span></span>

<span data-ttu-id="06f5e-126">**HKLM \\ 軟體 \\ Hello World**</span><span class="sxs-lookup"><span data-stu-id="06f5e-126">**HKLM\\SOFTWARE\\Hello World**</span></span>  
<span data-ttu-id="06f5e-127">**HKLM \\ SOFTWARE \\ Wow6432Node \\ Hello World**</span><span class="sxs-lookup"><span data-stu-id="06f5e-127">**HKLM\\SOFTWARE\\Wow6432Node\\Hello World**</span></span>  
<span data-ttu-id="06f5e-128">**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**</span><span class="sxs-lookup"><span data-stu-id="06f5e-128">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}**</span></span>  
<span data-ttu-id="06f5e-129">**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="06f5e-129">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32**</span></span>  
<span data-ttu-id="06f5e-130">**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="06f5e-130">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32**</span></span>  
<span data-ttu-id="06f5e-131">**HKCR \\ HELLO HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**</span><span class="sxs-lookup"><span data-stu-id="06f5e-131">**HKCR\\Hello HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}**</span></span>  
<span data-ttu-id="06f5e-132">**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="06f5e-132">**HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32**</span></span>  
<span data-ttu-id="06f5e-133">**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="06f5e-133">**HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32**</span></span>  
<span data-ttu-id="06f5e-134">**HKCR \\ Wow6432Node \\ Hello**</span><span class="sxs-lookup"><span data-stu-id="06f5e-134">**HKCR\\Wow6432Node\\Hello**</span></span>  


## <a name="related-topics"></a><span data-ttu-id="06f5e-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="06f5e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06f5e-136">登錄重新導向程式</span><span class="sxs-lookup"><span data-stu-id="06f5e-136">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="06f5e-137">登錄反映</span><span class="sxs-lookup"><span data-stu-id="06f5e-137">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

 




