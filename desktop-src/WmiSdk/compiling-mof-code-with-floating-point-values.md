---
description: MOF 編譯器接受針對 nonfloating 點屬性指定的浮點值。 此值會向上或向下舍入，並儲存為 nonfloating 點數位。 這種情況可能會導致某些非預期的結果。
ms.assetid: 5cf7d8e1-c29d-4b9f-8557-e656c5e83370
ms.tgt_platform: multiple
title: 使用 Floating-Point 值編譯 MOF 程式碼
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734639e1038b8e9739fead694740dbf5ab5f9cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193873"
---
# <a name="compiling-mof-code-with-floating-point-values"></a><span data-ttu-id="5781c-105">使用 Floating-Point 值編譯 MOF 程式碼</span><span class="sxs-lookup"><span data-stu-id="5781c-105">Compiling MOF Code with Floating-Point Values</span></span>

<span data-ttu-id="5781c-106">MOF 編譯器接受針對 nonfloating 點屬性指定的浮點值。</span><span class="sxs-lookup"><span data-stu-id="5781c-106">The MOF compiler accepts a floating-point value specified for a nonfloating-point property.</span></span> <span data-ttu-id="5781c-107">此值會向上或向下舍入，並儲存為 nonfloating 點數位。</span><span class="sxs-lookup"><span data-stu-id="5781c-107">The value is rounded up or down and stored as a nonfloating-point number.</span></span> <span data-ttu-id="5781c-108">這種情況可能會導致某些非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="5781c-108">This situation can cause some unexpected results.</span></span>

<span data-ttu-id="5781c-109">下列 MOF 程式碼範例會在名為 "Test" 的命名空間中，定義名為 **abc** 的類別。</span><span class="sxs-lookup"><span data-stu-id="5781c-109">The following MOF code example defines a class called **abc** in a namespace called "Test".</span></span> <span data-ttu-id="5781c-110">這個 MOF 程式碼會進行編譯而不會發生錯誤，但是您無法在此程式碼所建立的實例中，查詢針對屬性 **exampleUint16** 所定義的浮點值。</span><span class="sxs-lookup"><span data-stu-id="5781c-110">This MOF code compiles without errors, but you cannot query for the floating-point value defined for the property **exampleUint16** in the instance this code creates.</span></span>

``` syntax
#pragma namespace ("\\\\.\\Root")

instance of __Namespace
{
    Name = "Test";
};

#pragma namespace ("\\\\.\\Root\\test")

Class abc
{
        [KEY] String testID ;
        Uint16 exampleUint16;
        Real64 exampleReal64;
};

Instance of abc
{ 
        TestID ="exampleID";
        exampleUint16 = 1000.4;
};
```

<span data-ttu-id="5781c-111">如果您發出下列查詢，則會收到指出無效查詢的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5781c-111">If you issue the following query, you get an error code that indicates an invalid query.</span></span>


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



<span data-ttu-id="5781c-112">但是，下列查詢會尋找指定的實例。</span><span class="sxs-lookup"><span data-stu-id="5781c-112">However, the following query finds the indicated instance.</span></span>


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a><span data-ttu-id="5781c-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="5781c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5781c-114">編譯 MOF 檔案</span><span class="sxs-lookup"><span data-stu-id="5781c-114">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="5781c-115">**mofcomp.exe**</span><span class="sxs-lookup"><span data-stu-id="5781c-115">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="5781c-116">預處理器命令</span><span class="sxs-lookup"><span data-stu-id="5781c-116">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



