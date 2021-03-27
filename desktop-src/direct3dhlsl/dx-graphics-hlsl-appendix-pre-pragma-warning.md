---
title: warning pragma 指示詞
description: 修改編譯器警告訊息行為的 Pragma 指示詞。
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- 警告 pragma 指示詞 HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7599886b47830b33c69f11c0c341c7775c644dd3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932696"
---
# <a name="warning-pragma-directive"></a><span data-ttu-id="c6977-104">warning pragma 指示詞</span><span class="sxs-lookup"><span data-stu-id="c6977-104">warning pragma Directive</span></span>

<span data-ttu-id="c6977-105">修改編譯器警告訊息行為的 Pragma 指示詞。</span><span class="sxs-lookup"><span data-stu-id="c6977-105">Pragma directive that modifies the behavior of compiler warning messages.</span></span>



| <span data-ttu-id="c6977-106">\#pragma 警告 ( *警告-規範* ： *警告-數位-清單* \[ ; *警告-規範* ： *警告-數位-清單*... \] ) </span><span class="sxs-lookup"><span data-stu-id="c6977-106">\#pragma warning( *warning-specifier* : *warning-number-list* \[; *warning-specifier* : *warning-number-list*...\] )</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="c6977-107">參數</span><span class="sxs-lookup"><span data-stu-id="c6977-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c6977-108">項目</span><span class="sxs-lookup"><span data-stu-id="c6977-108">Item</span></span></th>
<th><span data-ttu-id="c6977-109">描述</span><span class="sxs-lookup"><span data-stu-id="c6977-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6977-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>warning-規範</em></span><span class="sxs-lookup"><span data-stu-id="c6977-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>warning-specifier</em></span></span><br/></td>
<td><span data-ttu-id="c6977-111">要針對指定的警告設定的行為。</span><span class="sxs-lookup"><span data-stu-id="c6977-111">Behavior to set for the specified warnings.</span></span> <span data-ttu-id="c6977-112">此參數可以採用下表所列的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c6977-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c6977-113">值</span><span class="sxs-lookup"><span data-stu-id="c6977-113">Value</span></span></th>
<th><span data-ttu-id="c6977-114">描述</span><span class="sxs-lookup"><span data-stu-id="c6977-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6977-115">once</span><span class="sxs-lookup"><span data-stu-id="c6977-115">once</span></span></td>
<td><span data-ttu-id="c6977-116">只顯示指定數位一次的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="c6977-116">Display the message of the warnings with the specified numbers only once.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6977-117">預設</span><span class="sxs-lookup"><span data-stu-id="c6977-117">default</span></span></td>
<td><span data-ttu-id="c6977-118">將具有指定數位之警告的行為重設為其預設值。</span><span class="sxs-lookup"><span data-stu-id="c6977-118">Reset the behavior of the warnings with the specified numbers to their default value.</span></span> <span data-ttu-id="c6977-119">這也具有開啟警告的效果（預設為關閉）。</span><span class="sxs-lookup"><span data-stu-id="c6977-119">This also has the effect of turning a warning on that is off by default.</span></span> <span data-ttu-id="c6977-120">警告會在其預設層級產生。</span><span class="sxs-lookup"><span data-stu-id="c6977-120">The warning will be generated at its default level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6977-121">1、2、3、4</span><span class="sxs-lookup"><span data-stu-id="c6977-121">1, 2, 3, 4</span></span></td>
<td><span data-ttu-id="c6977-122">將指定的層級套用至具有指定數位的警告。</span><span class="sxs-lookup"><span data-stu-id="c6977-122">Apply the specified level to the warnings with the specified numbers.</span></span> <span data-ttu-id="c6977-123">這也具有開啟警告的效果（預設為關閉）。</span><span class="sxs-lookup"><span data-stu-id="c6977-123">This also has the effect of turning a warning on that is off by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6977-124">disable</span><span class="sxs-lookup"><span data-stu-id="c6977-124">disable</span></span></td>
<td><span data-ttu-id="c6977-125">請勿發出具有指定數位的警告。</span><span class="sxs-lookup"><span data-stu-id="c6977-125">Do not issue the warnings with the specified numbers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6977-126">error</span><span class="sxs-lookup"><span data-stu-id="c6977-126">error</span></span></td>
<td><span data-ttu-id="c6977-127">以指定的數位將警告報告為錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6977-127">Report the warnings with the specified numbers as errors.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6977-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>警告-數位-清單</em></span><span class="sxs-lookup"><span data-stu-id="c6977-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>warning-number-list</em></span></span></p></td>
<td><p><span data-ttu-id="c6977-129">以空格分隔的清單，其中列出要修改其行為的警告數目。</span><span class="sxs-lookup"><span data-stu-id="c6977-129">White space-delimited list of the numbers of the warnings to modify the behavior of.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="c6977-130">備註</span><span class="sxs-lookup"><span data-stu-id="c6977-130">Remarks</span></span>

<span data-ttu-id="c6977-131">您可以使用分號分隔變更，在相同的警告 pragma 內指定任何數目的相異警告行為變更。</span><span class="sxs-lookup"><span data-stu-id="c6977-131">You can specify any number of distinct warning behavior changes within the same warning pragma by separating the changes with semicolons.</span></span>

<span data-ttu-id="c6977-132">編譯器會將4000加入至0和999之間的任何警告編號。</span><span class="sxs-lookup"><span data-stu-id="c6977-132">The compiler will add 4000 to any warning number that is between 0 and 999.</span></span> <span data-ttu-id="c6977-133">若為大於4699的警告編號， (與程式碼產生相關聯的警告編號) 警告 pragma 只有在放置於函式定義之外時才會生效。</span><span class="sxs-lookup"><span data-stu-id="c6977-133">For warning numbers greater than 4699, (those associated with code generation) the warning pragma has effect only when placed outside function definitions.</span></span> <span data-ttu-id="c6977-134">如果指定的數位大於4699，並在函式內使用，則會忽略 pragma。</span><span class="sxs-lookup"><span data-stu-id="c6977-134">The pragma is ignored if it specifies a number greater than 4699 and is used inside a function.</span></span>

<span data-ttu-id="c6977-135">HLSL 警告 pragma 不支援 c + + 編譯器中包含的 warning pragma 的 **push** 和 **pop** 功能。</span><span class="sxs-lookup"><span data-stu-id="c6977-135">The HLSL warning pragma does not support the **push** and **pop** functionality of the warning pragma included in the C++ compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="c6977-136">範例</span><span class="sxs-lookup"><span data-stu-id="c6977-136">Examples</span></span>

<span data-ttu-id="c6977-137">下列範例會停用警告4507和4034、顯示警告4385一次，並將警告4164報告為錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6977-137">The following example disables warnings 4507 and 4034, displays warning 4385 once once, and reports warning 4164 as an error.</span></span>


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



<span data-ttu-id="c6977-138">上述範例在功能上等同于下列專案：</span><span class="sxs-lookup"><span data-stu-id="c6977-138">The preceding example is functionally equivalent to the following:</span></span>


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a><span data-ttu-id="c6977-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6977-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6977-140"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="c6977-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="c6977-141">\# (DirectX HLSL) 的 pragma 指示詞 </span><span class="sxs-lookup"><span data-stu-id="c6977-141">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





