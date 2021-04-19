---
description: C + + 範例顯示如何顯示每個磁片區和裝置的所有路徑。 針對系統中的每個磁片區，此範例會尋找磁片區、取得裝置名稱、取得該磁片區的所有路徑，並顯示路徑。
ms.assetid: a9ee8cc8-fa62-4fc9-aa69-35ee98afe417
title: 顯示磁片區路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f4a9fcb032099b3cb2456d4bf2193b55f4580
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981025"
---
# <a name="displaying-volume-paths"></a><span data-ttu-id="68ab2-104">顯示磁片區路徑</span><span class="sxs-lookup"><span data-stu-id="68ab2-104">Displaying Volume Paths</span></span>

<span data-ttu-id="68ab2-105">下列 c + + 範例顯示如何顯示每個磁片區和裝置的所有路徑。</span><span class="sxs-lookup"><span data-stu-id="68ab2-105">The following C++ example shows how to display all paths for each volume and device.</span></span> <span data-ttu-id="68ab2-106">針對系統中的每個磁片區，此範例會尋找磁片區、取得裝置名稱、取得該磁片區的所有路徑，並顯示路徑。</span><span class="sxs-lookup"><span data-stu-id="68ab2-106">For each volume in the system, the example locates the volume, obtains the device name, obtains all paths for that volume, and displays the paths.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void DisplayVolumePaths(
        __in PWCHAR VolumeName
        )
{
    DWORD  CharCount = MAX_PATH + 1;
    PWCHAR Names     = NULL;
    PWCHAR NameIdx   = NULL;
    BOOL   Success   = FALSE;

    for (;;) 
    {
        //
        //  Allocate a buffer to hold the paths.
        Names = (PWCHAR) new BYTE [CharCount * sizeof(WCHAR)];

        if ( !Names ) 
        {
            //
            //  If memory can't be allocated, return.
            return;
        }

        //
        //  Obtain all of the paths
        //  for this volume.
        Success = GetVolumePathNamesForVolumeNameW(
            VolumeName, Names, CharCount, &CharCount
            );

        if ( Success ) 
        {
            break;
        }

        if ( GetLastError() != ERROR_MORE_DATA ) 
        {
            break;
        }

        //
        //  Try again with the
        //  new suggested size.
        delete [] Names;
        Names = NULL;
    }

    if ( Success )
    {
        //
        //  Display the various paths.
        for ( NameIdx = Names; 
              NameIdx[0] != L'\0'; 
              NameIdx += wcslen(NameIdx) + 1 ) 
        {
            wprintf(L"  %s", NameIdx);
        }
        wprintf(L"\n");
    }

    if ( Names != NULL ) 
    {
        delete [] Names;
        Names = NULL;
    }

    return;
}

void __cdecl wmain(void)
{
    DWORD  CharCount            = 0;
    WCHAR  DeviceName[MAX_PATH] = L"";
    DWORD  Error                = ERROR_SUCCESS;
    HANDLE FindHandle           = INVALID_HANDLE_VALUE;
    BOOL   Found                = FALSE;
    size_t Index                = 0;
    BOOL   Success              = FALSE;
    WCHAR  VolumeName[MAX_PATH] = L"";

    //
    //  Enumerate all volumes in the system.
    FindHandle = FindFirstVolumeW(VolumeName, ARRAYSIZE(VolumeName));

    if (FindHandle == INVALID_HANDLE_VALUE)
    {
        Error = GetLastError();
        wprintf(L"FindFirstVolumeW failed with error code %d\n", Error);
        return;
    }

    for (;;)
    {
        //
        //  Skip the \\?\ prefix and remove the trailing backslash.
        Index = wcslen(VolumeName) - 1;

        if (VolumeName[0]     != L'\\' ||
            VolumeName[1]     != L'\\' ||
            VolumeName[2]     != L'?'  ||
            VolumeName[3]     != L'\\' ||
            VolumeName[Index] != L'\\') 
        {
            Error = ERROR_BAD_PATHNAME;
            wprintf(L"FindFirstVolumeW/FindNextVolumeW returned a bad path: %s\n", VolumeName);
            break;
        }

        //
        //  QueryDosDeviceW does not allow a trailing backslash,
        //  so temporarily remove it.
        VolumeName[Index] = L'\0';

        CharCount = QueryDosDeviceW(&VolumeName[4], DeviceName, ARRAYSIZE(DeviceName)); 

        VolumeName[Index] = L'\\';

        if ( CharCount == 0 ) 
        {
            Error = GetLastError();
            wprintf(L"QueryDosDeviceW failed with error code %d\n", Error);
            break;
        }

        wprintf(L"\nFound a device:\n %s", DeviceName);
        wprintf(L"\nVolume name: %s", VolumeName);
        wprintf(L"\nPaths:");
        DisplayVolumePaths(VolumeName);

        //
        //  Move on to the next volume.
        Success = FindNextVolumeW(FindHandle, VolumeName, ARRAYSIZE(VolumeName));

        if ( !Success ) 
        {
            Error = GetLastError();

            if (Error != ERROR_NO_MORE_FILES) 
            {
                wprintf(L"FindNextVolumeW failed with error code %d\n", Error);
                break;
            }

            //
            //  Finished iterating
            //  through all the volumes.
            Error = ERROR_SUCCESS;
            break;
        }
    }

    FindVolumeClose(FindHandle);
    FindHandle = INVALID_HANDLE_VALUE;

    return;
}
```



<span data-ttu-id="68ab2-107">以下是執行應用程式的範例輸出。</span><span class="sxs-lookup"><span data-stu-id="68ab2-107">The following is example output from running the application.</span></span> <span data-ttu-id="68ab2-108">針對每個磁片區，輸出中會包含磁片區裝置路徑、磁片區 GUID 路徑和磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="68ab2-108">For each volume, the output includes a volume device path, a volume GUID path, and a drive letter.</span></span>

``` syntax
Found a device:
 \Device\HarddiskVolume2
Volume name: \\?\Volume{4c1b02c1-d990-11dc-99ae-806e6f6e6963}\
Paths:  C:\

Found a device:
 \Device\CdRom0
Volume name: \\?\Volume{4c1b02c4-d990-11dc-99ae-806e6f6e6963}\
Paths:  D:\
```

## <a name="related-topics"></a><span data-ttu-id="68ab2-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="68ab2-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68ab2-110">**FindFirstVolume**</span><span class="sxs-lookup"><span data-stu-id="68ab2-110">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
</dt> <dt>

[<span data-ttu-id="68ab2-111">**FindNextVolume**</span><span class="sxs-lookup"><span data-stu-id="68ab2-111">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
</dt> <dt>

[<span data-ttu-id="68ab2-112">**FindVolumeClose**</span><span class="sxs-lookup"><span data-stu-id="68ab2-112">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)
</dt> <dt>

[<span data-ttu-id="68ab2-113">**GetVolumePathNamesForVolumeName**</span><span class="sxs-lookup"><span data-stu-id="68ab2-113">**GetVolumePathNamesForVolumeName**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamesforvolumenamew)
</dt> <dt>

[<span data-ttu-id="68ab2-114">**QueryDosDevice**</span><span class="sxs-lookup"><span data-stu-id="68ab2-114">**QueryDosDevice**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew)
</dt> </dl>

 

 



