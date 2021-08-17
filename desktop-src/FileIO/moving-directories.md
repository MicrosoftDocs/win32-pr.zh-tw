---
description: 若要將目錄移至另一個位置，以及其中包含的檔案和子目錄，請呼叫 MoveFileEx、MoveFileWithProgress 或 MoveFileTransacted 函數。
ms.assetid: ca56c109-d6a3-456e-956c-126ce4aee8ba
title: 移動目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da891e22c2840ad9460f5fb43c8cc1b130905b86de80a988be2eeeb9a4010ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951137"
---
# <a name="moving-directories"></a>移動目錄

若要將目錄移至另一個位置，以及其中包含的檔案和子目錄，請呼叫 [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)、 [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)或 [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) 函數。 [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)函式的功能與 [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)相同，不同之處在于 **MoveFileWithProgress** 可讓您指定回呼常式，以接收作業進度的通知。 [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda)函式可讓您將作業當作交易作業來執行。

下列範例示範如何使用 [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) 函數搭配目錄。


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    printf("\n");
    if( argc != 3 )
    {
        printf("ERROR:  Incorrect number of arguments\n\n");
        printf("Description:\n");
        printf("  Moves a directory and its contents\n\n");
        printf("Usage:\n");
        _tprintf(TEXT("  %s [source_dir] [target_dir]\n\n"), argv[0]);
        printf("  The target directory cannot exist already.\n\n");
        return;
    }

    // Move the source directory to the target directory location.
    // The target directory must be on the same drive as the source.
    // The target directory cannot already exist.

    if (!MoveFileEx(argv[1], argv[2], MOVEFILE_WRITE_THROUGH))
    { 
        printf ("MoveFileEx failed with error %d\n", GetLastError());
        return;
    }
    else _tprintf(TEXT("%s has been moved to %s\n"), argv[1], argv[2]);
}
```



 

 



