---
description: 檔案系統辨識功能能夠辨識包含尚未定義之有效檔案系統/磁片區配置的存放媒體，但是媒體能夠透過 Windows 在內部定義的辨識結構來識別本身。
ms.assetid: 23ed6de0-25ff-4841-91f6-94b487dee613
title: 取得檔案系統識別資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cafa9f1c7cf6cbbe11d434aff3db424a1cd0a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318692"
---
# <a name="obtaining-file-system-recognition-information"></a><span data-ttu-id="c2d09-103">取得檔案系統識別資訊</span><span class="sxs-lookup"><span data-stu-id="c2d09-103">Obtaining File System Recognition Information</span></span>

<span data-ttu-id="c2d09-104">[檔案系統](file-system-recognition.md) 辨識功能能夠辨識包含尚未定義之有效檔案系統/磁片區配置的存放媒體，但是媒體能夠透過 Windows 在內部定義的辨識結構來識別本身。</span><span class="sxs-lookup"><span data-stu-id="c2d09-104">[File system recognition](file-system-recognition.md) is the ability to recognize storage media that contain a valid file system/volume layout that has not been defined yet, but the media is able to identify itself through the presence of the recognition structure defined internally by Windows.</span></span>

<span data-ttu-id="c2d09-105">由於沒有任何現有的檔案系統會辨識新的磁片配置，因此「原始」檔案系統會掛接磁片區，並提供直接封鎖層級的存取。</span><span class="sxs-lookup"><span data-stu-id="c2d09-105">Because no existing file system will recognize a new disk layout, the "RAW" file system will mount the volume and provide direct block level access.</span></span> <span data-ttu-id="c2d09-106">「原始」檔案系統（併入 *ntoskrnl.exe*）將能夠讀取檔案系統辨識結構，並透過檔案系統控制要求 [**FSCTL \_ 查詢 \_ 檔 \_ 系統 \_ 識別**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)，提供對這類結構的應用程式存取權，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="c2d09-106">The "RAW" file system, incorporated in *NtosKrnl*, will have the ability to read the file system recognition structure and provide applications access to such structures through the file system control request [**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), shown in the following example.</span></span>


```C++
STDMETHODIMP CheckFileSystem(
    PCWSTR pcwszDrive
    ) 
{
    HRESULT hr = S_OK;
    HANDLE  hDisk = INVALID_HANDLE_VALUE;
    BOOL    fResult = FALSE;    
    ULONG   BytesReturned = 0;    
    FILE_SYSTEM_RECOGNITION_INFORMATION     FsRi = {0};
    
    //
    // Open the target, for example "\\.\C:"
    //
    wprintf( L"CreateFile on %s...", pcwszDrive );
    hDisk = CreateFile( pcwszDrive, 
                        FILE_READ_ATTRIBUTES|SYNCHRONIZE|FILE_TRAVERSE,                        
                        FILE_SHARE_READ|FILE_SHARE_WRITE,
                        NULL, OPEN_EXISTING, 0, NULL );    
    if( hDisk == INVALID_HANDLE_VALUE ) 
    {
        hr = HRESULT_FROM_WIN32( GetLastError() );
        wprintf( L"CreateFile failed on %s, GLE = 0x%x\n", pcwszDrive, GetLastError() );
        goto exit;
    }
    wprintf( L"succeeded.\n\n" );

    wprintf( L"\nPress Any Key to send down the FSCTL\n" );
    _getwch();

    //
    // Send down the FSCTL
    //
    wprintf( L"Calling DeviceIoControl( FSCTL_QUERY_FILE_SYSTEM_RECOGNITION ) " );
    
    fResult = DeviceIoControl( hDisk, 
                               FSCTL_QUERY_FILE_SYSTEM_RECOGNITION, 
                               NULL, 
                               0, 
                               &FsRi, 
                               sizeof(FsRi), 
                               &BytesReturned, 
                               NULL );
    if( !fResult ) 
    {
        hr = HRESULT_FROM_WIN32( GetLastError() );
        wprintf( L"failed GLE = 0x%x\n", GetLastError() );
        goto exit;
    }
    wprintf( L"succeeded.\n\n" );

    wprintf( L"FSCTL_QUERY_FILE_SYSTEM_RECOGNITION returned success.\n" );

    wprintf( L"FSCTL_QUERY_FILE_SYSTEM_RECOGNITION retrieved \"%S\".\n",
              FsRi.FileSystem );

exit:

    if( hDisk != INVALID_HANDLE_VALUE ) 
    {
        CloseHandle( hDisk );
        hDisk = INVALID_HANDLE_VALUE;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c2d09-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2d09-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2d09-108">檔案系統識別</span><span class="sxs-lookup"><span data-stu-id="c2d09-108">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="c2d09-109">**檔 \_ 系統 \_ 識別 \_ 結構**</span><span class="sxs-lookup"><span data-stu-id="c2d09-109">**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**</span></span>](file-system-recognition-structure.md)
</dt> <dt>

[<span data-ttu-id="c2d09-110">**FSCTL \_ 查詢 \_ 檔 \_ 系統 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="c2d09-110">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

 
