---
description: 受控物件格式 (MOF) 編譯器會使用兩種不同的批註分隔符號樣式來支援兩種形式的批註。
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: 建立批註
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d0e7cf2484fef018c62c8c47d9c55d245191681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993076"
---
# <a name="creating-a-comment"></a><span data-ttu-id="3b450-103">建立批註</span><span class="sxs-lookup"><span data-stu-id="3b450-103">Creating a Comment</span></span>

<span data-ttu-id="3b450-104">受控物件格式 (MOF) 編譯器會使用兩種不同的批註分隔符號樣式來支援兩種形式的批註。</span><span class="sxs-lookup"><span data-stu-id="3b450-104">The Managed Object Format (MOF) compiler supports two styles of comment using two different styles of comment delimiters.</span></span>

<span data-ttu-id="3b450-105">下表列出用於批註的分隔符號，以及分隔符號在程式碼中的效果。</span><span class="sxs-lookup"><span data-stu-id="3b450-105">The following table lists the delimiters that are used for comments and the effect that the delimiters have in the code.</span></span>



| <span data-ttu-id="3b450-106">分隔符號</span><span class="sxs-lookup"><span data-stu-id="3b450-106">Delimiter</span></span>   | <span data-ttu-id="3b450-107">標記</span><span class="sxs-lookup"><span data-stu-id="3b450-107">Marks</span></span>                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | <span data-ttu-id="3b450-108">在行尾終止的批註開頭。</span><span class="sxs-lookup"><span data-stu-id="3b450-108">Start of a comment that terminates at the end of the line.</span></span>                                    |
| <span data-ttu-id="3b450-109">/\* 和 \*/</span><span class="sxs-lookup"><span data-stu-id="3b450-109">/\* and \*/</span></span> | <span data-ttu-id="3b450-110">批註的開頭和結尾可能橫跨多行，或只跨越某部分的行。</span><span class="sxs-lookup"><span data-stu-id="3b450-110">Beginning and end of a comment that may span multiple lines or only span a portion of a line.</span></span> |



 

<span data-ttu-id="3b450-111">如同 C 和 c + + 程式設計語言，您必須只使用單一行批註的//分隔符號，但使用/ \* 和 \* /分隔符號搭配單行或多行批註。</span><span class="sxs-lookup"><span data-stu-id="3b450-111">As in the C and C++ programming languages, you must use the // delimiter with single-line comments only, but use the /\* and \*/ delimiters with either single-line or multiple-line comments.</span></span>

<span data-ttu-id="3b450-112">下列程式碼範例描述兩個分隔符號樣式。</span><span class="sxs-lookup"><span data-stu-id="3b450-112">The following code example describes the two delimiter styles.</span></span>

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a><span data-ttu-id="3b450-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b450-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b450-114">設計受控物件格式 (MOF) 類別</span><span class="sxs-lookup"><span data-stu-id="3b450-114">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



