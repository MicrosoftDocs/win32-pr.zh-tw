---
title: 回應檔
description: 除了在命令列上放置所有選項以外，MIDL 編譯器還接受包含參數和引數的回應檔。
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL 編譯器 MIDL，回應檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9b4d079e92dff3c25f8a38c6c73073a548ea91
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387068"
---
# <a name="response-files"></a><span data-ttu-id="a2943-104">回應檔</span><span class="sxs-lookup"><span data-stu-id="a2943-104">Response Files</span></span>

<span data-ttu-id="a2943-105">除了在命令列上放置所有選項以外，MIDL 編譯器還接受包含參數和引數的回應檔。</span><span class="sxs-lookup"><span data-stu-id="a2943-105">As an alternative to placing all the options on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="a2943-106">回應檔是一個文字檔，其中包含一個或多個 MIDL 編譯器命令列選項。</span><span class="sxs-lookup"><span data-stu-id="a2943-106">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="a2943-107">與命令列不同的是，回應檔允許多行的選項和檔案名。</span><span class="sxs-lookup"><span data-stu-id="a2943-107">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="a2943-108">這可能會因為您的組建環境有所限制，或為了方便您建立您的組建流程。</span><span class="sxs-lookup"><span data-stu-id="a2943-108">This may be useful due to limitations of your build environment or as a convenience for your build process.</span></span> <span data-ttu-id="a2943-109">您可以指定 MIDL 回應檔，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a2943-109">You can specify a MIDL response file as:</span></span>

<span data-ttu-id="a2943-110">**midl** **\@ 檔案名**</span><span class="sxs-lookup"><span data-stu-id="a2943-110">**midl** **\@filename**</span></span>

<dl> <dt>

<span data-ttu-id="a2943-111"><span id="filename"></span><span id="FILENAME"></span>*檔案名*</span><span class="sxs-lookup"><span data-stu-id="a2943-111"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="a2943-112">指定回應檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2943-112">Specifies the name of the response file.</span></span> <span data-ttu-id="a2943-113">回應檔名稱必須緊接在 @ 字元之後，@ 字元和回應檔名稱之間不能有空白字元。</span><span class="sxs-lookup"><span data-stu-id="a2943-113">The response file name must immediately follow the @ character with no white space between the @ character and the response file name.</span></span>

</dd> </dl>

<span data-ttu-id="a2943-114">回應檔中的選項會被解釋為在 MIDL 命令列中出現的位置。</span><span class="sxs-lookup"><span data-stu-id="a2943-114">Options in a response file are interpreted as if they were present at that place in the MIDL command line.</span></span> <span data-ttu-id="a2943-115">回應檔中的每個引數都必須在同一行的開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="a2943-115">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="a2943-116">您無法使用 () 的反斜線字元 \\ 來串連行。</span><span class="sxs-lookup"><span data-stu-id="a2943-116">You cannot use the backslash character (\\) to concatenate lines.</span></span>

<span data-ttu-id="a2943-117">MIDL 支援包含一或多個回應檔的命令列引數，並與其他命令列參數結合：</span><span class="sxs-lookup"><span data-stu-id="a2943-117">MIDL supports command-line arguments that include one or more response files, combined with other command-line switches:</span></span>

<span data-ttu-id="a2943-118">**midl-Oicf @midl1.rsp -envwin32 @midl2.rsp itf .idl**</span><span class="sxs-lookup"><span data-stu-id="a2943-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span></span>

<span data-ttu-id="a2943-119">MIDL 編譯器不支援嵌套回應檔。</span><span class="sxs-lookup"><span data-stu-id="a2943-119">The MIDL compiler does not support nested response files.</span></span>

 

 




