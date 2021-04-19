---
description: 描述命名空間。
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: nameSpace 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2414919f699bb60c2cf1e48bc52030c36cf67a0
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380842"
---
# <a name="namespace-element"></a><span data-ttu-id="30f77-103">nameSpace 元素</span><span class="sxs-lookup"><span data-stu-id="30f77-103">nameSpace element</span></span>

<span data-ttu-id="30f77-104">描述命名空間。</span><span class="sxs-lookup"><span data-stu-id="30f77-104">Describes a namespace.</span></span> <span data-ttu-id="30f77-105">這個命名空間可用於產生程式碼或處理指示詞 \<wsdl:import> 。</span><span class="sxs-lookup"><span data-stu-id="30f77-105">This namespace may be used for code generation or for handling \<wsdl:import> directives.</span></span>

## <a name="usage"></a><span data-ttu-id="30f77-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="30f77-106">Usage</span></span>

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a><span data-ttu-id="30f77-107">屬性</span><span class="sxs-lookup"><span data-stu-id="30f77-107">Attributes</span></span>



| <span data-ttu-id="30f77-108">屬性</span><span class="sxs-lookup"><span data-stu-id="30f77-108">Attribute</span></span>          | <span data-ttu-id="30f77-109">類型</span><span class="sxs-lookup"><span data-stu-id="30f77-109">Type</span></span>                         | <span data-ttu-id="30f77-110">必要</span><span class="sxs-lookup"><span data-stu-id="30f77-110">Required</span></span>       | <span data-ttu-id="30f77-111">描述</span><span class="sxs-lookup"><span data-stu-id="30f77-111">Description</span></span>                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="30f77-112">**uri**</span><span class="sxs-lookup"><span data-stu-id="30f77-112">**uri**</span></span><br/> | <span data-ttu-id="30f77-113">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="30f77-113">character\_string</span></span><br/> | <span data-ttu-id="30f77-114">是</span><span class="sxs-lookup"><span data-stu-id="30f77-114">Yes</span></span><br/> | <span data-ttu-id="30f77-115">命名空間的唯一 URI。</span><span class="sxs-lookup"><span data-stu-id="30f77-115">The unique URI of the namespace.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="30f77-116">子元素</span><span class="sxs-lookup"><span data-stu-id="30f77-116">Child elements</span></span>



| <span data-ttu-id="30f77-117">元素</span><span class="sxs-lookup"><span data-stu-id="30f77-117">Element</span></span>                                               | <span data-ttu-id="30f77-118">描述</span><span class="sxs-lookup"><span data-stu-id="30f77-118">Description</span></span>                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30f77-119">**代號**</span><span class="sxs-lookup"><span data-stu-id="30f77-119">**codeName**</span></span>](codename.md)<br/>               | <span data-ttu-id="30f77-120">用來在產生的程式碼中識別命名空間的名稱。</span><span class="sxs-lookup"><span data-stu-id="30f77-120">The name to be used to identify the namespace in generated code.</span></span><br/> <br/>                  |
| [<span data-ttu-id="30f77-121">**macroPrefix**</span><span class="sxs-lookup"><span data-stu-id="30f77-121">**macroPrefix**</span></span>](macroprefix.md)<br/>         | <span data-ttu-id="30f77-122">在命名空間中宏名稱所產生的程式碼中，所要使用的前置詞。</span><span class="sxs-lookup"><span data-stu-id="30f77-122">The prefix to be used in the generated code for names of macros in the namespace.</span></span><br/> <br/> |
| [<span data-ttu-id="30f77-123">**名字**</span><span class="sxs-lookup"><span data-stu-id="30f77-123">**name**</span></span>](name.md)<br/>                       | <span data-ttu-id="30f77-124">命名空間中的限定名稱。</span><span class="sxs-lookup"><span data-stu-id="30f77-124">A qualified name in the namespace.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="30f77-125">**preferredPrefix**</span><span class="sxs-lookup"><span data-stu-id="30f77-125">**preferredPrefix**</span></span>](preferredprefix.md)<br/> | <span data-ttu-id="30f77-126">應對應命名空間的前置詞，讓 XML 更容易讀取。</span><span class="sxs-lookup"><span data-stu-id="30f77-126">The prefix to which the namespace should be mapped to make the XML more readable.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="30f77-127">子項目順序</span><span class="sxs-lookup"><span data-stu-id="30f77-127">Child element sequence</span></span>

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a><span data-ttu-id="30f77-128">父元素</span><span class="sxs-lookup"><span data-stu-id="30f77-128">Parent elements</span></span>



| <span data-ttu-id="30f77-129">元素</span><span class="sxs-lookup"><span data-stu-id="30f77-129">Element</span></span>                                     | <span data-ttu-id="30f77-130">描述</span><span class="sxs-lookup"><span data-stu-id="30f77-130">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="30f77-131">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="30f77-131">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="30f77-132">WSDAPI 程式碼產生器 XML 腳本檔的根項目。</span><span class="sxs-lookup"><span data-stu-id="30f77-132">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="30f77-133">備註</span><span class="sxs-lookup"><span data-stu-id="30f77-133">Remarks</span></span>

<span data-ttu-id="30f77-134">這個元素可用來提供程式碼產生器，其中包含在 WSDL 和 XSD 檔案中遇到之命名空間的其他相關資訊，或引進新的命名空間。</span><span class="sxs-lookup"><span data-stu-id="30f77-134">This element may be used to provide the code generator with additional information about namespaces that it encounters in WSDL and XSD files or to introduce new namespaces.</span></span>

<span data-ttu-id="30f77-135">由程式碼產生器會自動剖析型別反映所隱含或在 WSDL 和 XSD 檔案中指定的命名空間，而不需要在腳本中明確定義。</span><span class="sxs-lookup"><span data-stu-id="30f77-135">Namespaces implied by type reflection or specified in WSDL and XSD files are parsed automatically by the code generator and do not have to be explicitly defined in the script.</span></span> <span data-ttu-id="30f77-136">在某些情況下，這個專案可以用來將其他屬性或名稱加入至類型反映或 WSDL/XSD 所參考的命名空間。</span><span class="sxs-lookup"><span data-stu-id="30f77-136">In some cases, this element can be used to add additional properties or names to a namespace that is referenced by type reflection or WSDL/XSD.</span></span> <span data-ttu-id="30f77-137">程式碼產生器不會將此視為衝突。</span><span class="sxs-lookup"><span data-stu-id="30f77-137">The code generator does not regard this as a conflict.</span></span>

<span data-ttu-id="30f77-138">下列 XML 會顯示命名空間元素 (已省略子系，以求簡潔) 。</span><span class="sxs-lookup"><span data-stu-id="30f77-138">The following XML shows a nameSpace element (with children omitted for brevity).</span></span>

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a><span data-ttu-id="30f77-139">項目資訊</span><span class="sxs-lookup"><span data-stu-id="30f77-139">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="30f77-140">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="30f77-140">Minimum supported system</span></span><br/> | <span data-ttu-id="30f77-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30f77-141">Windows Vista</span></span> |
| <span data-ttu-id="30f77-142">可以是空的</span><span class="sxs-lookup"><span data-stu-id="30f77-142">Can be empty</span></span>                        | <span data-ttu-id="30f77-143">是</span><span class="sxs-lookup"><span data-stu-id="30f77-143">Yes</span></span>           |



 

 




