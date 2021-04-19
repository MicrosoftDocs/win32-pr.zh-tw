---
description: 安裝程式物件的 MsiGetPatchFileList 函式和 PatchFiles 屬性會取得 Windows Installer 修補程式 ( .msp 檔) 的清單，並傳回可由修補程式更新的檔案清單。
ms.assetid: cc2eb506-c1fc-4125-b98c-12221b918e23
title: 列出可更新的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c15872cce902f5a9059d4256e9e5c30ecff213f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978016"
---
# <a name="listing-the-files-that-can-be-updated"></a>列出可更新的檔案

[**安裝程式物件**](installer-object.md)的 [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)函式和 [**PatchFiles**](installer-patchfiles.md)屬性會取得 Windows Installer 修補程式 ( .msp 檔) 的清單，並傳回可由修補程式更新的檔案清單。 從 Windows Installer 4.0 開始，可以使用 [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) 函數和 [**PatchFiles**](installer-patchfiles.md) 屬性。

## <a name="listing-files-that-can-be-updated"></a>列出可更新的檔案

下列範例示範如何使用 [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)，將 Windows Installer 修補程式 ( .msp 檔案清單中的適用性資訊解壓縮) 。 **MsiGetPatchFileList** 函式會提供修補程式目標的產品代碼，以及以分號分隔的 .msp 檔清單。 此範例需要在 Windows Vista 上執行 Windows Installer 4.0。


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")
#pragma comment(lib, "shell32.lib")

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles);

int __cdecl main()
{
    UINT uiRet = ERROR_SUCCESS;
    int argc;
    WCHAR** argv = CommandLineToArgvW(GetCommandLine(), &argc);
    
    MSIHANDLE *phFileListRec = NULL;
    DWORD dwcFiles = 0;
    WCHAR* szProductCode = argv[1];
    WCHAR* szPatchFileList = argv[2];
    if(ERROR_SUCCESS != (uiRet = MsiGetPatchFileList(szProductCode, szPatchFileList, &dwcFiles, &phFileListRec)))
    {
        printf("MsiGetPatchFileListW(%S, ...) Failed with:%d", szProductCode, uiRet);
        return uiRet;
    }
    
    DWORD cchBuf = 1;
    DWORD cchBufSize = 1;
    WCHAR* szBuf = new WCHAR[cchBufSize];
    if (!szBuf)
    {
        printf("Failed to allocate memory");
        CloseMsiHandles(phFileListRec, dwcFiles);
        return ERROR_OUTOFMEMORY;
    }
    memset(szBuf, 0, sizeof(WCHAR)*cchBufSize);
    
    for(unsigned int i = 0; i < dwcFiles; i++)
    {
        cchBuf = cchBufSize;
        while(ERROR_MORE_DATA == (uiRet = MsiRecordGetString(phFileListRec[i], 0, szBuf, &cchBuf)))
        {
            if (szBuf)
                delete[] szBuf;
            cchBufSize = ++cchBuf;
            szBuf = new WCHAR[cchBufSize];
            if (!szBuf)
            {
                printf("Failed to allocate memory");
                CloseMsiHandles(phFileListRec, dwcFiles);
                return ERROR_OUTOFMEMORY;
            }
        }
        
        if(uiRet != ERROR_SUCCESS)
        {
            printf("MsiRecordGetString(phFileListRec[%d] with %d", i, uiRet);
            CloseMsiHandles(phFileListRec, dwcFiles);
            if (szBuf)
                delete[] szBuf;
            return uiRet;
        }
        else
        {
            printf("File %d:%S\n", i, szBuf);
        }            
    }

    CloseMsiHandles(phFileListRec, dwcFiles);
    if (szBuf)
        delete[] szBuf;
    return 0;
}

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles)
{
    if (!phFileListRec)
        return;
    
    for (unsigned int i = 0; i < dwcFiles; i++)
    {
        if (phFileListRec[i])
            MsiCloseHandle(phFileListRec[i]);
    }    
}
//
```



下列範例示範如何使用 [**安裝程式物件**](installer-object.md)的 [**PatchFiles**](installer-patchfiles.md)屬性，將 Windows Installer 修補程式 ( .msp 檔案清單中的適用性資訊解壓縮) 。 **PatchFiles** 屬性會提供修補程式目標的產品代碼，以及以分號分隔的 .msp 檔清單。 此範例需要在 Windows Vista 上執行 Windows Installer 4.0。


```VB
Dim FileList
Dim installer : Set installer = Nothing
Dim argCount:argCount = Wscript.Arguments.Count

Set installer = Wscript.CreateObject("WindowsInstaller.Installer")

If (argCount > 0) Then
    sProdCode = Wscript.Arguments(0)
    sPatchPckgPath = Wscript.Arguments(1)
    Set FileList = installer.PatchFiles (sProdCode, sPatchPckgPath)
    For each File in FileList
           Wscript.Echo "Affected file: " & File
    Next
Else
    Usage
End If

Sub Usage
    Wscript.Echo "Windows Installer utility to list files updated by a patch for an installed product" &_
    vbNewLine & " 1st argument is the product code (GUID) of an installed product" &_
    vbNewLine & " 2nd argument is the list of patches" &_
    vbNewLine &_
    vbNewLine & "Copyright (C) Microsoft. All rights reserved."
    Wscript.Quit 1
End Sub
```



 

 



