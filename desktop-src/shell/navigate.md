---
description: 您現在已擁有在命名空間中的任何位置流覽所需的所有必要元素。
ms.assetid: bd9f903d-bea6-494f-af81-d90457dc2647
title: 流覽命名空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2778fc21df12e9228f9335a52c04556e97563cba5f8a4cb6b82eb779944c451
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111478"
---
# <a name="navigating-the-namespace"></a>流覽命名空間

您現在已擁有在命名空間中的任何位置流覽所需的所有必要元素。 最簡單的開始方式是讓您的應用程式呼叫 [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) ，以取得桌面的 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。 然後，若要向下流覽命名空間，您的應用程式可以遵循下列步驟：

1.  列舉資料夾的內容。
2.  判斷哪些物件是子資料夾，然後選取其中一個。
3.  系結至子資料夾，以取出其 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。

視需要重複執行這些步驟以達到目標。

## <a name="a-simple-example-of-namespace-navigation"></a>命名空間導覽的簡單範例

下列範例程式碼是一個簡單的主控台應用程式，說明上述各節所討論的一些程式。 為了清楚起見，已省略錯誤檢查。 此應用程式會執行下列工作：

1.  [使用 IShellFolder 介面](folder-info.md))  (抓取 Program Files 資料夾的 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)介面。
2.  列舉資料夾的內容， ([列舉資料夾](folder-info.md)) 的內容。
3.  決定所有顯示名稱，並將它們列印 ([判斷) 顯示名稱和其他屬性](folder-info.md) 。
4.  尋找子資料夾 ([取得子資料夾 IShellFolder 介面的指標](folder-info.md)) 。
5.  系結到它所找到的第一個子資料夾， ([取得子資料夾 IShellFolder 介面的指標](folder-info.md)) 。
6.  在子資料夾中列印物件的顯示名稱。


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>

main()
{
    LPITEMIDLIST pidlProgFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfFirstFolder = NULL;
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfProgFiles = NULL;
    LPENUMIDLIST ppenum = NULL;
    ULONG celtFetched;
    HRESULT hr;
    STRRET strDispName;
    TCHAR pszDisplayName[MAX_PATH];
    ULONG uAttr;
   
    CoInitialize( NULL );
    
    hr = SHGetFolderLocation(NULL, CSIDL_PROGRAM_FILES, NULL, 0, &pidlProgFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlProgFiles, NULL, IID_IShellFolder, (LPVOID *) &psfProgFiles);
    psfDeskTop->Release();

    hr = psfProgFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfProgFiles->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
        cout << pszDisplayName << '\n';
        if(!psfFirstFolder)
        {
            uAttr = SFGAO_FOLDER;
            psfProgFiles->GetAttributesOf(1, (LPCITEMIDLIST *) &pidlItems, &uAttr);
            if(uAttr & SFGAO_FOLDER)
            {
                hr = psfProgFiles->BindToObject(pidlItems, NULL, IID_IShellFolder, (LPVOID *) &psfFirstFolder);
            }
        }
        CoTaskMemFree(pidlItems);
    }

    cout << "\n\n";

    ppenum->Release();

    if(psfFirstFolder)
    {
        hr = psfFirstFolder->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

        while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
        {
            psfFirstFolder->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
            StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
            cout << pszDisplayName << '\n';
            CoTaskMemFree(pidlItems);
        }
    }

    ppenum->Release();
    CoTaskMemFree(pidlProgFiles);
    psfProgFiles->Release();
    psfFirstFolder->Release();

    CoUninitialize();
    return 0;
}
```



 

 
