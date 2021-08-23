---
description: 檔案系統辨識功能能夠辨識包含尚未定義之有效檔案系統/磁片區配置的存放媒體，但是媒體可透過 Windows 在內部定義的辨識結構來識別本身。
ms.assetid: 23ed6de0-25ff-4841-91f6-94b487dee613
title: 取得檔案系統識別資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c10b538f9e98ecab3f8f8f72784ef658c068f780388dc7b600be68b76380757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148502"
---
# <a name="obtaining-file-system-recognition-information"></a>取得檔案系統識別資訊

[檔案系統](file-system-recognition.md)辨識功能能夠辨識包含尚未定義之有效檔案系統/磁片區配置的存放媒體，但是媒體可透過 Windows 在內部定義的辨識結構來識別本身。

由於沒有任何現有的檔案系統會辨識新的磁片配置，因此「原始」檔案系統會掛接磁片區，並提供直接封鎖層級的存取。 「原始」檔案系統（併入 *ntoskrnl.exe*）將能夠讀取檔案系統辨識結構，並透過檔案系統控制要求 [**FSCTL \_ 查詢 \_ 檔 \_ 系統 \_ 識別**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)，提供對這類結構的應用程式存取權，如下列範例所示。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案系統識別](file-system-recognition.md)
</dt> <dt>

[**檔 \_ 系統 \_ 識別 \_ 結構**](file-system-recognition-structure.md)
</dt> <dt>

[**FSCTL \_ 查詢 \_ 檔 \_ 系統 \_ 識別**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

 
