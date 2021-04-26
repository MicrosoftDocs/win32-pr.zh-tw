---
description: 在產生的輸出中包含宏或檔案的內容。
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: 包含元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8237ec865cd3cfbb80f500358e8f363be8f230
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995775"
---
# <a name="include-element"></a><span data-ttu-id="c1821-103">包含元素</span><span class="sxs-lookup"><span data-stu-id="c1821-103">include element</span></span>

<span data-ttu-id="c1821-104">在產生的輸出中包含宏或檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="c1821-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="c1821-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="c1821-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="c1821-106">屬性</span><span class="sxs-lookup"><span data-stu-id="c1821-106">Attributes</span></span>



| <span data-ttu-id="c1821-107">屬性</span><span class="sxs-lookup"><span data-stu-id="c1821-107">Attribute</span></span>            | <span data-ttu-id="c1821-108">類型</span><span class="sxs-lookup"><span data-stu-id="c1821-108">Type</span></span>                         | <span data-ttu-id="c1821-109">必要</span><span class="sxs-lookup"><span data-stu-id="c1821-109">Required</span></span>      | <span data-ttu-id="c1821-110">描述</span><span class="sxs-lookup"><span data-stu-id="c1821-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="c1821-111">**file**</span><span class="sxs-lookup"><span data-stu-id="c1821-111">**file**</span></span><br/>  | <span data-ttu-id="c1821-112">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="c1821-112">character\_string</span></span><br/> | <span data-ttu-id="c1821-113">No</span><span class="sxs-lookup"><span data-stu-id="c1821-113">No</span></span><br/> | <span data-ttu-id="c1821-114">要包含之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c1821-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="c1821-115">**宏觀**</span><span class="sxs-lookup"><span data-stu-id="c1821-115">**macro**</span></span><br/> | <span data-ttu-id="c1821-116">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="c1821-116">character\_string</span></span><br/> | <span data-ttu-id="c1821-117">No</span><span class="sxs-lookup"><span data-stu-id="c1821-117">No</span></span><br/> | <span data-ttu-id="c1821-118">要包含的宏名稱。</span><span class="sxs-lookup"><span data-stu-id="c1821-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="c1821-119">子元素</span><span class="sxs-lookup"><span data-stu-id="c1821-119">Child elements</span></span>

<span data-ttu-id="c1821-120">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="c1821-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c1821-121">父元素</span><span class="sxs-lookup"><span data-stu-id="c1821-121">Parent elements</span></span>



| <span data-ttu-id="c1821-122">元素</span><span class="sxs-lookup"><span data-stu-id="c1821-122">Element</span></span>                         | <span data-ttu-id="c1821-123">描述</span><span class="sxs-lookup"><span data-stu-id="c1821-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1821-124">**檔**</span><span class="sxs-lookup"><span data-stu-id="c1821-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="c1821-125">指示程式碼產生器產生檔案並指定輸出檔名稱。</span><span class="sxs-lookup"><span data-stu-id="c1821-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c1821-126">備註</span><span class="sxs-lookup"><span data-stu-id="c1821-126">Remarks</span></span>

<span data-ttu-id="c1821-127">必須指定 **宏** 屬性或 **檔** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c1821-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="c1821-128">請勿同時指定這兩個屬性。</span><span class="sxs-lookup"><span data-stu-id="c1821-128">Do not specify both attributes.</span></span>

<span data-ttu-id="c1821-129">WsdCodeGen 會定義名為 **DoNotModify** 的宏。</span><span class="sxs-lookup"><span data-stu-id="c1821-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="c1821-130">包含此宏時，產生的程式碼會包含高可見度的批註區塊，指示開發人員不修改產生的程式碼。</span><span class="sxs-lookup"><span data-stu-id="c1821-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="c1821-131">範例</span><span class="sxs-lookup"><span data-stu-id="c1821-131">Examples</span></span>

<span data-ttu-id="c1821-132">下列 XML 說明如何包含 **DoNotModify** 宏。</span><span class="sxs-lookup"><span data-stu-id="c1821-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="c1821-133">您可以將此 XML 新增至 XML 設定檔以進行 WsdCodeGen。</span><span class="sxs-lookup"><span data-stu-id="c1821-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="c1821-134">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c1821-134">Element information</span></span>



| <span data-ttu-id="c1821-135">標籤</span><span class="sxs-lookup"><span data-stu-id="c1821-135">Label</span></span> | <span data-ttu-id="c1821-136">值</span><span class="sxs-lookup"><span data-stu-id="c1821-136">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="c1821-137">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="c1821-137">Minimum supported system</span></span><br/> | <span data-ttu-id="c1821-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1821-138">Windows Vista</span></span> |
| <span data-ttu-id="c1821-139">可以是空的</span><span class="sxs-lookup"><span data-stu-id="c1821-139">Can be empty</span></span>                        | <span data-ttu-id="c1821-140">是</span><span class="sxs-lookup"><span data-stu-id="c1821-140">Yes</span></span>           |



 

 




