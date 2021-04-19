---
description: 每個進程都有與其相關聯的環境區塊。
ms.assetid: b428688c-7b16-48c7-8d89-55d066496d1c
title: 變更環境變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13054afff996c4f8128fdc58f9d6dfadc35cc84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974446"
---
# <a name="changing-environment-variables"></a><span data-ttu-id="bfae3-103">變更環境變數</span><span class="sxs-lookup"><span data-stu-id="bfae3-103">Changing Environment Variables</span></span>

<span data-ttu-id="bfae3-104">每個進程都有與其相關聯的環境區塊。</span><span class="sxs-lookup"><span data-stu-id="bfae3-104">Each process has an environment block associated with it.</span></span> <span data-ttu-id="bfae3-105">環境區塊是由以 null 終止的字串之以 null 結束的區塊所組成， (表示區塊結尾有兩個 null 位元組) ，其中每個字串的格式如下：</span><span class="sxs-lookup"><span data-stu-id="bfae3-105">The environment block consists of a null-terminated block of null-terminated strings (meaning there are two null bytes at the end of the block), where each string is in the form:</span></span>

<span data-ttu-id="bfae3-106">*名稱* =*值*</span><span class="sxs-lookup"><span data-stu-id="bfae3-106">*name*=*value*</span></span>

<span data-ttu-id="bfae3-107">環境區塊中的所有字串都必須依名稱以字母順序排序。</span><span class="sxs-lookup"><span data-stu-id="bfae3-107">All strings in the environment block must be sorted alphabetically by name.</span></span> <span data-ttu-id="bfae3-108">排序不區分大小寫、Unicode 順序，而不考慮地區設定。</span><span class="sxs-lookup"><span data-stu-id="bfae3-108">The sort is case-insensitive, Unicode order, without regard to locale.</span></span> <span data-ttu-id="bfae3-109">因為等號是分隔符號，所以不能用於環境變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="bfae3-109">Because the equal sign is a separator, it must not be used in the name of an environment variable.</span></span>

## <a name="example-1"></a><span data-ttu-id="bfae3-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="bfae3-110">Example 1</span></span>

<span data-ttu-id="bfae3-111">根據預設，子進程會繼承父進程的環境區塊複本。</span><span class="sxs-lookup"><span data-stu-id="bfae3-111">By default, a child process inherits a copy of the environment block of the parent process.</span></span> <span data-ttu-id="bfae3-112">下列範例示範如何建立新的環境區塊，以使用 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)傳遞給子進程。</span><span class="sxs-lookup"><span data-stu-id="bfae3-112">The following example demonstrates how to create a new environment block to pass to a child process using [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

<span data-ttu-id="bfae3-113">此範例會使用範例三中的程式碼做為子進程，Ex3.exe。</span><span class="sxs-lookup"><span data-stu-id="bfae3-113">This example uses the code in example three as the child process, Ex3.exe.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

#define BUFSIZE 4096

int _tmain()
{
    TCHAR chNewEnv[BUFSIZE];
    LPTSTR lpszCurrentVariable; 
    DWORD dwFlags=0;
    TCHAR szAppName[]=TEXT("ex3.exe");
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fSuccess; 
 
    // Copy environment strings into an environment block. 
 
    lpszCurrentVariable = (LPTSTR) chNewEnv;
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MySetting=A"))))
    {
        printf("String copy failed\n"); 
        return FALSE;
    }

    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MyVersion=2")))) 
    {
        printf("String copy failed\n"); 
        return FALSE;
    }
 
    // Terminate the block with a NULL byte. 
 
    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    *lpszCurrentVariable = (TCHAR)0; 

    // Create the child process, specifying a new environment block. 
 
    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);

#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags,
        (LPVOID) chNewEnv,   // new environment block
        NULL, &si, &pi); 
 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError());
        return FALSE;
    }
    WaitForSingleObject(pi.hProcess, INFINITE);
    return TRUE;
}
```



## <a name="example-2"></a><span data-ttu-id="bfae3-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="bfae3-114">Example 2</span></span>

<span data-ttu-id="bfae3-115">在進程建立期間改變子進程的環境變數，是一個進程可以直接變更另一個進程的環境變數的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="bfae3-115">Altering the environment variables of a child process during process creation is the only way one process can directly change the environment variables of another process.</span></span> <span data-ttu-id="bfae3-116">進程絕對不能直接變更另一個進程的環境變數，而該進程不是該進程的子系。</span><span class="sxs-lookup"><span data-stu-id="bfae3-116">A process can never directly change the environment variables of another process that is not a child of that process.</span></span>

<span data-ttu-id="bfae3-117">如果您想讓子進程繼承大部分父系的環境，只需進行一些變更，請使用 [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)抓取目前的值、儲存這些值、建立子進程的已更新區塊以進行繼承、建立子進程，然後使用 [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable)還原已儲存的值，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="bfae3-117">If you want the child process to inherit most of the parent's environment with only a few changes, retrieve the current values using [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable), save these values, create an updated block for the child process to inherit, create the child process, and then restore the saved values using [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable), as shown in the following example.</span></span>

<span data-ttu-id="bfae3-118">此範例會使用範例三中的程式碼做為子進程，Ex3.exe。</span><span class="sxs-lookup"><span data-stu-id="bfae3-118">This example uses the code in example three as the child process, Ex3.exe.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 4096
#define VARNAME TEXT("MyVariable")

int _tmain()
{
    DWORD dwRet, dwErr;
    LPTSTR pszOldVal; 
    TCHAR szAppName[]=TEXT("ex3.exe");
    DWORD dwFlags=0;
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fExist, fSuccess; 
 
    // Retrieves the current value of the variable if it exists.
    // Sets the variable to a new value, creates a child process,
    // then uses SetEnvironmentVariable to restore the original
    // value or delete it if it did not exist previously. 
 
    pszOldVal = (LPTSTR) malloc(BUFSIZE*sizeof(TCHAR));
    if(NULL == pszOldVal)
    {
        printf("Out of memory\n");
        return FALSE;
    }

    dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, BUFSIZE);

    if(0 == dwRet)
    {
        dwErr = GetLastError();
        if( ERROR_ENVVAR_NOT_FOUND == dwErr )
        {
            printf("Environment variable does not exist.\n");
            fExist=FALSE;
        }
    }
    else if(BUFSIZE < dwRet)
    {
        pszOldVal = (LPTSTR) realloc(pszOldVal, dwRet*sizeof(TCHAR));   
        if(NULL == pszOldVal)
        {
            printf("Out of memory\n");
            return FALSE;
        }
        dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, dwRet);
        if(!dwRet)
        {
            printf("GetEnvironmentVariable failed (%d)\n", GetLastError());
            return FALSE;
        }
        else fExist=TRUE;
    }
    else fExist=TRUE;

    // Set a value for the child process to inherit. 
 
    if (! SetEnvironmentVariable(VARNAME, TEXT("Test"))) 
    {
        printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
        return FALSE;
    }
 
    // Create a child process. 

    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);
 
#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags, 
        NULL,     // inherit parent's environment 
        NULL, &si, &pi); 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError()); 
    }
    WaitForSingleObject(pi.hProcess, INFINITE);

    // Restore the original environment variable. 
 
    if(fExist)
    {
        if (! SetEnvironmentVariable(VARNAME, pszOldVal)) 
        {
            printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
            return FALSE;
        }
    }
    else SetEnvironmentVariable(VARNAME, NULL);

    free(pszOldVal);
    
    return fSuccess;
}
```



## <a name="example-3"></a><span data-ttu-id="bfae3-119">範例 3</span><span class="sxs-lookup"><span data-stu-id="bfae3-119">Example 3</span></span>

<span data-ttu-id="bfae3-120">下列範例會使用 [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) 抓取進程的環境區塊，並將內容列印至主控台。</span><span class="sxs-lookup"><span data-stu-id="bfae3-120">The following example retrieves the process's environment block using [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) and prints the contents to the console.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int _tmain()
{
    LPTSTR lpszVariable; 
    LPTCH lpvEnv; 
 
    // Get a pointer to the environment block. 
 
    lpvEnv = GetEnvironmentStrings();

    // If the returned pointer is NULL, exit.
    if (lpvEnv == NULL)
    {
        printf("GetEnvironmentStrings failed (%d)\n", GetLastError()); 
        return 0;
    }
 
    // Variable strings are separated by NULL byte, and the block is 
    // terminated by a NULL byte. 

    lpszVariable = (LPTSTR) lpvEnv;

    while (*lpszVariable)
    {
        _tprintf(TEXT("%s\n"), lpszVariable);
        lpszVariable += lstrlen(lpszVariable) + 1;
    }
    FreeEnvironmentStrings(lpvEnv);
    return 1;
}
```



 

 
