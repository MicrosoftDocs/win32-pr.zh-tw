---
description: 您現在已擁有在命名空間中的任何位置流覽所需的所有必要元素。
ms.assetid: bd9f903d-bea6-494f-af81-d90457dc2647
title: 流覽命名空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24993369222fb32f9de6c79a0c998b1d7be9f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026334"
---
# <a name="navigating-the-namespace"></a><span data-ttu-id="c850c-103">流覽命名空間</span><span class="sxs-lookup"><span data-stu-id="c850c-103">Navigating the Namespace</span></span>

<span data-ttu-id="c850c-104">您現在已擁有在命名空間中的任何位置流覽所需的所有必要元素。</span><span class="sxs-lookup"><span data-stu-id="c850c-104">You now have all the essential elements needed to navigate anywhere in the namespace.</span></span> <span data-ttu-id="c850c-105">最簡單的開始方式是讓您的應用程式呼叫 [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) ，以取得桌面的 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。</span><span class="sxs-lookup"><span data-stu-id="c850c-105">The simplest way to start is to have your application call [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) to retrieve the desktop's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="c850c-106">然後，若要向下流覽命名空間，您的應用程式可以遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="c850c-106">Then, to navigate downward through the namespace, your application can follow these steps:</span></span>

1.  <span data-ttu-id="c850c-107">列舉資料夾的內容。</span><span class="sxs-lookup"><span data-stu-id="c850c-107">Enumerate the folder's contents.</span></span>
2.  <span data-ttu-id="c850c-108">判斷哪些物件是子資料夾，然後選取其中一個。</span><span class="sxs-lookup"><span data-stu-id="c850c-108">Determine which objects are subfolders, and select one.</span></span>
3.  <span data-ttu-id="c850c-109">系結至子資料夾，以取出其 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。</span><span class="sxs-lookup"><span data-stu-id="c850c-109">Bind to the subfolder to retrieve its [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span>

<span data-ttu-id="c850c-110">視需要重複執行這些步驟以達到目標。</span><span class="sxs-lookup"><span data-stu-id="c850c-110">Repeat these steps as often as necessary to reach the target.</span></span>

## <a name="a-simple-example-of-namespace-navigation"></a><span data-ttu-id="c850c-111">命名空間導覽的簡單範例</span><span class="sxs-lookup"><span data-stu-id="c850c-111">A Simple Example of Namespace Navigation</span></span>

<span data-ttu-id="c850c-112">下列範例程式碼是一個簡單的主控台應用程式，說明上述各節所討論的一些程式。</span><span class="sxs-lookup"><span data-stu-id="c850c-112">The following piece of sample code is a simple console application that illustrates a number of the procedures discussed in the preceding sections.</span></span> <span data-ttu-id="c850c-113">為了清楚起見，已省略錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="c850c-113">Error checking has been omitted for clarity.</span></span> <span data-ttu-id="c850c-114">此應用程式會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="c850c-114">The application performs the following tasks:</span></span>

1.  <span data-ttu-id="c850c-115">[使用 IShellFolder 介面](folder-info.md))  (抓取 Program Files 資料夾的 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)介面。</span><span class="sxs-lookup"><span data-stu-id="c850c-115">Retrieves the Program Files folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface ([Using the IShellFolder Interface](folder-info.md)).</span></span>
2.  <span data-ttu-id="c850c-116">列舉資料夾的內容， ([列舉資料夾](folder-info.md)) 的內容。</span><span class="sxs-lookup"><span data-stu-id="c850c-116">Enumerates the contents of the folder ([Enumerating the Contents of a Folder](folder-info.md)).</span></span>
3.  <span data-ttu-id="c850c-117">決定所有顯示名稱，並將它們列印 ([判斷) 顯示名稱和其他屬性](folder-info.md) 。</span><span class="sxs-lookup"><span data-stu-id="c850c-117">Determines all the display names and prints them ([Determining Display Names and Other Properties](folder-info.md)).</span></span>
4.  <span data-ttu-id="c850c-118">尋找子資料夾 ([取得子資料夾 IShellFolder 介面的指標](folder-info.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c850c-118">Looks for a subfolder ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
5.  <span data-ttu-id="c850c-119">系結到它所找到的第一個子資料夾， ([取得子資料夾 IShellFolder 介面的指標](folder-info.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c850c-119">Binds to the first subfolder it finds ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
6.  <span data-ttu-id="c850c-120">在子資料夾中列印物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c850c-120">Prints the display names of the objects in the subfolder.</span></span>


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



 

 
