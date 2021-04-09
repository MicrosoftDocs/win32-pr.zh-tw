---
description: 從程式（例如自訂動作或自動化進程）呼叫下列任何資料庫函式之前，安裝程式必須先執行 CostInitialize 動作、FileCost 動作和 CostFinalize 動作。
ms.assetid: b9795825-41fa-474b-a0c5-06770aa99bc1
title: 從程式呼叫資料庫函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e2adeab5570bc6786439d5de509f03ab906a0c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848942"
---
# <a name="calling-database-functions-from-programs"></a><span data-ttu-id="4a81b-103">從程式呼叫資料庫函式</span><span class="sxs-lookup"><span data-stu-id="4a81b-103">Calling Database Functions from Programs</span></span>

<span data-ttu-id="4a81b-104">從程式（例如自訂動作或自動化進程）呼叫下列任何 [資料庫](database-functions.md) 函式之前，安裝程式必須先執行 [CostInitialize 動作](costinitialize-action.md)、 [FileCost 動作](filecost-action.md)和 [CostFinalize 動作](costfinalize-action.md)。</span><span class="sxs-lookup"><span data-stu-id="4a81b-104">Before calling any of the following [Database Functions](database-functions.md) from a program, such as a custom action or an automation process, the installer must first run the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="4a81b-105">以下是 Windows Installer 中所使用的資料庫函數清單：</span><span class="sxs-lookup"><span data-stu-id="4a81b-105">The following is a list of database functions used in Windows Installer:</span></span>

-   [<span data-ttu-id="4a81b-106">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="4a81b-106">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
-   [<span data-ttu-id="4a81b-107">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="4a81b-107">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)
-   [<span data-ttu-id="4a81b-108">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="4a81b-108">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
-   [<span data-ttu-id="4a81b-109">**MsiGetFeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="4a81b-109">**MsiGetFeatureValidStates**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)
-   [<span data-ttu-id="4a81b-110">**MsiGetSourcePath**</span><span class="sxs-lookup"><span data-stu-id="4a81b-110">**MsiGetSourcePath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)
-   [<span data-ttu-id="4a81b-111">**MsiGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="4a81b-111">**MsiGetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)
-   [<span data-ttu-id="4a81b-112">**MsiSetComponentState**</span><span class="sxs-lookup"><span data-stu-id="4a81b-112">**MsiSetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)
-   [<span data-ttu-id="4a81b-113">**MsiSetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="4a81b-113">**MsiSetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)
-   [<span data-ttu-id="4a81b-114">**MsiSetInstallLevel**</span><span class="sxs-lookup"><span data-stu-id="4a81b-114">**MsiSetInstallLevel**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)
-   [<span data-ttu-id="4a81b-115">**MsiSetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="4a81b-115">**MsiSetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)
-   [<span data-ttu-id="4a81b-116">**MsiVerifyDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="4a81b-116">**MsiVerifyDiskSpace**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)

<span data-ttu-id="4a81b-117">從程式呼叫 [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) 之前，安裝程式必須先執行 CostInitialize 動作。</span><span class="sxs-lookup"><span data-stu-id="4a81b-117">Before calling [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) from a program, the installer must first run the CostInitialize action.</span></span> <span data-ttu-id="4a81b-118">然後，安裝程式會在 **MsiSetFeatureAttributes** 之後執行 CostFinalize 動作。</span><span class="sxs-lookup"><span data-stu-id="4a81b-118">The installer then runs the CostFinalize action after **MsiSetFeatureAttributes**.</span></span>

<span data-ttu-id="4a81b-119">下列範例說明在程式中使用 [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) 時，必須呼叫函數動作的順序。</span><span class="sxs-lookup"><span data-stu-id="4a81b-119">The following example illustrates the order in which function actions must be called when using [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) in a program.</span></span>


```C++
#include <windows.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib") 

int main()  
{ 

MSIHANDLE hInstall;
TCHAR *szBuf;
DWORD cch  = 0 ;
 
if(MsiOpenPackage(_T("PathToPackage...."), &hInstall) == ERROR_SUCCESS)
{
    if(MsiDoAction(hInstall, _T("CostInitialize"))==ERROR_SUCCESS  
        && MsiDoAction(hInstall, _T("FileCost"))==ERROR_SUCCESS  
        && MsiDoAction(hInstall, _T("CostFinalize"))==ERROR_SUCCESS)   
    { 
        if(MsiGetTargetPath(hInstall, _T("FolderName"), _T(""),&cch)==ERROR_MORE_DATA)
        { 
            cch++; // add 1 to include null terminator since MsiGetTargetPath does not include it on return 
            szBuf = (TCHAR *) malloc(cch*sizeof(TCHAR));
            if(szBuf)
            {
                if(MsiGetTargetPath(hInstall, _T("FolderName"), szBuf,&cch)==ERROR_SUCCESS)
                {
                    // Add code to use szBuf here
                }
                free(szBuf);
            }
        } 
    } 
    MsiCloseHandle(hInstall);
}

return 0;  
}
```



 

 



