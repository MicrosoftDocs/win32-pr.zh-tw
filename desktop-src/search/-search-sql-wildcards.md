---
description: CONTAINS 述詞支援使用星號 (\*) 作為萬用字元，以代表單字和片語。 您只能在單字或片語的結尾加上星號。 星號是否存在會啟用前置比對模式。
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: 在 CONTAINS 述詞中使用萬用字元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013e49f97cf23c7a00aca7bb287edd19951520f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112409"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a><span data-ttu-id="efc00-105">在 CONTAINS 述詞中使用萬用字元</span><span class="sxs-lookup"><span data-stu-id="efc00-105">Using Wildcard Characters in the CONTAINS Predicate</span></span>

<span data-ttu-id="efc00-106">CONTAINS 述詞支援使用星號 (\*) 作為萬用字元，以代表單字和片語。</span><span class="sxs-lookup"><span data-stu-id="efc00-106">The CONTAINS predicate supports the use of the asterisk (\*) as a wildcard character to represent words and phrases.</span></span> <span data-ttu-id="efc00-107">您只能在單字或片語的結尾加上星號。</span><span class="sxs-lookup"><span data-stu-id="efc00-107">You can add the asterisk only at the end of the word or phrase.</span></span> <span data-ttu-id="efc00-108">星號是否存在會啟用前置比對模式。</span><span class="sxs-lookup"><span data-stu-id="efc00-108">The presence of the asterisk enables the prefix-matching mode.</span></span> <span data-ttu-id="efc00-109">在此模式中，如果資料行包含指定的搜尋字，後面接著零或多個其他字元，則會傳回相符專案。</span><span class="sxs-lookup"><span data-stu-id="efc00-109">In this mode, matches are returned if the column contains the specified search word followed by zero or more other characters.</span></span> <span data-ttu-id="efc00-110">如果提供了片語，則如果資料行包含所有指定的單字，且該單字後面有零或多個其他字元，則會偵測到相符專案。</span><span class="sxs-lookup"><span data-stu-id="efc00-110">If a phrase is provided, matches are detected if the column contains all the specified words with zero or more other characters following the final word.</span></span>

## <a name="examples"></a><span data-ttu-id="efc00-111">範例</span><span class="sxs-lookup"><span data-stu-id="efc00-111">Examples</span></span>

<span data-ttu-id="efc00-112">第一個範例會比對檔案名欄中具有任何單字（開頭為 "serv"）的檔。</span><span class="sxs-lookup"><span data-stu-id="efc00-112">The first example matches documents that have any word in the FileName column beginning with "serv".</span></span> <span data-ttu-id="efc00-113">符合字組範例包括 "server"、"servers" 和 "service"。</span><span class="sxs-lookup"><span data-stu-id="efc00-113">Example matching words include "server", "servers", and "service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



<span data-ttu-id="efc00-114">第二個範例會比對檔中 FileName 資料行中的任何片語（開頭為 "comp"），並在下一個單字開頭為 "serv"。</span><span class="sxs-lookup"><span data-stu-id="efc00-114">The second example matches documents with any phrase in the FileName column that begins with "comp" and in which the next word begins with "serv".</span></span> <span data-ttu-id="efc00-115">符合字組範例包括「複合伺服器」、「複合伺服器」和「複合服務」。</span><span class="sxs-lookup"><span data-stu-id="efc00-115">Example matching words include "comp server", "comp servers", and "comp service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



<span data-ttu-id="efc00-116">星號只適用于前置詞比對，而且只能放在單字或片語的結尾。它不適用於尾碼比對。</span><span class="sxs-lookup"><span data-stu-id="efc00-116">The asterisk works only for prefix-matching and can be placed only at the end of the word or phrase; it does not work for suffix-matching.</span></span> <span data-ttu-id="efc00-117">下列語法無效，而且不符合檔案名資料行中任何單字結尾為 "服務" 的檔。</span><span class="sxs-lookup"><span data-stu-id="efc00-117">The following syntax is not valid and does not match documents with any word in the FileName column ending with "serve".</span></span>


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a><span data-ttu-id="efc00-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="efc00-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="efc00-119">**參考**</span><span class="sxs-lookup"><span data-stu-id="efc00-119">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="efc00-120">FREETEXT 述詞</span><span class="sxs-lookup"><span data-stu-id="efc00-120">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="efc00-121">WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="efc00-121">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



