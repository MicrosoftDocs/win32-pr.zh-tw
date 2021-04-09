---
title: MIDL 編譯器輸出
description: 使用 IDL 和 ACF 檔案作為輸入，MIDL 編譯器最多會產生五個 C 語言的原始檔。
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb45bb369ea9d5faa695bf2658f3bafe2b3cb3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021082"
---
# <a name="midl-compiler-output"></a><span data-ttu-id="48641-103">MIDL 編譯器輸出</span><span class="sxs-lookup"><span data-stu-id="48641-103">MIDL Compiler Output</span></span>

<span data-ttu-id="48641-104">使用 IDL 和 ACF 檔案作為輸入，MIDL 編譯器最多會產生五個 C 語言的原始檔。</span><span class="sxs-lookup"><span data-stu-id="48641-104">With the IDL and ACF files as input, the MIDL compiler generates up to five C-language source files.</span></span> <span data-ttu-id="48641-105">根據預設，MIDL 編譯器會在產生的存根檔案中使用 IDL 檔案的基底檔案名。</span><span class="sxs-lookup"><span data-stu-id="48641-105">By default, the MIDL compiler uses the base file name of the IDL file as part of the generated stub files.</span></span> <span data-ttu-id="48641-106">當基底檔案名中有六個以上的字元時，某些檔案系統可能不會接受完整的存根名稱。</span><span class="sxs-lookup"><span data-stu-id="48641-106">When more than six characters are present in the base file name, some file systems may not accept the full stub name.</span></span> <span data-ttu-id="48641-107">下表顯示檔案名所使用的慣例。</span><span class="sxs-lookup"><span data-stu-id="48641-107">The following table shows conventions used for file names.</span></span>



| <span data-ttu-id="48641-108">檔案</span><span class="sxs-lookup"><span data-stu-id="48641-108">File</span></span>        | <span data-ttu-id="48641-109">基底檔案名的預設部分</span><span class="sxs-lookup"><span data-stu-id="48641-109">Default portion of base file name</span></span> | <span data-ttu-id="48641-110">範例</span><span class="sxs-lookup"><span data-stu-id="48641-110">Example</span></span>      |
|-------------|-----------------------------------|--------------|
| <span data-ttu-id="48641-111">IDL 檔案</span><span class="sxs-lookup"><span data-stu-id="48641-111">IDL file</span></span>    | ---                               | <span data-ttu-id="48641-112">Abcdefgh .idl</span><span class="sxs-lookup"><span data-stu-id="48641-112">Abcdefgh.idl</span></span> |
| <span data-ttu-id="48641-113">標頭</span><span class="sxs-lookup"><span data-stu-id="48641-113">Header</span></span>      | <span data-ttu-id="48641-114">.h</span><span class="sxs-lookup"><span data-stu-id="48641-114">.h</span></span>                                | <span data-ttu-id="48641-115">Abcdef。h</span><span class="sxs-lookup"><span data-stu-id="48641-115">Abcdef.h</span></span>     |
| <span data-ttu-id="48641-116">用戶端存根</span><span class="sxs-lookup"><span data-stu-id="48641-116">Client stub</span></span> | <span data-ttu-id="48641-117">\_c. c</span><span class="sxs-lookup"><span data-stu-id="48641-117">\_c.c</span></span>                             | <span data-ttu-id="48641-118">Abcdef \_ c。</span><span class="sxs-lookup"><span data-stu-id="48641-118">Abcdef\_c.c</span></span>  |
| <span data-ttu-id="48641-119">伺服器 stub</span><span class="sxs-lookup"><span data-stu-id="48641-119">Server stub</span></span> | <span data-ttu-id="48641-120">\_s. c</span><span class="sxs-lookup"><span data-stu-id="48641-120">\_s.c</span></span>                             | <span data-ttu-id="48641-121">Abcdef \_ s. c</span><span class="sxs-lookup"><span data-stu-id="48641-121">Abcdef\_s.c</span></span>  |



 

 

 




