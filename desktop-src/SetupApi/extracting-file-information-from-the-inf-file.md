---
description: 開啟 INF 檔案之後，您可以從該檔案收集資訊以建立使用者介面，或指示安裝程式。 安裝函式提供數個層級的功能，可從 INF 檔案收集資訊。
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: 從 INF 檔案解壓縮檔案資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848231"
---
# <a name="extracting-file-information-from-the-inf-file"></a><span data-ttu-id="d9f20-104">從 INF 檔案解壓縮檔案資訊</span><span class="sxs-lookup"><span data-stu-id="d9f20-104">Extracting File Information from the INF file</span></span>

<span data-ttu-id="d9f20-105">開啟 INF 檔案之後，您可以從該檔案收集資訊以建立使用者介面，或指示安裝程式。</span><span class="sxs-lookup"><span data-stu-id="d9f20-105">After the INF file is opened, you can gather information from it to build the user interface, or to direct the installation process.</span></span> <span data-ttu-id="d9f20-106">安裝函式提供數個層級的功能，可從 INF 檔案收集資訊。</span><span class="sxs-lookup"><span data-stu-id="d9f20-106">The setup functions provide several levels of functionality for gathering information from an INF file.</span></span>



| <span data-ttu-id="d9f20-107">若要收集資訊 .。。</span><span class="sxs-lookup"><span data-stu-id="d9f20-107">To gather information…</span></span>                | <span data-ttu-id="d9f20-108">使用這些函數 .。。</span><span class="sxs-lookup"><span data-stu-id="d9f20-108">Use these functions…</span></span>                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="d9f20-109">關於 INF 檔案</span><span class="sxs-lookup"><span data-stu-id="d9f20-109">About the INF file</span></span>                    | [<span data-ttu-id="d9f20-110">**SetupGetInfInformation**</span><span class="sxs-lookup"><span data-stu-id="d9f20-110">**SetupGetInfInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [<span data-ttu-id="d9f20-111">**SetupQueryInfFileInformation**</span><span class="sxs-lookup"><span data-stu-id="d9f20-111">**SetupQueryInfFileInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | <span data-ttu-id="d9f20-112">[**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)。</span><span class="sxs-lookup"><span data-stu-id="d9f20-112">[**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span></span> |
| <span data-ttu-id="d9f20-113">關於來源和目標檔案</span><span class="sxs-lookup"><span data-stu-id="d9f20-113">About source and target files</span></span>         | [<span data-ttu-id="d9f20-114">**SetupGetSourceFileLocation**</span><span class="sxs-lookup"><span data-stu-id="d9f20-114">**SetupGetSourceFileLocation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [<span data-ttu-id="d9f20-115">**SetupGetSourceFileSize**</span><span class="sxs-lookup"><span data-stu-id="d9f20-115">**SetupGetSourceFileSize**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [<span data-ttu-id="d9f20-116">**SetupGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="d9f20-116">**SetupGetTargetPath**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [<span data-ttu-id="d9f20-117">**SetupGetSourceInfo**</span><span class="sxs-lookup"><span data-stu-id="d9f20-117">**SetupGetSourceInfo**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| <span data-ttu-id="d9f20-118">從 INF 檔案中的一行</span><span class="sxs-lookup"><span data-stu-id="d9f20-118">From a line of an INF file</span></span>            | [<span data-ttu-id="d9f20-119">**SetupGetLineText**</span><span class="sxs-lookup"><span data-stu-id="d9f20-119">**SetupGetLineText**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [<span data-ttu-id="d9f20-120">**SetupFindNextLine**</span><span class="sxs-lookup"><span data-stu-id="d9f20-120">**SetupFindNextLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [<span data-ttu-id="d9f20-121">**SetupFindNextMatchLine**</span><span class="sxs-lookup"><span data-stu-id="d9f20-121">**SetupFindNextMatchLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [<span data-ttu-id="d9f20-122">**SetupGetLineByIndex**</span><span class="sxs-lookup"><span data-stu-id="d9f20-122">**SetupGetLineByIndex**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [<span data-ttu-id="d9f20-123">**SetupFindFirstLine**</span><span class="sxs-lookup"><span data-stu-id="d9f20-123">**SetupFindFirstLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| <span data-ttu-id="d9f20-124">從 INF 檔案中的列欄位</span><span class="sxs-lookup"><span data-stu-id="d9f20-124">From a field of a line in an INF file</span></span> | [<span data-ttu-id="d9f20-125">**SetupGetStringField**</span><span class="sxs-lookup"><span data-stu-id="d9f20-125">**SetupGetStringField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [<span data-ttu-id="d9f20-126">**SetupGetIntField**</span><span class="sxs-lookup"><span data-stu-id="d9f20-126">**SetupGetIntField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [<span data-ttu-id="d9f20-127">**SetupGetBinaryField**</span><span class="sxs-lookup"><span data-stu-id="d9f20-127">**SetupGetBinaryField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [<span data-ttu-id="d9f20-128">**SetupGetMultiSzField**</span><span class="sxs-lookup"><span data-stu-id="d9f20-128">**SetupGetMultiSzField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

<span data-ttu-id="d9f20-129">下列範例會使用 [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) 函式，從 INF 檔案取出來源媒體的人們可讀取描述。</span><span class="sxs-lookup"><span data-stu-id="d9f20-129">The following example uses the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function to retrieve the human-readable description of a source media from an INF file.</span></span>


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



<span data-ttu-id="d9f20-130">在此範例中，MyInf 是開啟的 INF 檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d9f20-130">In the example, MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="d9f20-131">SourceId 是特定來源媒體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9f20-131">SourceId is the identifier for a specific source media.</span></span> <span data-ttu-id="d9f20-132">值 SRCINFO \_ 描述指定 [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) 函式應該取出來源媒體描述。</span><span class="sxs-lookup"><span data-stu-id="d9f20-132">The value SRCINFO\_DESCRIPTION specifies that the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function should retrieve the source media description.</span></span> <span data-ttu-id="d9f20-133">緩衝區指向將接收描述的字串，MaxBufSize 表示配置給緩衝區的資源，而 BufSize 指出儲存緩衝區所需的資源。</span><span class="sxs-lookup"><span data-stu-id="d9f20-133">Buffer points to a string that will receive the description, MaxBufSize indicates the resources allocated to the buffer, and BufSize indicates the resources necessary to store the buffer.</span></span>

<span data-ttu-id="d9f20-134">如果 BufSize 大於 MaxBufSize，則函式會傳回 **FALSE**，而後續對 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 的呼叫將會傳回錯誤 \_ 的 \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d9f20-134">If BufSize is greater than MaxBufSize, the function will return **FALSE**, and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return ERROR\_INSUFFICIENT\_BUFFER.</span></span>

 

 
