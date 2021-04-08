---
title: MIDL 中的 ODL 語言功能
description: 物件描述語言 (ODL 屬於 MIDL 一部分的) 屬性、關鍵字、語句和指示詞。
ms.assetid: beca14a6-01c4-4605-b1c5-214d48a7f46a
keywords:
- MIDL 和 ODL MIDL，語言功能
- 在 MIDL 中 ODL MIDL
- ODL MIDL，屬性
- ODL MIDL，關鍵字
- ODL MIDL，語句
- ODL MIDL，指示詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e525322eb185e38303b387dc4aa0007322e713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840615"
---
# <a name="odl-language-features-in-midl"></a><span data-ttu-id="8fcb4-109">MIDL 中的 ODL 語言功能</span><span class="sxs-lookup"><span data-stu-id="8fcb4-109">ODL Language Features in MIDL</span></span>

> [!Note]  
> <span data-ttu-id="8fcb4-110">Mktyplib.exe 工具已淘汰。</span><span class="sxs-lookup"><span data-stu-id="8fcb4-110">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="8fcb4-111">請改用 MIDL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="8fcb4-111">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="8fcb4-112">下列主題列出物件描述語言 (ODL) 屬性、關鍵字、語句和指示詞，這些屬性現在是 Microsoft 介面定義語言 (MIDL) 的一部分：</span><span class="sxs-lookup"><span data-stu-id="8fcb4-112">The following topics list the Object Description Language (ODL) attributes, keywords, statements, and directives that are now part of the Microsoft Interface Definition Language (MIDL):</span></span>

-   [<span data-ttu-id="8fcb4-113">ODL 屬性</span><span class="sxs-lookup"><span data-stu-id="8fcb4-113">ODL Attributes</span></span>](#odl-attributes)
-   [<span data-ttu-id="8fcb4-114">ODL 關鍵字、語句和指示詞</span><span class="sxs-lookup"><span data-stu-id="8fcb4-114">ODL Keywords, Statements, and Directives</span></span>](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a><span data-ttu-id="8fcb4-115">ODL 屬性</span><span class="sxs-lookup"><span data-stu-id="8fcb4-115">ODL Attributes</span></span>



|                                            |                                        |
|--------------------------------------------|----------------------------------------|
| <span data-ttu-id="8fcb4-116">\[[**appobject**](appobject.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-116">\[[**appobject**](appobject.md)\]</span></span>         | <span data-ttu-id="8fcb4-117">\[[**可系結**](bindable.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-117">\[[**bindable**](bindable.md)\]</span></span>       |
| <span data-ttu-id="8fcb4-118">\[[**控制**](control.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-118">\[[**control**](control.md)\]</span></span>             | <span data-ttu-id="8fcb4-119">\[[**預設**](default.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-119">\[[**default**](default.md)\]</span></span>         |
| <span data-ttu-id="8fcb4-120">\[[**值**](defaultvalue.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-120">\[[**defaultvalue**](defaultvalue.md)\]</span></span>   | <span data-ttu-id="8fcb4-121">\[[**displaybind**](displaybind.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-121">\[[**displaybind**](displaybind.md)\]</span></span> |
| <span data-ttu-id="8fcb4-122">\[[**dllname**](dllname-str-.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-122">\[[**dllname**](dllname-str-.md)\]</span></span>        | <span data-ttu-id="8fcb4-123">\[[**雙**](dual.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-123">\[[**dual**](dual.md)\]</span></span>               |
| <span data-ttu-id="8fcb4-124">\[[**進入**](entry.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-124">\[[**entry**](entry.md)\]</span></span>                 | <span data-ttu-id="8fcb4-125">\[[**helpcoNtext**](helpcontext.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-125">\[[**helpcontext**](helpcontext.md)\]</span></span> |
| <span data-ttu-id="8fcb4-126">\[[**helpstring**](helpstring.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-126">\[[**helpstring**](helpstring.md)\]</span></span>       | <span data-ttu-id="8fcb4-127">\[[**helpfile**](helpfile.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-127">\[[**helpfile**](helpfile.md)\]</span></span>       |
| <span data-ttu-id="8fcb4-128">\[[**隱藏**](hidden.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-128">\[[**hidden**](hidden.md)\]</span></span>               | <span data-ttu-id="8fcb4-129">\[[**Id**](id.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-129">\[[**id**](id.md)\]</span></span>                   |
| <span data-ttu-id="8fcb4-130">\[[**immediatebind**](immediatebind.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-130">\[[**immediatebind**](immediatebind.md)\]</span></span> | <span data-ttu-id="8fcb4-131">\[[**在**](in.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-131">\[[**in**](in.md)\]</span></span>                   |
| <span data-ttu-id="8fcb4-132">\[[**Lcid**](lcid.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-132">\[[**lcid**](lcid.md)\]</span></span>                   | <span data-ttu-id="8fcb4-133">\[[**許可**](licensed.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-133">\[[**licensed**](licensed.md)\]</span></span>       |
| <span data-ttu-id="8fcb4-134">\[[**nonextensible**](nonextensible.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-134">\[[**nonextensible**](nonextensible.md)\]</span></span> | <span data-ttu-id="8fcb4-135">\[[**odl**](odl.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-135">\[[**odl**](odl.md)\]</span></span>                 |
| <span data-ttu-id="8fcb4-136">\[[**oleautomation**](oleautomation.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-136">\[[**oleautomation**](oleautomation.md)\]</span></span> | <span data-ttu-id="8fcb4-137">\[[**選**](optional.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-137">\[[**optional**](optional.md)\]</span></span>       |
| <span data-ttu-id="8fcb4-138">\[[**擴展**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-138">\[[**out**](out-idl.md)\]</span></span>                 | <span data-ttu-id="8fcb4-139">\[[**propget**](propget.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-139">\[[**propget**](propget.md)\]</span></span>         |
| <span data-ttu-id="8fcb4-140">\[[**propput**](propput.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-140">\[[**propput**](propput.md)\]</span></span>             | <span data-ttu-id="8fcb4-141">\[[**propputref**](propputref.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-141">\[[**propputref**](propputref.md)\]</span></span>   |
| <span data-ttu-id="8fcb4-142">\[[**公共**](public.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-142">\[[**public**](public.md)\]</span></span>               | <span data-ttu-id="8fcb4-143">\[[ **readonly**](readonly.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-143">\[ [**readonly**](readonly.md)\]</span></span>      |
| <span data-ttu-id="8fcb4-144">\[[**requestedit**](requestedit.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-144">\[[**requestedit**](requestedit.md)\]</span></span>     | <span data-ttu-id="8fcb4-145">\[[**限制**](restricted.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-145">\[[**restricted**](restricted.md)\]</span></span>   |
| <span data-ttu-id="8fcb4-146">\[[**retval**](retval.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-146">\[[**retval**](retval.md)\]</span></span>               | <span data-ttu-id="8fcb4-147">\[[**源**](source.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-147">\[[**source**](source.md)\]</span></span>           |
| <span data-ttu-id="8fcb4-148">\[[**Uuid**](uuid.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-148">\[[**uuid**](uuid.md)\]</span></span>                   | <span data-ttu-id="8fcb4-149">[**vararg**](vararg.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-149">[**vararg**](vararg.md)\]</span></span>             |
| <span data-ttu-id="8fcb4-150">\[[**版本**](version.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-150">\[[**version**](version.md)\]</span></span>             | <span data-ttu-id="8fcb4-151">Â</span><span class="sxs-lookup"><span data-stu-id="8fcb4-151">Â</span></span>                                      |



 

## <a name="odl-keywords-statements-and-directives"></a><span data-ttu-id="8fcb4-152">ODL 關鍵字、語句和指示詞</span><span class="sxs-lookup"><span data-stu-id="8fcb4-152">ODL Keywords, Statements, and Directives</span></span>



|                                        |
|----------------------------------------|
| [<span data-ttu-id="8fcb4-153">**coclass**</span><span class="sxs-lookup"><span data-stu-id="8fcb4-153">**coclass**</span></span>](coclass.md)             |
| [<span data-ttu-id="8fcb4-154">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="8fcb4-154">**dispinterface**</span></span>](dispinterface.md) |
| [<span data-ttu-id="8fcb4-155">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="8fcb4-155">**enum**</span></span>](enum.md)                   |
| <span data-ttu-id="8fcb4-156">\[[**importlib**](importlib.md)\]</span><span class="sxs-lookup"><span data-stu-id="8fcb4-156">\[[**importlib**](importlib.md)\]</span></span>     |
| [<span data-ttu-id="8fcb4-157">**介面**</span><span class="sxs-lookup"><span data-stu-id="8fcb4-157">**interface**</span></span>](interface.md)         |
| [<span data-ttu-id="8fcb4-158">**圖書館**</span><span class="sxs-lookup"><span data-stu-id="8fcb4-158">**library**</span></span>](library.md)             |
| [<span data-ttu-id="8fcb4-159">**模組**</span><span class="sxs-lookup"><span data-stu-id="8fcb4-159">**module**</span></span>](module.md)               |
| [<span data-ttu-id="8fcb4-160">**結構**</span><span class="sxs-lookup"><span data-stu-id="8fcb4-160">**struct**</span></span>](struct.md)               |
| [<span data-ttu-id="8fcb4-161">**著**</span><span class="sxs-lookup"><span data-stu-id="8fcb4-161">**typedef**</span></span>](typedef.md)             |
| [<span data-ttu-id="8fcb4-162">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="8fcb4-162">**union**</span></span>](union.md)                 |



 

<span data-ttu-id="8fcb4-163">如需有關如何封送處理 OLE Automation 型別（例如 **BSTR**、 **VARIANT** 和 **SAFEARRAY**）的詳細資訊，請參閱 [封送處理 ole 資料類型](marshaling-ole-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="8fcb4-163">For information on how to marshal OLE Automation types, such as **BSTR**, **VARIANT**, and **SAFEARRAY**, see [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




