---
title: ScriptFile
description: ScriptFile 屬性會指定隨附 JScript 檔案的檔案名。
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- ScriptFile Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976179"
---
# <a name="viewscriptfile"></a><span data-ttu-id="dd9af-104">ScriptFile</span><span class="sxs-lookup"><span data-stu-id="dd9af-104">VIEW.scriptFile</span></span>

<span data-ttu-id="dd9af-105">**ScriptFile** 屬性會指定隨附 JScript 檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="dd9af-105">The **scriptFile** attribute specifies the file names of accompanying JScript files.</span></span>

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a><span data-ttu-id="dd9af-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="dd9af-106">Possible Values</span></span>

<span data-ttu-id="dd9af-107">這個屬性是僅限寫入的 **字串** ，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="dd9af-107">This attribute is a write-only **String** with no default value.</span></span> <span data-ttu-id="dd9af-108">多個 JScript 檔案的檔案名會以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="dd9af-108">The file names of multiple JScript files are delimited with semicolons.</span></span> <span data-ttu-id="dd9af-109">開頭和後面不應出現空格和分號。</span><span class="sxs-lookup"><span data-stu-id="dd9af-109">Leading and following spaces and semicolons should not be present.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd9af-110">備註</span><span class="sxs-lookup"><span data-stu-id="dd9af-110">Remarks</span></span>

<span data-ttu-id="dd9af-111">指定檔案中的程式碼可供視圖中的任何事件處理常式使用。</span><span class="sxs-lookup"><span data-stu-id="dd9af-111">The code in the specified files can be used by any event handler in the View.</span></span> <span data-ttu-id="dd9af-112">多個視圖中的事件處理常式所使用的程式碼，可以放在與面板定義檔同名的檔案中，但是使用 .js 副檔名，而不是 wms 副檔名。</span><span class="sxs-lookup"><span data-stu-id="dd9af-112">Code that is used by event handlers in multiple Views can be placed in a file with the same name as the skin definition file but with a .js extension instead of a .wms extension.</span></span> <span data-ttu-id="dd9af-113">此檔案會自動載入，且不需要在外觀定義檔中指定。</span><span class="sxs-lookup"><span data-stu-id="dd9af-113">This file is loaded automatically and need not be specified in the skin definition file.</span></span>

## <a name="examples"></a><span data-ttu-id="dd9af-114">範例</span><span class="sxs-lookup"><span data-stu-id="dd9af-114">Examples</span></span>


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a><span data-ttu-id="dd9af-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd9af-115">Requirements</span></span>



| <span data-ttu-id="dd9af-116">需求</span><span class="sxs-lookup"><span data-stu-id="dd9af-116">Requirement</span></span> | <span data-ttu-id="dd9af-117">值</span><span class="sxs-lookup"><span data-stu-id="dd9af-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="dd9af-118">版本</span><span class="sxs-lookup"><span data-stu-id="dd9af-118">Version</span></span><br/> | <span data-ttu-id="dd9af-119">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="dd9af-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd9af-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd9af-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd9af-121">**VIEW 元素**</span><span class="sxs-lookup"><span data-stu-id="dd9af-121">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





