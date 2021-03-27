---
title: 'switch 語句 (Urlmon.dll) '
description: 將控制權傳輸至切換主體內的不同語句區塊（視選取器的值而定）。
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- switch 語句 HLSL
topic_type:
- apiref
api_name:
- switch Statement
api_location:
- urlmon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c65049acce4265dd2abdf849119aad5902db9e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696559"
---
# <a name="switch-statement"></a><span data-ttu-id="c78ac-104">switch 陳述式</span><span class="sxs-lookup"><span data-stu-id="c78ac-104">switch Statement</span></span>

<span data-ttu-id="c78ac-105">將控制權傳輸至切換主體內的不同語句區塊（視選取器的值而定）。</span><span class="sxs-lookup"><span data-stu-id="c78ac-105">Transfer control to a different statement block within the switch body depending on the value of a selector.</span></span>



|                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c78ac-106">\[*屬性* \]切換 (*選取器*) {case 0： { *StatementBlock*;}  折  案例1： { *StatementBlock*;}  折  案例 n： { *StatementBlock*;}  折  預設值： { *StatementBlock*;}  折</span><span class="sxs-lookup"><span data-stu-id="c78ac-106">\[*Attribute*\] switch( *Selector* ) {   case 0 :     { *StatementBlock*; }   break;   case 1 :     { *StatementBlock*; }   break;   case n :     { *StatementBlock*; }   break;   default :     { *StatementBlock*; }   break;</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="c78ac-107">參數</span><span class="sxs-lookup"><span data-stu-id="c78ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c78ac-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*屬性*</span><span class="sxs-lookup"><span data-stu-id="c78ac-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="c78ac-109">可控制如何編譯語句的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="c78ac-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="c78ac-110">未指定任何屬性時，編譯器可能會使用硬體參數或發出一系列的 **if** 語句。</span><span class="sxs-lookup"><span data-stu-id="c78ac-110">When no attribute is specified, the compiler may use a hardware switch or emit a series of **if** statements.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c78ac-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c78ac-111">Attribute</span></span></th>
<th><span data-ttu-id="c78ac-112">描述</span><span class="sxs-lookup"><span data-stu-id="c78ac-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c78ac-113">扁平化</span><span class="sxs-lookup"><span data-stu-id="c78ac-113">flatten</span></span></td>
<td><span data-ttu-id="c78ac-114">將語句編譯為一系列的 <strong>if</strong> 語句，每個語句都有壓 <strong>平</strong> 合併屬性。</span><span class="sxs-lookup"><span data-stu-id="c78ac-114">Compile the statement as a series of <strong>if</strong> statements, each with the <strong>flatten</strong> attribute.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c78ac-115">分支</span><span class="sxs-lookup"><span data-stu-id="c78ac-115">branch</span></span></td>
<td><span data-ttu-id="c78ac-116">將語句編譯為一系列的 <strong>if</strong> 語句，其中每個語句都有 <strong>分支</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="c78ac-116">Compile the statement as a series of <strong>if</strong> statements each with the <strong>branch</strong> attribute.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c78ac-117">當您使用 <a href="dx-graphics-hlsl-sm2.md">著色器模型</a> 2.X 或 <a href="dx-graphics-hlsl-sm3.md">著色器模型 3.0</a>時，每次使用動態分支都會耗用資源。</span><span class="sxs-lookup"><span data-stu-id="c78ac-117">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="c78ac-118">因此，如果您在以這些設定檔為目標時，過度使用動態分支，您可能會收到編譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="c78ac-118">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c78ac-119">forcecase</span><span class="sxs-lookup"><span data-stu-id="c78ac-119">forcecase</span></span></td>
<td><span data-ttu-id="c78ac-120">在硬體中強制執行 switch 語句。</span><span class="sxs-lookup"><span data-stu-id="c78ac-120">Force a switch statement in the hardware.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c78ac-121">需要 <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">功能層級</a> 10_0 或更新版本的硬體。</span><span class="sxs-lookup"><span data-stu-id="c78ac-121">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c78ac-122">call</span><span class="sxs-lookup"><span data-stu-id="c78ac-122">call</span></span></td>
<td><span data-ttu-id="c78ac-123">交換器中個別案例的內文將會移至硬體副程式，而參數將會是一連串的副程式呼叫。</span><span class="sxs-lookup"><span data-stu-id="c78ac-123">The bodies of the individual cases in the switch will be moved into hardware subroutines and the switch will be a series of subroutine calls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c78ac-124">需要 <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">功能層級</a> 10_0 或更新版本的硬體。</span><span class="sxs-lookup"><span data-stu-id="c78ac-124">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="c78ac-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*選擇*</span><span class="sxs-lookup"><span data-stu-id="c78ac-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*</span></span>
</dt> <dd>

<span data-ttu-id="c78ac-126">變數。</span><span class="sxs-lookup"><span data-stu-id="c78ac-126">A variable.</span></span> <span data-ttu-id="c78ac-127">大括弧內的 case 語句會各自檢查此變數，以查看 SwitchValue 是否符合其特定 CaseValue。</span><span class="sxs-lookup"><span data-stu-id="c78ac-127">The case statements inside the curly brackets will each check this variable to see if the SwitchValue matches their particular CaseValue.</span></span>

</dd> <dt>

<span data-ttu-id="c78ac-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="c78ac-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="c78ac-129">一或多個 [語句](dx-graphics-hlsl-statement-blocks.md)。</span><span class="sxs-lookup"><span data-stu-id="c78ac-129">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c78ac-130">備註</span><span class="sxs-lookup"><span data-stu-id="c78ac-130">Remarks</span></span>


```
[branch] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



<span data-ttu-id="c78ac-131">相當於：</span><span class="sxs-lookup"><span data-stu-id="c78ac-131">Is equivalent to:</span></span>


```
[branch] if( a == 2 )
    return 3;
else if( a == 1 )
    return 1;
else if( a == 0 )
    return 0;
else
    return 6;
```



<span data-ttu-id="c78ac-132">以下是 forcecase 和呼叫流程式控制制屬性的範例使用方式：</span><span class="sxs-lookup"><span data-stu-id="c78ac-132">Here are example usages of forcecase and call flow control attributes:</span></span>


```
[forcecase] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}

[call] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



## <a name="requirements"></a><span data-ttu-id="c78ac-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="c78ac-133">Requirements</span></span>



| <span data-ttu-id="c78ac-134">需求</span><span class="sxs-lookup"><span data-stu-id="c78ac-134">Requirement</span></span> | <span data-ttu-id="c78ac-135">值</span><span class="sxs-lookup"><span data-stu-id="c78ac-135">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c78ac-136">標頭</span><span class="sxs-lookup"><span data-stu-id="c78ac-136">Header</span></span><br/> | <dl> <span data-ttu-id="c78ac-137"><dt>Urlmon.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c78ac-137"><dt>Urlmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c78ac-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c78ac-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c78ac-139">流程式控制制</span><span class="sxs-lookup"><span data-stu-id="c78ac-139">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

