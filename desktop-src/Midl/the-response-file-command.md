---
title: 回應檔命令
description: 回應檔是一個文字檔，其中包含一個或多個 MIDL 編譯器命令列選項。
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- 命令列參考 MIDL，回應檔案命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f624f8bb4fd50fa77df604e5d56f48c9e55c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932462"
---
# <a name="the-response-file-command"></a><span data-ttu-id="911b0-104">回應檔命令</span><span class="sxs-lookup"><span data-stu-id="911b0-104">The Response File Command</span></span>

<span data-ttu-id="911b0-105">回應檔是一個文字檔，其中包含一個或多個 MIDL 編譯器命令列選項。</span><span class="sxs-lookup"><span data-stu-id="911b0-105">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="911b0-106">與命令列不同的是，回應檔允許多行的選項和檔案名。</span><span class="sxs-lookup"><span data-stu-id="911b0-106">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="911b0-107">這可能會因為您的組建環境有所限制，或為了方便您建立您的組建流程。</span><span class="sxs-lookup"><span data-stu-id="911b0-107">This may be useful due to limitations of your build environment, or as a convenience for your build process.</span></span>

## <a name="switch-options"></a><span data-ttu-id="911b0-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="911b0-108">Switch Options</span></span>

``` syntax
midl @response_file
```

<dl> <dt>

<span data-ttu-id="911b0-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*回應 \_ 檔*</span><span class="sxs-lookup"><span data-stu-id="911b0-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*response\_file*</span></span>
</dt> <dd>

<span data-ttu-id="911b0-110">指定回應檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="911b0-110">Specifies the name of a response file.</span></span> <span data-ttu-id="911b0-111">回應檔名稱必須緊接在 @ 字元後面。</span><span class="sxs-lookup"><span data-stu-id="911b0-111">The response file name must immediately follow the @ character.</span></span> <span data-ttu-id="911b0-112">@ 字元和回應檔名稱之間不允許有空格。</span><span class="sxs-lookup"><span data-stu-id="911b0-112">No white space is allowed between the @ character and the response file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="911b0-113">備註</span><span class="sxs-lookup"><span data-stu-id="911b0-113">Remarks</span></span>

<span data-ttu-id="911b0-114">除了在命令列上放置與參數相關聯的所有選項以外，MIDL 編譯器還接受包含參數和引數的回應檔。</span><span class="sxs-lookup"><span data-stu-id="911b0-114">As an alternative to placing all options associated with a switch on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="911b0-115">回應檔中的選項會被解讀為 MIDL 命令列中的該位置。</span><span class="sxs-lookup"><span data-stu-id="911b0-115">Options in a response file are interpreted as if they are present in that location in the MIDL command line.</span></span>

<span data-ttu-id="911b0-116">回應檔中的每個引數都必須在同一行的開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="911b0-116">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="911b0-117">反斜線字元 (\) 不能用來串連行。</span><span class="sxs-lookup"><span data-stu-id="911b0-117">The backslash character (\) cannot be used to concatenate lines.</span></span> <span data-ttu-id="911b0-118">當它是回應檔中引號字串的一部分時，反斜線字元只能用在另一個反斜線之前或雙引號字元 ( ") 之前。</span><span class="sxs-lookup"><span data-stu-id="911b0-118">When it is part of a quoted string in the response file, the backslash character can only be used before another backslash or before a double quotation mark character (").</span></span> <span data-ttu-id="911b0-119">當它不是引號字串的一部分時，反斜線字元只能用在雙引號字元之前。</span><span class="sxs-lookup"><span data-stu-id="911b0-119">When it is not part of a quoted string, the backslash character can only be used before a double quotation mark character.</span></span>

<span data-ttu-id="911b0-120">MIDL 支援命令列引數，其中包含一或多個與其他命令列參數結合的回應檔。</span><span class="sxs-lookup"><span data-stu-id="911b0-120">MIDL supports command-line arguments that include one or more response files combined with other command-line switches.</span></span>

<span data-ttu-id="911b0-121">MIDL 編譯器不支援嵌套回應檔。</span><span class="sxs-lookup"><span data-stu-id="911b0-121">The MIDL compiler does not support nested response files.</span></span>

## <a name="examples"></a><span data-ttu-id="911b0-122">範例</span><span class="sxs-lookup"><span data-stu-id="911b0-122">Examples</span></span>

<span data-ttu-id="911b0-123">**midl @midl.rsp**</span><span class="sxs-lookup"><span data-stu-id="911b0-123">**midl @midl.rsp**</span></span>

<span data-ttu-id="911b0-124">**midl-Oicf @midl1.rsp -env win32 @midl2.rsp itf .idl**</span><span class="sxs-lookup"><span data-stu-id="911b0-124">**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**</span></span>

## <a name="related-topics"></a><span data-ttu-id="911b0-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="911b0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="911b0-126">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="911b0-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




