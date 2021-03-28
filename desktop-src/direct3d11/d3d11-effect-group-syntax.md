---
title: " (Direct3D 11) 的效果群組語法"
description: 使用本節所述的語法來宣告效果群組。
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9221341810990801f1ed07005e0dcb917df42360
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104462609"
---
# <a name="effect-group-syntax-direct3d-11"></a><span data-ttu-id="dcffb-103"> (Direct3D 11) 的效果群組語法</span><span class="sxs-lookup"><span data-stu-id="dcffb-103">Effect Group Syntax (Direct3D 11)</span></span>

<span data-ttu-id="dcffb-104">使用本節所述的語法來宣告效果群組。</span><span class="sxs-lookup"><span data-stu-id="dcffb-104">An effect group is declared with the syntax described in this section.</span></span>


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a><span data-ttu-id="dcffb-105">參數</span><span class="sxs-lookup"><span data-stu-id="dcffb-105">Parameters</span></span>



| <span data-ttu-id="dcffb-106">項目</span><span class="sxs-lookup"><span data-stu-id="dcffb-106">Item</span></span>                                                                                                                                                                           | <span data-ttu-id="dcffb-107">描述</span><span class="sxs-lookup"><span data-stu-id="dcffb-107">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcffb-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span><span class="sxs-lookup"><span data-stu-id="dcffb-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span></span><br/>                                                                                                         | <span data-ttu-id="dcffb-109">equired 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="dcffb-109">equired keyword.</span></span><br/>                                                                                                                                                                                                         |
| <span data-ttu-id="dcffb-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span><span class="sxs-lookup"><span data-stu-id="dcffb-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span></span><br/>                                                                       | <span data-ttu-id="dcffb-111">必要。</span><span class="sxs-lookup"><span data-stu-id="dcffb-111">Required.</span></span> <span data-ttu-id="dcffb-112">可唯一識別效果群組名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="dcffb-112">An ASCII string that uniquely identifies the name of the effect group.</span></span> <span data-ttu-id="dcffb-113">不同于技術，群組必須有名稱，以確保技術有唯一的識別碼 (請參閱下面) 的 [群組和技術] 區段。</span><span class="sxs-lookup"><span data-stu-id="dcffb-113">Unlike techniques, groups must have names to ensure that techniques have a unique identifier (see Groups and Techniques section below).</span></span><br/> |
| <span data-ttu-id="dcffb-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < 注釋 ></span><span class="sxs-lookup"><span data-stu-id="dcffb-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < Annotations ></span></span><br/> | <span data-ttu-id="dcffb-115">\[（ \] 選擇性）。</span><span class="sxs-lookup"><span data-stu-id="dcffb-115">\[in\] Optional.</span></span> <span data-ttu-id="dcffb-116"> (中繼資料) 的一或多個使用者提供的資訊，會被效果系統忽略。</span><span class="sxs-lookup"><span data-stu-id="dcffb-116">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="dcffb-117">如需語法，請參閱 (Direct3D 11) 的批註語法。</span><span class="sxs-lookup"><span data-stu-id="dcffb-117">For syntax, see Annotation Syntax (Direct3D 11).</span></span> <br/>                                                      |
| <span data-ttu-id="dcffb-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span><span class="sxs-lookup"><span data-stu-id="dcffb-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/>                                           | <span data-ttu-id="dcffb-119">可能是 "technique10" 或 "technique11"。</span><span class="sxs-lookup"><span data-stu-id="dcffb-119">Either "technique10" or "technique11".</span></span> <span data-ttu-id="dcffb-120">使用 Direct3D 11 的新功能 (5 \_ 0 著色器、BindInterfaces 等) 的技巧必須使用 "technique11"。</span><span class="sxs-lookup"><span data-stu-id="dcffb-120">Techniques which use functionality new to Direct3D 11 (5\_0 shaders, BindInterfaces, etc) must use "technique11".</span></span><br/>                                                                 |
| <span data-ttu-id="dcffb-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName</span><span class="sxs-lookup"><span data-stu-id="dcffb-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName</span></span><br/>                                                       | <span data-ttu-id="dcffb-122">選擇性。</span><span class="sxs-lookup"><span data-stu-id="dcffb-122">Optional.</span></span> <span data-ttu-id="dcffb-123">可唯一識別效果技巧名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="dcffb-123">An ASCII string that uniquely identifies the name of the effect technique.</span></span> <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a><span data-ttu-id="dcffb-124">群組和技巧</span><span class="sxs-lookup"><span data-stu-id="dcffb-124">Groups and Techniques</span></span>

<span data-ttu-id="dcffb-125">為了維持與 fx \_ 4 0 效果的相容性 \_ ，群組是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="dcffb-125">In order to maintain compatibility with fx\_4\_0 effects, groups are optional.</span></span> <span data-ttu-id="dcffb-126">所有全域技術都有隱含的 Null 命名群組。</span><span class="sxs-lookup"><span data-stu-id="dcffb-126">There is an implicit NULL-named group surrounding all global techniques.</span></span>

<span data-ttu-id="dcffb-127">請考慮下列範例：</span><span class="sxs-lookup"><span data-stu-id="dcffb-127">Consider the following example:</span></span>


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



<span data-ttu-id="dcffb-128">在 c + + 中，有兩種方式可以依名稱取得技巧。</span><span class="sxs-lookup"><span data-stu-id="dcffb-128">In C++, one can get a technique by name in two ways.</span></span> <span data-ttu-id="dcffb-129">下列命令會尋找明顯的技巧：</span><span class="sxs-lookup"><span data-stu-id="dcffb-129">The following commands will find the obvious techniques:</span></span>


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



<span data-ttu-id="dcffb-130">為了確保 [**ID3DX11Effect：： GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) 的運作方式類似于效果10，所有定義的群組都必須有名稱。</span><span class="sxs-lookup"><span data-stu-id="dcffb-130">In order to ensure that [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) works similarly to Effects 10, all defined groups must have a name.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dcffb-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="dcffb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcffb-132">效果格式</span><span class="sxs-lookup"><span data-stu-id="dcffb-132">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="dcffb-133"> (Direct3D 11) 的效果技巧語法 </span><span class="sxs-lookup"><span data-stu-id="dcffb-133">Effect Technique Syntax (Direct3D 11)</span></span>](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





