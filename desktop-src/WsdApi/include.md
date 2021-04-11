---
description: 在產生的輸出中包含宏或檔案的內容。
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: 包含元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f22cfde339ca218d4cd10525bbca3e57b8d836f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027167"
---
# <a name="include-element"></a><span data-ttu-id="f3b95-103">包含元素</span><span class="sxs-lookup"><span data-stu-id="f3b95-103">include element</span></span>

<span data-ttu-id="f3b95-104">在產生的輸出中包含宏或檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="f3b95-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="f3b95-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="f3b95-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="f3b95-106">屬性</span><span class="sxs-lookup"><span data-stu-id="f3b95-106">Attributes</span></span>



| <span data-ttu-id="f3b95-107">屬性</span><span class="sxs-lookup"><span data-stu-id="f3b95-107">Attribute</span></span>            | <span data-ttu-id="f3b95-108">類型</span><span class="sxs-lookup"><span data-stu-id="f3b95-108">Type</span></span>                         | <span data-ttu-id="f3b95-109">必要</span><span class="sxs-lookup"><span data-stu-id="f3b95-109">Required</span></span>      | <span data-ttu-id="f3b95-110">描述</span><span class="sxs-lookup"><span data-stu-id="f3b95-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="f3b95-111">**file**</span><span class="sxs-lookup"><span data-stu-id="f3b95-111">**file**</span></span><br/>  | <span data-ttu-id="f3b95-112">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="f3b95-112">character\_string</span></span><br/> | <span data-ttu-id="f3b95-113">No</span><span class="sxs-lookup"><span data-stu-id="f3b95-113">No</span></span><br/> | <span data-ttu-id="f3b95-114">要包含之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="f3b95-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="f3b95-115">**宏觀**</span><span class="sxs-lookup"><span data-stu-id="f3b95-115">**macro**</span></span><br/> | <span data-ttu-id="f3b95-116">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="f3b95-116">character\_string</span></span><br/> | <span data-ttu-id="f3b95-117">No</span><span class="sxs-lookup"><span data-stu-id="f3b95-117">No</span></span><br/> | <span data-ttu-id="f3b95-118">要包含的宏名稱。</span><span class="sxs-lookup"><span data-stu-id="f3b95-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="f3b95-119">子元素</span><span class="sxs-lookup"><span data-stu-id="f3b95-119">Child elements</span></span>

<span data-ttu-id="f3b95-120">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="f3b95-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f3b95-121">父元素</span><span class="sxs-lookup"><span data-stu-id="f3b95-121">Parent elements</span></span>



| <span data-ttu-id="f3b95-122">元素</span><span class="sxs-lookup"><span data-stu-id="f3b95-122">Element</span></span>                         | <span data-ttu-id="f3b95-123">描述</span><span class="sxs-lookup"><span data-stu-id="f3b95-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3b95-124">**檔**</span><span class="sxs-lookup"><span data-stu-id="f3b95-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="f3b95-125">指示程式碼產生器產生檔案並指定輸出檔名稱。</span><span class="sxs-lookup"><span data-stu-id="f3b95-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f3b95-126">備註</span><span class="sxs-lookup"><span data-stu-id="f3b95-126">Remarks</span></span>

<span data-ttu-id="f3b95-127">必須指定 **宏** 屬性或 **檔** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f3b95-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="f3b95-128">請勿同時指定這兩個屬性。</span><span class="sxs-lookup"><span data-stu-id="f3b95-128">Do not specify both attributes.</span></span>

<span data-ttu-id="f3b95-129">WsdCodeGen 會定義名為 **DoNotModify** 的宏。</span><span class="sxs-lookup"><span data-stu-id="f3b95-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="f3b95-130">包含此宏時，產生的程式碼會包含高可見度的批註區塊，指示開發人員不修改產生的程式碼。</span><span class="sxs-lookup"><span data-stu-id="f3b95-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="f3b95-131">範例</span><span class="sxs-lookup"><span data-stu-id="f3b95-131">Examples</span></span>

<span data-ttu-id="f3b95-132">下列 XML 說明如何包含 **DoNotModify** 宏。</span><span class="sxs-lookup"><span data-stu-id="f3b95-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="f3b95-133">您可以將此 XML 新增至 XML 設定檔以進行 WsdCodeGen。</span><span class="sxs-lookup"><span data-stu-id="f3b95-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="f3b95-134">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f3b95-134">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f3b95-135">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="f3b95-135">Minimum supported system</span></span><br/> | <span data-ttu-id="f3b95-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3b95-136">Windows Vista</span></span> |
| <span data-ttu-id="f3b95-137">可以是空的</span><span class="sxs-lookup"><span data-stu-id="f3b95-137">Can be empty</span></span>                        | <span data-ttu-id="f3b95-138">是</span><span class="sxs-lookup"><span data-stu-id="f3b95-138">Yes</span></span>           |



 

 




