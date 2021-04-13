---
title: " include 指示詞"
description: 預處理器指示詞，可將指定檔案的內容插入來來源程式中指示詞出現的位置。
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- include 指示詞 HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a844459234200ca99233eb3f64a2a1c30449cdcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990942"
---
# <a name="include-directive"></a><span data-ttu-id="f48e3-104">\#include 指示詞</span><span class="sxs-lookup"><span data-stu-id="f48e3-104">\#include Directive</span></span>

<span data-ttu-id="f48e3-105">預處理器指示詞，可將指定檔案的內容插入來來源程式中指示詞出現的位置。</span><span class="sxs-lookup"><span data-stu-id="f48e3-105">Preprocessor directive that inserts the contents of the specified file into the source program at the point where the directive appears.</span></span>


| <span data-ttu-id="f48e3-106">\#包含 "*filename*"</span><span class="sxs-lookup"><span data-stu-id="f48e3-106">\#include "*filename*"</span></span>       |
|------------------------------|
| <span data-ttu-id="f48e3-107">\#包含 <*檔案名*></span><span class="sxs-lookup"><span data-stu-id="f48e3-107">\#include <*filename*></span></span> |

## <a name="parameters"></a><span data-ttu-id="f48e3-108">參數</span><span class="sxs-lookup"><span data-stu-id="f48e3-108">Parameters</span></span>

| <span data-ttu-id="f48e3-109">項目</span><span class="sxs-lookup"><span data-stu-id="f48e3-109">Item</span></span> | <span data-ttu-id="f48e3-110">描述</span><span class="sxs-lookup"><span data-stu-id="f48e3-110">Description</span></span> |
|------|-------------|
| <span data-ttu-id="f48e3-111">*filename*</span><span class="sxs-lookup"><span data-stu-id="f48e3-111">*filename*</span></span> | <span data-ttu-id="f48e3-112">要包含之檔案的檔案名（選擇性地在前面加上目錄規格）。</span><span class="sxs-lookup"><span data-stu-id="f48e3-112">Filename of the file to include, optionally preceded by a directory specification.</span></span> <span data-ttu-id="f48e3-113">檔案名必須指定現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="f48e3-113">The filename must specify an existing file.</span></span> |

## <a name="remarks"></a><span data-ttu-id="f48e3-114">備註</span><span class="sxs-lookup"><span data-stu-id="f48e3-114">Remarks</span></span>

<span data-ttu-id="f48e3-115">\#Include 指示詞會導致指定檔案的整個內容取代指示詞。</span><span class="sxs-lookup"><span data-stu-id="f48e3-115">The \#include directive causes replacement of the directive by the entire contents of the specified file.</span></span> <span data-ttu-id="f48e3-116">當預處理器找到具有指定名稱的檔案時，就會立即停止搜尋;如果您為檔案指定完整、明確的路徑規格，預處理器只會搜尋指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="f48e3-116">The preprocessor stops searching as soon as it finds a file with the specified name; if you specify a complete, unambiguous path specification for the file, the preprocessor searches only the specified path.</span></span>

> [!NOTE]
> <span data-ttu-id="f48e3-117">[效果編譯器工具](/windows/desktop/direct3dtools/fxc)具有使用/i 參數的內建 include 處理常式。</span><span class="sxs-lookup"><span data-stu-id="f48e3-117">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) has a built-in include handler using the /I switch.</span></span> <span data-ttu-id="f48e3-118">不過，從 API 執行編譯器時，您可以藉由執行 ID3DXInclude 介面提供自訂的 include 處理常式。</span><span class="sxs-lookup"><span data-stu-id="f48e3-118">However, when executing the compiler from the API, you can provide a customized include handler by implementing the ID3DXInclude interface.</span></span>

<span data-ttu-id="f48e3-119">這兩種語法形式之間的差異在於，當路徑未完成指定時，預處理器會搜尋標頭檔的順序，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="f48e3-119">The difference between the two syntax forms is the order in which the preprocessor searches for header files when the path is incompletely specified, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f48e3-120">語法形式</span><span class="sxs-lookup"><span data-stu-id="f48e3-120">Syntax form</span></span></th>
<th><span data-ttu-id="f48e3-121">預處理器搜尋模式</span><span class="sxs-lookup"><span data-stu-id="f48e3-121">Preprocessor search pattern</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f48e3-122">#包含 <b>&quot;</b> <em>檔案名</em><b>&quot;</b></span><span class="sxs-lookup"><span data-stu-id="f48e3-122">#include <b>&quot;</b><em>filename</em><b>&quot;</b></span></span></td>
<td><span data-ttu-id="f48e3-123">搜尋 include 檔：</span><span class="sxs-lookup"><span data-stu-id="f48e3-123">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="f48e3-124">在與包含 #include 指示詞的檔案相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="f48e3-124">in the same directory as the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="f48e3-125">在包含 #include 指示詞之檔案的 #include 指示詞之任何檔案的目錄中。</span><span class="sxs-lookup"><span data-stu-id="f48e3-125">in the directories of any files that contain a #include directive for the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="f48e3-126">在/I 編譯器選項指定的路徑中，依列出的順序排列。</span><span class="sxs-lookup"><span data-stu-id="f48e3-126">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="f48e3-127">在 INCLUDE 環境變數所指定的路徑中，依列出的順序排列。</span><span class="sxs-lookup"><span data-stu-id="f48e3-127">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="f48e3-128">在開發環境中會忽略 INCLUDE 環境變數。</span><span class="sxs-lookup"><span data-stu-id="f48e3-128">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="f48e3-129">請參閱您開發環境的檔，以取得如何設定專案包含路徑的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f48e3-129">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f48e3-130">#包含 <b><</b> <em>檔案名</em><b>></b></span><span class="sxs-lookup"><span data-stu-id="f48e3-130">#include <b><</b><em>filename</em><b>></b></span></span></td>
<td><span data-ttu-id="f48e3-131">搜尋 include 檔：</span><span class="sxs-lookup"><span data-stu-id="f48e3-131">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="f48e3-132">在/I 編譯器選項指定的路徑中，依列出的順序排列。</span><span class="sxs-lookup"><span data-stu-id="f48e3-132">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="f48e3-133">在 INCLUDE 環境變數所指定的路徑中，依列出的順序排列。</span><span class="sxs-lookup"><span data-stu-id="f48e3-133">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="f48e3-134">在開發環境中會忽略 INCLUDE 環境變數。</span><span class="sxs-lookup"><span data-stu-id="f48e3-134">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="f48e3-135">請參閱您開發環境的檔，以取得如何設定專案包含路徑的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f48e3-135">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a><span data-ttu-id="f48e3-136">範例</span><span class="sxs-lookup"><span data-stu-id="f48e3-136">Examples</span></span>

<span data-ttu-id="f48e3-137">下列範例會讓預處理器將 include 指示詞取代為 \# stdio.h 的內容。</span><span class="sxs-lookup"><span data-stu-id="f48e3-137">The following example causes the preprocessor to replace the \#include directive with the contents of stdio.h.</span></span> <span data-ttu-id="f48e3-138">因為此範例使用角括弧格式，預處理器只會在/I 編譯器選項和 INCLUDE 環境變數所列的目錄中搜尋檔案。</span><span class="sxs-lookup"><span data-stu-id="f48e3-138">Because the example uses the angle bracket format, the preprocessor will search for the file only in the directories listed by the /I compiler option and the INCLUDE environment variable.</span></span>

```cpp
#include <stdio.h>
```

## <a name="see-also"></a><span data-ttu-id="f48e3-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f48e3-139">See also</span></span>

- [<span data-ttu-id="f48e3-140"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="f48e3-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)

- <span data-ttu-id="f48e3-141">[ID3D10Include 介面](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f48e3-141">[ID3D10Include Interface](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>

- [<span data-ttu-id="f48e3-142">效果-編譯器工具</span><span class="sxs-lookup"><span data-stu-id="f48e3-142">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)