---
description: 自訂使用者介面可以內嵌在 Windows Installer 套件中。
ms.assetid: d037cd8d-9c88-4851-a9da-b2179f53cee6
title: 使用內嵌 UI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f187e50461cfe88adc9c2cabbf8dd8b88ca97a5a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104035239"
---
# <a name="using-an-embedded-ui"></a><span data-ttu-id="8ea5a-103">使用內嵌 UI</span><span class="sxs-lookup"><span data-stu-id="8ea5a-103">Using an Embedded UI</span></span>

<span data-ttu-id="8ea5a-104">自訂使用者介面可以內嵌在 Windows Installer 套件中。</span><span class="sxs-lookup"><span data-stu-id="8ea5a-104">A custom user interface can be embedded within the Windows Installer package.</span></span>

<span data-ttu-id="8ea5a-105">包含自訂 UI 的 DLL 檔案，以及自訂 UI 所使用的任何資源檔，都應該列在 [MsiEmbeddedUI](msiembeddedui-table.md) 資料表中。</span><span class="sxs-lookup"><span data-stu-id="8ea5a-105">The DLL file containing the custom UI, and any resource files used by the custom UI, should be listed in the [MsiEmbeddedUI](msiembeddedui-table.md) table.</span></span> <span data-ttu-id="8ea5a-106">例如，此 MsiEmbeddedUI 表包含包含內嵌 UI 之 DLL 檔案的資料列，以及 UI 所使用點陣圖檔案的資料列。</span><span class="sxs-lookup"><span data-stu-id="8ea5a-106">For example, this MsiEmbeddedUI table contains a row for the DLL file containing the embedded UI and a row for a bitmap file used by the UI.</span></span>

| <span data-ttu-id="8ea5a-107">MsiEmbeddedUI</span><span class="sxs-lookup"><span data-stu-id="8ea5a-107">MsiEmbeddedUI</span></span> | <span data-ttu-id="8ea5a-108">FileName</span><span class="sxs-lookup"><span data-stu-id="8ea5a-108">FileName</span></span>    | <span data-ttu-id="8ea5a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="8ea5a-109">Attributes</span></span> | <span data-ttu-id="8ea5a-110">MessageFilter</span><span class="sxs-lookup"><span data-stu-id="8ea5a-110">MessageFilter</span></span> | <span data-ttu-id="8ea5a-111">資料</span><span class="sxs-lookup"><span data-stu-id="8ea5a-111">Data</span></span>            |
|---------------|-------------|------------|---------------|-----------------|
| <span data-ttu-id="8ea5a-112">EmbeddedUI</span><span class="sxs-lookup"><span data-stu-id="8ea5a-112">EmbeddedUI</span></span>    | <span data-ttu-id="8ea5a-113">embedui.dll</span><span class="sxs-lookup"><span data-stu-id="8ea5a-113">embedui.dll</span></span> | <span data-ttu-id="8ea5a-114">3</span><span class="sxs-lookup"><span data-stu-id="8ea5a-114">3</span></span>          | <span data-ttu-id="8ea5a-115">201359327</span><span class="sxs-lookup"><span data-stu-id="8ea5a-115">201359327</span></span>     | <span data-ttu-id="8ea5a-116">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="8ea5a-116">\[Binary Data\]</span></span> |
| <span data-ttu-id="8ea5a-117">CustomBitmap</span><span class="sxs-lookup"><span data-stu-id="8ea5a-117">CustomBitmap</span></span>  | <span data-ttu-id="8ea5a-118">custom.bmp</span><span class="sxs-lookup"><span data-stu-id="8ea5a-118">custom.bmp</span></span>  | <span data-ttu-id="8ea5a-119">0</span><span class="sxs-lookup"><span data-stu-id="8ea5a-119">0</span></span>          |               | <span data-ttu-id="8ea5a-120">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="8ea5a-120">\[Binary Data\]</span></span> |



 

<span data-ttu-id="8ea5a-121">在此範例 embedui.dll 的自訂 UI DLL 應該匯出使用者定義的 *InitializeEmbeddedUI*、 *EmbeddedUIHandler* 和 *ShutdownEmbeddedUI* 函數。</span><span class="sxs-lookup"><span data-stu-id="8ea5a-121">The custom UI DLL, in this example embedui.dll, should export the user-defined *InitializeEmbeddedUI*, *EmbeddedUIHandler*, and *ShutdownEmbeddedUI* functions.</span></span> <span data-ttu-id="8ea5a-122">下列範例程式碼說明這些函數。</span><span class="sxs-lookup"><span data-stu-id="8ea5a-122">The following sample code illustrates these functions.</span></span>


```C++
#include <stdio.h>
#include <stdlib.h>
#include <windows.h>
#include <msi.h>
#include <msiquery.h>
#include <Aclapi.h>
#include <strsafe.h>
#pragma comment(lib, "msi.lib")

#define cchGUID 38

int __stdcall InitializeEmbeddedUI(MSIHANDLE hInstall, 
        LPCWSTR szResourcePath, LPDWORD pdwInternalUILevel)
{
    // The hInstall handle is only valid within this function and 
     // can be used to get or set properties. The handle 
    // does not need to be explicitly closed.

    WCHAR szProductCode[cchGUID+1];
    DWORD cchProductCode = ARRAYSIZE(szProductCode);
    UINT uiStat =  MsiGetProperty(hInstall, L"ProductCode",
             szProductCode, &cchProductCode);
    UNREFERENCED_PARAMETER(szResourcePath);

    if (ERROR_SUCCESS != uiStat)
    {
        // The installation should fail.
        return ERROR_INSTALL_FAILURE;
    }

    WCHAR* szReinstall = NULL;
    DWORD cchReinstall = 0;
    uiStat = MsiGetProperty(hInstall, TEXT("REINSTALL"),  
            szReinstall, &cchReinstall);
    if (ERROR_MORE_DATA == uiStat)
    {
        ++cchProductCode; // Add 1 for terminating null character.
        szReinstall = new WCHAR[cchReinstall];
        if (szReinstall)
        {
        uiStat = MsiGetProperty(hInstall, L"REINSTALL", 
                szReinstall, &cchReinstall);
        }
    }
    if (ERROR_SUCCESS != uiStat)
    {
        if (szReinstall != NULL) 
            delete [] szReinstall;
        // This installation should fail.
        return ERROR_INSTALL_FAILURE;
    }

    if (INSTALLSTATE_DEFAULT != MsiQueryProductState(szProductCode))
    {
        if (INSTALLUILEVEL_BASIC == *pdwInternalUILevel)
        {
            // Insert the custom UI used by basic installation here.
        }
        else
        {
            // Insert the custom UI used by full installation here.
        }
    }
    else if (szReinstall && szReinstall[0])
    {
        // Reinstall the UI sequence.
    }
    else
    {
        // This is a maintenance installation. Remove the UI sequence.

        MsiSetProperty(hInstall, TEXT("REMOVE"), TEXT("ALL"));
    }

    if (szProductCode)
        delete [] szReinstall;

    // Setting the internal UI level to none specifies that 
    // no authored UI should run.
    *pdwInternalUILevel = INSTALLUILEVEL_NONE;
    return 0;
}

DWORD __stdcall ShutdownEmbeddedUI()
{
    // ShutdownEmbeddedUI is optional. It can allow the embedded UI 
    // to perform any cleanup. After this call, the embedded UI   
    // should not receive any additional callbacks.
    return 0;
}


INT __stdcall EmbeddedUIHandler(UINT iMessageType, MSIHANDLE hRecord)
{
    // This function is similar to the MsiSetExternalUIRecord callback.
    INSTALLMESSAGE mt;
    UINT uiFlags;
    UNREFERENCED_PARAMETER(hRecord);

    mt = (INSTALLMESSAGE) (0xFF000000 & (UINT) iMessageType);
    uiFlags = 0x00FFFFFF & iMessageType;

    switch (mt)
    {
    case INSTALLMESSAGE_FATALEXIT:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_ERROR:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_WARNING:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_FILESINUSE:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_RESOLVESOURCE:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_USER:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_INFO:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_OUTOFDISKSPACE:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_ACTIONSTART:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_ACTIONDATA:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_PROGRESS:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_SHOWDIALOG:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_COMMONDATA:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_INSTALLSTART:
        {
            // This message is sent when the Install begins.
            // Record contains the ProductName and ProductCode
            return IDOK;
        }
    case INSTALLMESSAGE_INSTALLEND:
        {
            // This message is sent when the Install ends.
            // Record contains the ProductName and ProductCode 
            // and return value of the installation.
            return IDOK;
        }

    default:
        {
            return 0;
        }
    }
}
```



 

 



