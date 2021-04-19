---
description: 將一個 MOF 檔案的內容包含在另一個 MOF 檔案中。
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5eb3d203cff5bca7e5096082cca7ba531580ae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983869"
---
# <a name="include"></a><span data-ttu-id="e52d8-103">' #include '</span><span class="sxs-lookup"><span data-stu-id="e52d8-103">'#include'</span></span>
<span data-ttu-id="e52d8-104">/\* 標題： MyMof。 Mof                           *//*   標題： MyMof2</span><span class="sxs-lookup"><span data-stu-id="e52d8-104">/\*   Title: MyMof.Mof                           */ /*   Title: MyMof2.Mof                               \*/</span></span>

<span data-ttu-id="e52d8-105">\#包含預處理器命令會將一個 mof 檔案的內容包含在另一個 mof 檔案中。</span><span class="sxs-lookup"><span data-stu-id="e52d8-105">The \#include preprocessor command includes the contents of one MOF file into another MOF file.</span></span> <span data-ttu-id="e52d8-106">下列程式碼範例描述 include 命令的語法 \# 。</span><span class="sxs-lookup"><span data-stu-id="e52d8-106">The following code example describes the syntax for the \#include command.</span></span>

``` syntax
#include ("Moffile.mof")
```

<span data-ttu-id="e52d8-107">在上述範例中，Moffile 是要包含的 MOF 檔案名。</span><span class="sxs-lookup"><span data-stu-id="e52d8-107">In the previous example, Moffile.mof is the name of the MOF file to include.</span></span>

<span data-ttu-id="e52d8-108">下列範例顯示兩個 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="e52d8-108">The following example shows two MOF files.</span></span> <span data-ttu-id="e52d8-109">當您編譯第一個 MOF 檔案時，編譯器會在您放置 include 語句的位置中，自動編譯第二個 MOF 檔案 (Mymof2) 。 \#</span><span class="sxs-lookup"><span data-stu-id="e52d8-109">When you compile the first MOF file, the compiler automatically compiles the second MOF file (Mymof2.mof) in the location you place the \#include statement.</span></span>

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

<span data-ttu-id="e52d8-110">上述範例包含下列 MOF 檔案：</span><span class="sxs-lookup"><span data-stu-id="e52d8-110">The following MOF file is included in the previous example:</span></span>

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a><span data-ttu-id="e52d8-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="e52d8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e52d8-112">預處理器命令</span><span class="sxs-lookup"><span data-stu-id="e52d8-112">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



