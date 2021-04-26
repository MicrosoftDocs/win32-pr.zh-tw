---
description: 將 C 或 IDL include 語句放在產生的程式碼中。
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: literalInclude 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1f43f1b8d3d95e2ad8a378dd1c8cbada7758ad
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995125"
---
# <a name="literalinclude-element"></a><span data-ttu-id="96e02-103">literalInclude 元素</span><span class="sxs-lookup"><span data-stu-id="96e02-103">literalInclude element</span></span>

<span data-ttu-id="96e02-104">將 C 或 IDL include 語句放在產生的程式碼中。</span><span class="sxs-lookup"><span data-stu-id="96e02-104">Places a C or IDL include statement in the generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="96e02-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="96e02-105">Usage</span></span>

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="96e02-106">屬性</span><span class="sxs-lookup"><span data-stu-id="96e02-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96e02-107">屬性</span><span class="sxs-lookup"><span data-stu-id="96e02-107">Attribute</span></span></th>
<th><span data-ttu-id="96e02-108">類型</span><span class="sxs-lookup"><span data-stu-id="96e02-108">Type</span></span></th>
<th><span data-ttu-id="96e02-109">必要</span><span class="sxs-lookup"><span data-stu-id="96e02-109">Required</span></span></th>
<th><span data-ttu-id="96e02-110">描述</span><span class="sxs-lookup"><span data-stu-id="96e02-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96e02-111"><strong>語言</strong></span><span class="sxs-lookup"><span data-stu-id="96e02-111"><strong>Language</strong></span></span><br/></td>
<td><span data-ttu-id="96e02-112">語言字串</span><span class="sxs-lookup"><span data-stu-id="96e02-112">language string</span></span><br/></td>
<td><span data-ttu-id="96e02-113">No</span><span class="sxs-lookup"><span data-stu-id="96e02-113">No</span></span><br/></td>
<td><span data-ttu-id="96e02-114">要包含的頭檔案類型。</span><span class="sxs-lookup"><span data-stu-id="96e02-114">The type of header file to be included.</span></span> <br/> <br/><span data-ttu-id="96e02-115">
<dt><strong>C</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="96e02-115">
<dt><strong>C</strong></dt> </span></span><dd> <span data-ttu-id="96e02-116">包含 C 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="96e02-116">Include a C header file.</span></span><br/> </dd> <span data-ttu-id="96e02-117"><dt><strong>Idl</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="96e02-117"><dt><strong>IDL</strong></dt> </span></span><dd> <span data-ttu-id="96e02-118">包含 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="96e02-118">Include an IDL file.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96e02-119"><strong>本機</strong></span><span class="sxs-lookup"><span data-stu-id="96e02-119"><strong>Local</strong></span></span><br/></td>
<td><span data-ttu-id="96e02-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="96e02-120">Boolean</span></span><br/></td>
<td><span data-ttu-id="96e02-121">No</span><span class="sxs-lookup"><span data-stu-id="96e02-121">No</span></span><br/></td>
<td><span data-ttu-id="96e02-122">只有當 <strong>語言</strong> 設定為 C 時，才會使用這個屬性 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="96e02-122">This attribute is only used when <strong>Language</strong> is set to &quot;C&quot;.</span></span><br/> <br/><span data-ttu-id="96e02-123">
<dt><strong>真</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="96e02-123">
<dt><strong>True</strong></dt> </span></span><dd> <span data-ttu-id="96e02-124">搜尋系統目錄之前，先在目前的目錄中搜尋指名的標頭。</span><span class="sxs-lookup"><span data-stu-id="96e02-124">Searches the current directory for the named header before searching the system directories.</span></span><br/> </dd> <span data-ttu-id="96e02-125"><dt><strong>假</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="96e02-125"><dt><strong>False</strong></dt> </span></span><dd> <span data-ttu-id="96e02-126">僅搜尋已命名標頭的系統目錄。</span><span class="sxs-lookup"><span data-stu-id="96e02-126">Only search system directories for the named header.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="96e02-127">子元素</span><span class="sxs-lookup"><span data-stu-id="96e02-127">Child elements</span></span>

<span data-ttu-id="96e02-128">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="96e02-128">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="96e02-129">父元素</span><span class="sxs-lookup"><span data-stu-id="96e02-129">Parent elements</span></span>



| <span data-ttu-id="96e02-130">元素</span><span class="sxs-lookup"><span data-stu-id="96e02-130">Element</span></span>                         | <span data-ttu-id="96e02-131">描述</span><span class="sxs-lookup"><span data-stu-id="96e02-131">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="96e02-132">**檔**</span><span class="sxs-lookup"><span data-stu-id="96e02-132">**file**</span></span>](file.md)<br/> | <span data-ttu-id="96e02-133">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="96e02-133">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="96e02-134">備註</span><span class="sxs-lookup"><span data-stu-id="96e02-134">Remarks</span></span>

<span data-ttu-id="96e02-135">下列範例顯示從不同的 **literalInclude** 元素產生的程式碼。</span><span class="sxs-lookup"><span data-stu-id="96e02-135">The following examples show the code generated from different **literalInclude** elements.</span></span>

### <a name="example-1---generating-a-c-include-statement"></a><span data-ttu-id="96e02-136">範例 1-產生 C include 語句</span><span class="sxs-lookup"><span data-stu-id="96e02-136">Example 1 - Generating a C include statement</span></span>

<span data-ttu-id="96e02-137">輸入 XML：</span><span class="sxs-lookup"><span data-stu-id="96e02-137">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

<span data-ttu-id="96e02-138">輸出碼：</span><span class="sxs-lookup"><span data-stu-id="96e02-138">Output code:</span></span>

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a><span data-ttu-id="96e02-139">範例 2-產生 C include 語句</span><span class="sxs-lookup"><span data-stu-id="96e02-139">Example 2 - Generating a C include statement</span></span>

<span data-ttu-id="96e02-140">輸入 XML：</span><span class="sxs-lookup"><span data-stu-id="96e02-140">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

<span data-ttu-id="96e02-141">輸出碼：</span><span class="sxs-lookup"><span data-stu-id="96e02-141">Output code:</span></span>

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a><span data-ttu-id="96e02-142">範例 3-產生 IDL 匯入語句</span><span class="sxs-lookup"><span data-stu-id="96e02-142">Example 3 - Generating an IDL import statement</span></span>

<span data-ttu-id="96e02-143">輸入 XML：</span><span class="sxs-lookup"><span data-stu-id="96e02-143">Input XML:</span></span>

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

<span data-ttu-id="96e02-144">輸出碼：</span><span class="sxs-lookup"><span data-stu-id="96e02-144">Output code:</span></span>

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a><span data-ttu-id="96e02-145">項目資訊</span><span class="sxs-lookup"><span data-stu-id="96e02-145">Element information</span></span>



| <span data-ttu-id="96e02-146">標籤</span><span class="sxs-lookup"><span data-stu-id="96e02-146">Label</span></span> | <span data-ttu-id="96e02-147">值</span><span class="sxs-lookup"><span data-stu-id="96e02-147">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="96e02-148">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="96e02-148">Minimum supported system</span></span><br/> | <span data-ttu-id="96e02-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96e02-149">Windows Vista</span></span> |
| <span data-ttu-id="96e02-150">可以是空的</span><span class="sxs-lookup"><span data-stu-id="96e02-150">Can be empty</span></span>                        | <span data-ttu-id="96e02-151">是</span><span class="sxs-lookup"><span data-stu-id="96e02-151">Yes</span></span>           |



 

 




