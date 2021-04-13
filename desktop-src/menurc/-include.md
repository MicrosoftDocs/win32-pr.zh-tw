---
title: " include"
description: '\ Include 指示詞會導致資源編譯器處理 filename 參數中所指定的檔案。'
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383766"
---
# <a name="-include"></a><span data-ttu-id="a9ffc-103">包含</span><span class="sxs-lookup"><span data-stu-id="a9ffc-103">' include'</span></span>

<span data-ttu-id="a9ffc-104">**\# Include** 指示詞會導致資源編譯器處理 *filename* 參數中所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="a9ffc-104">The **\#include** directive causes the resource compiler to process the file specified in the *filename* parameter.</span></span> <span data-ttu-id="a9ffc-105">這個檔案應該是定義資源定義檔中所使用之常數的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="a9ffc-105">This file should be a header file that defines the constants used in the resource-definition file.</span></span> <span data-ttu-id="a9ffc-106">檔案可以使用單一位元組、雙位元組或 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="a9ffc-106">The file can use single-byte, double-byte, or Unicode characters.</span></span>

``` syntax
#include filename
```

<dl> <dt>

<span data-ttu-id="a9ffc-107"><span id="filename"></span><span id="FILENAME"></span>*檔案名*</span><span class="sxs-lookup"><span data-stu-id="a9ffc-107"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="a9ffc-108">要包含的檔案名。</span><span class="sxs-lookup"><span data-stu-id="a9ffc-108">Name of the file to be included.</span></span> <span data-ttu-id="a9ffc-109">如果檔案在目前的目錄中，則字串必須用雙引號括住;如果檔案位於 INCLUDE 環境變數所指定的目錄中，則字串必須包含在 (<>) 的小於字元和大於字元。</span><span class="sxs-lookup"><span data-stu-id="a9ffc-109">If the file is in the current directory, the string must be enclosed in double quotation marks; if the file is in the directory specified by the INCLUDE environment variable, the string must be enclosed in less-than and greater-than characters (<>).</span></span> <span data-ttu-id="a9ffc-110">如果檔案不在目前的目錄或 INCLUDE 環境變數所指定的目錄中，您必須提供以雙引號括住的完整路徑 ( ") 。</span><span class="sxs-lookup"><span data-stu-id="a9ffc-110">You must give a full path enclosed in double quotation marks (") if the file is not in the current directory or in the directory specified by the INCLUDE environment variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9ffc-111">備註</span><span class="sxs-lookup"><span data-stu-id="a9ffc-111">Remarks</span></span>

<span data-ttu-id="a9ffc-112">在標頭檔中使用下列語句，以圍住可由 C 編譯器編譯但不能由 RC 編譯的語句：</span><span class="sxs-lookup"><span data-stu-id="a9ffc-112">Use the following statement in your header file to surround statements that can be compiled by a C compiler but not RC:</span></span>

``` syntax
#ifndef RC_INVOKED
```

<span data-ttu-id="a9ffc-113">如此一來，您就可以在 .c 和 .rc 檔案中使用相同的 include 檔。</span><span class="sxs-lookup"><span data-stu-id="a9ffc-113">This way, you can use the same include files in your .c and .rc files.</span></span>

## <a name="example"></a><span data-ttu-id="a9ffc-114">範例</span><span class="sxs-lookup"><span data-stu-id="a9ffc-114">Example</span></span>

<span data-ttu-id="a9ffc-115">此範例會在編譯資源定義檔時，處理標頭檔的 Windows .h 和 MyDefs：</span><span class="sxs-lookup"><span data-stu-id="a9ffc-115">This example processes the header files Windows.h and MyDefs.h while compiling the resource-definition file:</span></span>

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a><span data-ttu-id="a9ffc-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9ffc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9ffc-117">預處理器指示詞</span><span class="sxs-lookup"><span data-stu-id="a9ffc-117">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




