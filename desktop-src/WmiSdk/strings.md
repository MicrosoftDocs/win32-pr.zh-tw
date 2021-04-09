---
title: MOF 字串
description: 字串是包含字元字串的資料類型，通常是人們可讀取的文字。
ms.assetid: 08a07184-6d23-4988-a3de-e5bfc3e177f8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1427accbdb3a4dae0240563656785968d4bd075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848629"
---
# <a name="mof-strings"></a><span data-ttu-id="5c032-103">MOF 字串</span><span class="sxs-lookup"><span data-stu-id="5c032-103">MOF strings</span></span>

<span data-ttu-id="5c032-104">字串是包含字元字串的資料類型，通常是人們可讀取的文字。</span><span class="sxs-lookup"><span data-stu-id="5c032-104">A string is a data type that contains a string of characters usually intended as human-readable text.</span></span> <span data-ttu-id="5c032-105">MOF 描述兩種類型的字串，用來保存單一或多個字元。</span><span class="sxs-lookup"><span data-stu-id="5c032-105">MOF describes two types of strings, which use to hold single or multiple characters.</span></span> <span data-ttu-id="5c032-106">MOF 也有一系列的規則，描述如何在字串中使用引號。</span><span class="sxs-lookup"><span data-stu-id="5c032-106">MOF also has a series of rules describing the use of quotes within a string.</span></span>

<span data-ttu-id="5c032-107">下表列出 MOF 的字串資料類型。</span><span class="sxs-lookup"><span data-stu-id="5c032-107">The following table lists the string data types for MOF.</span></span>



| <span data-ttu-id="5c032-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="5c032-108">Data type</span></span>  | <span data-ttu-id="5c032-109">Automation 類型</span><span class="sxs-lookup"><span data-stu-id="5c032-109">Automation type</span></span> | <span data-ttu-id="5c032-110">Description</span><span class="sxs-lookup"><span data-stu-id="5c032-110">Description</span></span>                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c032-111">**char16**</span><span class="sxs-lookup"><span data-stu-id="5c032-111">**char16**</span></span> | <span data-ttu-id="5c032-112">**VT \_ I2**</span><span class="sxs-lookup"><span data-stu-id="5c032-112">**VT\_I2**</span></span>      | <span data-ttu-id="5c032-113">通用字元集2中的單一16位 Unicode 字元 (UCS-2) 格式</span><span class="sxs-lookup"><span data-stu-id="5c032-113">Single 16-bit Unicode character in Universal Character Set 2 (UCS-2) format</span></span><br/> |
| <span data-ttu-id="5c032-114">**string**</span><span class="sxs-lookup"><span data-stu-id="5c032-114">**string**</span></span> | <span data-ttu-id="5c032-115">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="5c032-115">**VT\_BSTR**</span></span>    | <span data-ttu-id="5c032-116">Unicode 字元字串</span><span class="sxs-lookup"><span data-stu-id="5c032-116">Unicode character string</span></span><br/>                                                    |



 

<span data-ttu-id="5c032-117">撰寫 MOF 的字串時，請使用下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="5c032-117">Use the following guidelines when writing strings for MOF:</span></span>

-   <span data-ttu-id="5c032-118">使用單引號來括住單一字元常數。</span><span class="sxs-lookup"><span data-stu-id="5c032-118">Surround single-character constants with single quotes.</span></span>

    <span data-ttu-id="5c032-119">如果您未搭配單一字元常數使用單引號，則必須使用 Unicode 字元值的整數表示。</span><span class="sxs-lookup"><span data-stu-id="5c032-119">If you do not use single quotes with single character constants, you must use the integer representation of the Unicode character value.</span></span> <span data-ttu-id="5c032-120">您可以選擇性地使用 \\ 美國國家標準局 (ANSI) C 標準的 x escape 序列來指定字元，如下所示：</span><span class="sxs-lookup"><span data-stu-id="5c032-120">Optionally, you could specify the character literally with the \\x escape sequence from the American National Standards Institute (ANSI) C standard, as shown:</span></span>

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    <span data-ttu-id="5c032-121">因為 MOF 是以 Unicode 為基礎，所以您也可以指定16位值。</span><span class="sxs-lookup"><span data-stu-id="5c032-121">Because MOF is based on Unicode, you can also specify 16-bit values.</span></span>

    <span data-ttu-id="5c032-122">請注意，ANSI C 格式的單一字元常數會以雙引號括住。</span><span class="sxs-lookup"><span data-stu-id="5c032-122">Be aware that single-character constants in ANSI C format are surrounded by double quotes.</span></span>

-   <span data-ttu-id="5c032-123">將字元字串括在雙引號中。</span><span class="sxs-lookup"><span data-stu-id="5c032-123">Surround character strings with double quotes.</span></span>

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   <span data-ttu-id="5c032-124">使用一或多個空白字元串連連續的引號字串。</span><span class="sxs-lookup"><span data-stu-id="5c032-124">Concatenate successive quote strings with one or more white spaces.</span></span>

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   <span data-ttu-id="5c032-125">使用以反斜線開頭的 escape 序列，將引號內嵌至字串中。</span><span class="sxs-lookup"><span data-stu-id="5c032-125">Use an escape sequence beginning with a backslash to embed quotes into a string.</span></span>

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

<span data-ttu-id="5c032-126">下列範例說明如何初始化字串屬性和字串參數：</span><span class="sxs-lookup"><span data-stu-id="5c032-126">The following example describes how to initialize string properties and a string parameter:</span></span>

``` syntax
class  StringDataClass
{
    [key]  String    Dstring;
    DateTime         DTime;
    char16           CharVal1;
    char16           CharVal2;
    sint32 DiskMethod ([in, Id(0)] string Description = "Disk 1");
};

instance of StringDataClass
{
    Dstring = "this can go on for " " some time"
       " before it is complete";
    DTime    = "19940107140332.000000-300";
    CharVal1 = '\x16';
    CharVal2 = '\x32';
};
```

 

 




