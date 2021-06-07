---
title: 使用資源
description: 本章節包含與資來源程式設計工作相關的程式碼。
ms.assetid: 73678045-1518-46cd-ab55-5d272852ba73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e4f42f908bc2ee63cfa273a5251b0bd8d9bf86
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549870"
---
# <a name="using-resources"></a><span data-ttu-id="6936f-103">使用資源</span><span class="sxs-lookup"><span data-stu-id="6936f-103">Using Resources</span></span>

<span data-ttu-id="6936f-104">本章節包含下列工作的程式碼片段：</span><span class="sxs-lookup"><span data-stu-id="6936f-104">This section contains code snippets for the following tasks:</span></span>

-   [<span data-ttu-id="6936f-105">更新資源</span><span class="sxs-lookup"><span data-stu-id="6936f-105">Updating Resources</span></span>](#updating-resources)
-   [<span data-ttu-id="6936f-106">建立資源清單</span><span class="sxs-lookup"><span data-stu-id="6936f-106">Creating a Resource List</span></span>](#creating-a-resource-list)

## <a name="updating-resources"></a><span data-ttu-id="6936f-107">更新資源</span><span class="sxs-lookup"><span data-stu-id="6936f-107">Updating Resources</span></span>

<span data-ttu-id="6936f-108">下列範例會依照下列步驟，將一個可執行檔 Hand.exe 中的對話方塊資源複製到另一個可執行檔 Foot.exe：</span><span class="sxs-lookup"><span data-stu-id="6936f-108">The following example copies a dialog box resource from one executable file, Hand.exe, to another, Foot.exe, by following these steps:</span></span>

1.  <span data-ttu-id="6936f-109">您可以使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式，Hand.exe 載入可執行檔。</span><span class="sxs-lookup"><span data-stu-id="6936f-109">Use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load the executable file Hand.exe.</span></span>
2.  <span data-ttu-id="6936f-110">使用 [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) 和 [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) 函式來找出並載入對話方塊資源。</span><span class="sxs-lookup"><span data-stu-id="6936f-110">Use the [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) and [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) functions to locate and load the dialog box resource.</span></span>
3.  <span data-ttu-id="6936f-111">您可以使用 [**LockResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource) 函式來取得對話方塊資源資料的指標。</span><span class="sxs-lookup"><span data-stu-id="6936f-111">Use the [**LockResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource) function to retrieve a pointer to the dialog box resource data.</span></span>
4.  <span data-ttu-id="6936f-112">您可以使用 [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) 函式來開啟 Foot.exe 的更新控制碼。</span><span class="sxs-lookup"><span data-stu-id="6936f-112">Use the [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) function to open an update handle to Foot.exe.</span></span>
5.  <span data-ttu-id="6936f-113">使用 [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) 函式，將對話方塊資源從 Hand.exe 複製到 Foot.exe。</span><span class="sxs-lookup"><span data-stu-id="6936f-113">Use the [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) function to copy the dialog box resource from Hand.exe to Foot.exe.</span></span>
6.  <span data-ttu-id="6936f-114">使用 [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) 函數來完成更新。</span><span class="sxs-lookup"><span data-stu-id="6936f-114">Use the [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) function to complete the update.</span></span>

<span data-ttu-id="6936f-115">下列程式碼會執行這些步驟。</span><span class="sxs-lookup"><span data-stu-id="6936f-115">The following code implements these steps.</span></span>

<span data-ttu-id="6936f-116">**安全性警告：** 不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="6936f-116">**Security Warning:** Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="6936f-117">請參閱 **LoadLibrary** 檔，以取得如何使用不同版本的 Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6936f-117">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```C++
HGLOBAL hResLoad;   // handle to loaded resource
HMODULE hExe;       // handle to existing .EXE file
HRSRC hRes;         // handle/ptr. to res. info. in hExe
HANDLE hUpdateRes;  // update resource handle
LPVOID lpResLock;   // pointer to resource data
BOOL result;
#define IDD_HAND_ABOUTBOX   103
#define IDD_FOOT_ABOUTBOX   110

// Load the .EXE file that contains the dialog box you want to copy.
hExe = LoadLibrary(TEXT("hand.exe"));
if (hExe == NULL)
{
    ErrorHandler(TEXT("Could not load exe."));
    return;
}

// Locate the dialog box resource in the .EXE file.
hRes = FindResource(hExe, MAKEINTRESOURCE(IDD_HAND_ABOUTBOX), RT_DIALOG);
if (hRes == NULL)
{
    ErrorHandler(TEXT("Could not locate dialog box."));
    return;
}

// Load the dialog box into global memory.
hResLoad = LoadResource(hExe, hRes);
if (hResLoad == NULL)
{
    ErrorHandler(TEXT("Could not load dialog box."));
    return;
}

// Lock the dialog box into global memory.
lpResLock = LockResource(hResLoad);
if (lpResLock == NULL)
{
    ErrorHandler(TEXT("Could not lock dialog box."));
    return;
}

// Open the file to which you want to add the dialog box resource.
hUpdateRes = BeginUpdateResource(TEXT("foot.exe"), FALSE);
if (hUpdateRes == NULL)
{
    ErrorHandler(TEXT("Could not open file for writing."));
    return;
}

// Add the dialog box resource to the update list.
result = UpdateResource(hUpdateRes,    // update resource handle
    RT_DIALOG,                         // change dialog box resource
    MAKEINTRESOURCE(IDD_FOOT_ABOUTBOX),         // dialog box id
    MAKELANGID(LANG_NEUTRAL, SUBLANG_NEUTRAL),  // neutral language
    lpResLock,                         // ptr to resource info
    SizeofResource(hExe, hRes));       // size of resource info

if (result == FALSE)
{
    ErrorHandler(TEXT("Could not add resource."));
    return;
}

// Write changes to FOOT.EXE and then close it.
if (!EndUpdateResource(hUpdateRes, FALSE))
{
    ErrorHandler(TEXT("Could not write changes to file."));
    return;
}

// Clean up.
if (!FreeLibrary(hExe))
{
    ErrorHandler(TEXT("Could not free executable."));
    return;
}
```



## <a name="creating-a-resource-list"></a><span data-ttu-id="6936f-118">建立資源清單</span><span class="sxs-lookup"><span data-stu-id="6936f-118">Creating a Resource List</span></span>

<span data-ttu-id="6936f-119">下列範例會建立 Hand.exe 檔案中的每個資源清單。</span><span class="sxs-lookup"><span data-stu-id="6936f-119">The following example creates a list of every resource in the Hand.exe file.</span></span> <span data-ttu-id="6936f-120">清單會寫入 Resinfo.txt 檔案中。</span><span class="sxs-lookup"><span data-stu-id="6936f-120">The list is written to the Resinfo.txt file.</span></span>

<span data-ttu-id="6936f-121">此程式碼示範如何載入可執行檔、建立要在其中寫入資源資訊的檔案，以及呼叫 [**EnumResourceTypes**](/windows/desktop/api/Winbase/nf-winbase-enumresourcetypesa) 函式，將模組中找到的每個資源類型傳送至應用程式定義的回呼函數 `EnumTypesFunc` 。</span><span class="sxs-lookup"><span data-stu-id="6936f-121">The code demonstrates how to load the executable file, create a file in which to write resource information, and call the [**EnumResourceTypes**](/windows/desktop/api/Winbase/nf-winbase-enumresourcetypesa) function to send each resource type found in the module to the application-defined callback function `EnumTypesFunc`.</span></span> <span data-ttu-id="6936f-122">如需此類型之回呼函數的詳細資訊，請參閱 [*EnumResTypeProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca) 。</span><span class="sxs-lookup"><span data-stu-id="6936f-122">See [*EnumResTypeProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca) for information on callback functions of this type.</span></span> <span data-ttu-id="6936f-123">這個回呼函式會使用 [**EnumResourceNames**](/windows/desktop/api/libloaderapi/nf-libloaderapi-enumresourcenamesa) 函式，將指定類型內每個資源的名稱傳遞給另一個應用程式定義的回呼函數 `EnumNamesFunc` 。</span><span class="sxs-lookup"><span data-stu-id="6936f-123">This callback function uses the [**EnumResourceNames**](/windows/desktop/api/libloaderapi/nf-libloaderapi-enumresourcenamesa) function to pass the name of every resource within the specified type to another application-defined callback function, `EnumNamesFunc`.</span></span> <span data-ttu-id="6936f-124">如需此類型之回呼函數的詳細資訊，請參閱 [*EnumResNameProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca) 。</span><span class="sxs-lookup"><span data-stu-id="6936f-124">See [*EnumResNameProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca) for information on callback functions of this type.</span></span> <span data-ttu-id="6936f-125">`EnumNamesFunc` 使用 [**EnumResourceLanguages**](/windows/desktop/api/Winbase/nf-winbase-enumresourcelanguagesa) 函式，將指定之類型和名稱的每個資源的語言傳遞給第三個回呼函數 `EnumLangsFunc` 。</span><span class="sxs-lookup"><span data-stu-id="6936f-125">`EnumNamesFunc` uses the [**EnumResourceLanguages**](/windows/desktop/api/Winbase/nf-winbase-enumresourcelanguagesa) function to pass the language of every resource of the specified type and name to a third callback function, `EnumLangsFunc`.</span></span> <span data-ttu-id="6936f-126">如需此類型之回呼函數的詳細資訊，請參閱 [*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="6936f-126">See [*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85)) for information on callback functions of this type.</span></span> <span data-ttu-id="6936f-127">`EnumLangsFunc` 將指定之類型、名稱和語言的資源相關資訊寫入 Resinfo.txt 檔。</span><span class="sxs-lookup"><span data-stu-id="6936f-127">`EnumLangsFunc` writes information about the resource of the specified type, name, and language to the Resinfo.txt file.</span></span>

<span data-ttu-id="6936f-128">請注意， [*EnumResTypeProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca)中的 *LPSZTYPE* 是資源識別碼或指向字串 (的指標，其中包含資源識別碼或類型名稱) ;[*EnumResNameProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca)和 [*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))中的 *lpszType* 和 *lpszName* 很類似。</span><span class="sxs-lookup"><span data-stu-id="6936f-128">Note that the *lpszType* in [*EnumResTypeProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca) is either a resource ID or a pointer to a string (containing a resource ID or type name); *lpszType* and *lpszName* in [*EnumResNameProc*](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca) and [*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85)) are similar.</span></span> <span data-ttu-id="6936f-129">若要載入列舉的資源，請直接呼叫適當的函式。</span><span class="sxs-lookup"><span data-stu-id="6936f-129">To load an enumerated resource, just call the appropriate function.</span></span> <span data-ttu-id="6936f-130">例如，如果已列舉) 的功能表資源 (**RT \_ 功能表** ，則將 *lpszName* 傳遞至 [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)。</span><span class="sxs-lookup"><span data-stu-id="6936f-130">For example, if a menu resource (**RT\_MENU**) was enumerated, then pass *lpszName* to [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua).</span></span> <span data-ttu-id="6936f-131">若為自訂資源，請將 *lpszType* 和 *LpszName* 傳遞至 [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea)。</span><span class="sxs-lookup"><span data-stu-id="6936f-131">For custom resources, pass *lpszType* and *lpszName* to [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea).</span></span>

<span data-ttu-id="6936f-132">[更新資源](#updating-resources)程式碼會遵循類似于對話方塊資源的模式。</span><span class="sxs-lookup"><span data-stu-id="6936f-132">The [Updating Resources](#updating-resources) code follows a similar pattern for a dialog box resource.</span></span>

<span data-ttu-id="6936f-133">**安全性警告：** 不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="6936f-133">**Security Warning:** Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="6936f-134">請參閱 **LoadLibrary** 檔，以取得如何使用不同版本的 Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6936f-134">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```C++
HANDLE g_hFile;   // global handle to resource info file
// Declare callback functions.
BOOL EnumTypesFunc(
       HMODULE hModule,
       LPTSTR lpType,
       LONG lParam);
   
BOOL EnumNamesFunc(
       HMODULE hModule,
       LPCTSTR lpType,
       LPTSTR lpName,
       LONG lParam);
   
BOOL EnumLangsFunc(
       HMODULE hModule,
       LPCTSTR lpType,
       LPCTSTR lpName,
       WORD wLang,
       LONG lParam);
```




```C++
HMODULE hExe;        // handle to .EXE file
TCHAR szBuffer[80];  // print buffer for info file
DWORD cbWritten;     // number of bytes written to resource info file
size_t cbString;     // length of string in szBuffer
HRESULT hResult;

// Load the .EXE whose resources you want to list.
hExe = LoadLibrary(TEXT("hand.exe"));
if (hExe == NULL)
{
    // Add code to fail as securely as possible.
    return;
}

// Create a file to contain the resource info.
g_hFile = CreateFile(TEXT("resinfo.txt"),   // name of file
    GENERIC_READ | GENERIC_WRITE,      // access mode
    0,                                 // share mode
    (LPSECURITY_ATTRIBUTES) NULL,      // default security
    CREATE_ALWAYS,                     // create flags
    FILE_ATTRIBUTE_NORMAL,             // file attributes
    (HANDLE) NULL);                    // no template
if (g_hFile == INVALID_HANDLE_VALUE)
{
    ErrorHandler(TEXT("Could not open file."));
    return;
}

// Find all of the loaded file's resources.
hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR),
    TEXT("The file contains the following resources:\r\n\r\n"));
if (FAILED(hResult))
{
    // Add code to fail as securely as possible.
    return;
}

hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
if (FAILED(hResult))
{
    // Add code to fail as securely as possible.
    return;
}

WriteFile(g_hFile,       // file to hold resource info
    szBuffer,            // what to write to the file
    (DWORD) cbString,    // number of bytes in szBuffer
    &cbWritten,          // number of bytes written
    NULL);               // no overlapped I/O

EnumResourceTypes(hExe,              // module handle
    (ENUMRESTYPEPROC)EnumTypesFunc,  // callback function
    0);                              // extra parameter

// Unload the executable file whose resources were
// enumerated and close the file created to contain
// the resource information.
FreeLibrary(hExe);
CloseHandle(g_hFile);
```




```C++
//    FUNCTION: EnumTypesFunc(HANDLE, LPSTR, LONG)
//
//    PURPOSE:  Resource type callback
BOOL EnumTypesFunc(
        HMODULE hModule,  // module handle
        LPTSTR lpType,    // address of resource type
        LONG lParam)      // extra parameter, could be
                          // used for error checking
{
    TCHAR szBuffer[80];  // print buffer for info file
    DWORD cbWritten;     // number of bytes written to resource info file
    size_t cbString;
    HRESULT hResult;

    // Write the resource type to a resource information file.
    // The type may be a string or an unsigned decimal
    // integer, so test before printing.
    if (!IS_INTRESOURCE(lpType))
    {
        hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("Type: %s\r\n"), lpType);
        if (FAILED(hResult))
        {
            // Add code to fail as securely as possible.
            return FALSE;
        }
    }
    else
    {
        hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("Type: %u\r\n"), (USHORT)lpType);
        if (FAILED(hResult))
        {
            // Add code to fail as securely as possible.
            return FALSE;
        }
    }

    hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    WriteFile(g_hFile, szBuffer, (DWORD) cbString, &cbWritten, NULL);
    // Find the names of all resources of type lpType.
    EnumResourceNames(hModule,
        lpType,
        (ENUMRESNAMEPROC)EnumNamesFunc,
        0);

    return TRUE;
}

//    FUNCTION: EnumNamesFunc(HANDLE, LPSTR, LPSTR, LONG)
//
//    PURPOSE:  Resource name callback
BOOL EnumNamesFunc(
        HMODULE hModule,  // module handle
        LPCTSTR lpType,   // address of resource type
        LPTSTR lpName,    // address of resource name
        LONG lParam)      // extra parameter, could be
                          // used for error checking
{
    TCHAR szBuffer[80];  // print buffer for info file
    DWORD cbWritten;     // number of bytes written to resource info file
    size_t cbString;
    HRESULT hResult;

    // Write the resource name to a resource information file.
    // The name may be a string or an unsigned decimal
    // integer, so test before printing.
    if (!IS_INTRESOURCE(lpName))
    {
        hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("\tName: %s\r\n"), lpName);
        if (FAILED(hResult))
        {
            // Add code to fail as securely as possible.
            return FALSE;
        }
    }
    else
    {
        hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("\tName: %u\r\n"), (USHORT)lpName);
        if (FAILED(hResult))
        {
            // Add code to fail as securely as possible.
            return FALSE;
        }
    }

    hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }
   
    WriteFile(g_hFile, szBuffer, (DWORD) cbString, &cbWritten, NULL);
    // Find the languages of all resources of type
    // lpType and name lpName.
    EnumResourceLanguages(hModule,
        lpType,
        lpName,
        (ENUMRESLANGPROC)EnumLangsFunc,
        0);

    return TRUE;
}

//    FUNCTION: EnumLangsFunc(HANDLE, LPSTR, LPSTR, WORD, LONG)
//
//    PURPOSE:  Resource language callback
BOOL EnumLangsFunc(
        HMODULE hModule, // module handle
        LPCTSTR lpType,  // address of resource type
        LPCTSTR lpName,  // address of resource name
        WORD wLang,      // resource language
        LONG lParam)     // extra parameter, could be
                         // used for error checking
{
    HRSRC hResInfo;
    TCHAR szBuffer[80];  // print buffer for info file
    DWORD cbWritten;     // number of bytes written to resource info file
    size_t cbString;
    HRESULT hResult;

    hResInfo = FindResourceEx(hModule, lpType, lpName, wLang);
    // Write the resource language to the resource information file.
    hResult = StringCchPrintf(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), TEXT("\t\tLanguage: %u\r\n"), (USHORT) wLang);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    WriteFile(g_hFile, szBuffer, (DWORD) cbString, &cbWritten, NULL); 
    // Write the resource handle and size to buffer.
    hResult = StringCchPrintf(szBuffer,
        sizeof(szBuffer)/sizeof(TCHAR),
        TEXT("\t\thResInfo == %lx,  Size == %lu\r\n\r\n"),
        hResInfo,
        SizeofResource(hModule, hResInfo));
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    hResult = StringCchLength(szBuffer, sizeof(szBuffer)/sizeof(TCHAR), &cbString);
    if (FAILED(hResult))
    {
        // Add code to fail as securely as possible.
        return FALSE;
    }

    WriteFile(g_hFile, szBuffer, (DWORD)cbString, &cbWritten, NULL);
    return TRUE;
}
```



 

 