---
description: 您必須使用 SetupOpenInfFile 函式來開啟 INF 檔案，才能從其中抓取資訊，或將其他 INF 檔案附加至該檔案。
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: 開啟 INF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849603"
---
# <a name="opening-the-inf-file"></a><span data-ttu-id="0e034-103">開啟 INF 檔案</span><span class="sxs-lookup"><span data-stu-id="0e034-103">Opening the INF File</span></span>

<span data-ttu-id="0e034-104">您必須使用 [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) 函式來開啟 INF 檔案，才能從其中抓取資訊，或將其他 INF 檔案附加至該檔案。</span><span class="sxs-lookup"><span data-stu-id="0e034-104">You must use the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function to open the INF file before you can retrieve information from it, or append other INF files to it.</span></span>

<span data-ttu-id="0e034-105">下列程式會使用 [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) 開啟 inf 檔案，並將控制碼 MyInf 傳回至已開啟的 INF 檔案。</span><span class="sxs-lookup"><span data-stu-id="0e034-105">The following opens an INF file using [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) and returns a handle, MyInf, to the opened INF file.</span></span> <span data-ttu-id="0e034-106">**SetupOpenInfFile** 的 *InfClass* 參數會指定為 **Null** ，表示應該忽略 INF 檔案的類別。</span><span class="sxs-lookup"><span data-stu-id="0e034-106">The *InfClass* parameter of **SetupOpenInfFile** is specified as **NULL** to indicate that the Class of the INF file should be ignored.</span></span>


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



<span data-ttu-id="0e034-107">開啟 INF 檔案之後，您可以呼叫 [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) 函式，將檔案附加至開啟的 INF 檔案。</span><span class="sxs-lookup"><span data-stu-id="0e034-107">After an INF file is opened, you can call the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function to append a file to the open INF file.</span></span> <span data-ttu-id="0e034-108">若要附加數個檔案，請重複此程式。</span><span class="sxs-lookup"><span data-stu-id="0e034-108">To append several files, repeat this process.</span></span> <span data-ttu-id="0e034-109">如果您呼叫 **SetupOpenAppendInfFile** 函式，且傳遞給它的檔案名為 **Null**，則函式會在開啟的 inf 檔案的版本區段中搜尋 (以及 LayoutFile 金鑰的任何附加 INF 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="0e034-109">If you call the **SetupOpenAppendInfFile** function and the filename passed to it is **NULL**, then the function will search the Version section of the open INF file (and any appended INF files) for a LayoutFile key.</span></span> <span data-ttu-id="0e034-110">如果函式找到索引鍵，則會附加該索引鍵所指定的檔案， (通常是版面配置。INF) 。</span><span class="sxs-lookup"><span data-stu-id="0e034-110">If the function finds a key, it will append the file specified by that key (usually LAYOUT.INF).</span></span> <span data-ttu-id="0e034-111">合併多個 INF 檔案時， **SetupOpenAppendInfFile** 會在搜尋版本區段時，從最後附加的 inf 檔案開始。</span><span class="sxs-lookup"><span data-stu-id="0e034-111">When multiple INF files have been combined, **SetupOpenAppendInfFile** starts with the last appended INF file when it searches for a Version section.</span></span>

 

 



