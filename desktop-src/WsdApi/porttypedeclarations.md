---
description: 產生埠類型的 C 常數宣告。
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: portTypeDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19780d4a48c95cd47872b0428b368e6b7e99887
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996555"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="8e076-103">portTypeDeclarations 元素</span><span class="sxs-lookup"><span data-stu-id="8e076-103">portTypeDeclarations element</span></span>

<span data-ttu-id="8e076-104">產生埠類型的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="8e076-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="8e076-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="8e076-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="8e076-106">屬性</span><span class="sxs-lookup"><span data-stu-id="8e076-106">Attributes</span></span>

<span data-ttu-id="8e076-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="8e076-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8e076-108">子元素</span><span class="sxs-lookup"><span data-stu-id="8e076-108">Child elements</span></span>



| <span data-ttu-id="8e076-109">元素</span><span class="sxs-lookup"><span data-stu-id="8e076-109">Element</span></span>                                   | <span data-ttu-id="8e076-110">描述</span><span class="sxs-lookup"><span data-stu-id="8e076-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e076-111">**代號**</span><span class="sxs-lookup"><span data-stu-id="8e076-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="8e076-112">指定要在產生的程式碼中用於埠類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e076-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="8e076-113">根據預設，會從埠類型的限定名稱產生程式碼名稱。</span><span class="sxs-lookup"><span data-stu-id="8e076-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="8e076-114">**操作**</span><span class="sxs-lookup"><span data-stu-id="8e076-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="8e076-115">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="8e076-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="8e076-116">**portType**</span><span class="sxs-lookup"><span data-stu-id="8e076-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="8e076-117">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="8e076-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="8e076-118">子項目順序</span><span class="sxs-lookup"><span data-stu-id="8e076-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="8e076-119">父元素</span><span class="sxs-lookup"><span data-stu-id="8e076-119">Parent elements</span></span>



| <span data-ttu-id="8e076-120">元素</span><span class="sxs-lookup"><span data-stu-id="8e076-120">Element</span></span>                         | <span data-ttu-id="8e076-121">描述</span><span class="sxs-lookup"><span data-stu-id="8e076-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8e076-122">**檔**</span><span class="sxs-lookup"><span data-stu-id="8e076-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="8e076-123">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="8e076-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8e076-124">備註</span><span class="sxs-lookup"><span data-stu-id="8e076-124">Remarks</span></span>

<span data-ttu-id="8e076-125">應用程式會參考埠類型宣告，以及大部分產生的程式碼。</span><span class="sxs-lookup"><span data-stu-id="8e076-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="8e076-126">此元素用來產生 include 檔案。</span><span class="sxs-lookup"><span data-stu-id="8e076-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="8e076-127">項目資訊</span><span class="sxs-lookup"><span data-stu-id="8e076-127">Element information</span></span>



| <span data-ttu-id="8e076-128">標籤</span><span class="sxs-lookup"><span data-stu-id="8e076-128">Label</span></span> | <span data-ttu-id="8e076-129">值</span><span class="sxs-lookup"><span data-stu-id="8e076-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8e076-130">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="8e076-130">Minimum supported system</span></span><br/> | <span data-ttu-id="8e076-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e076-131">Windows Vista</span></span> |
| <span data-ttu-id="8e076-132">可以是空的</span><span class="sxs-lookup"><span data-stu-id="8e076-132">Can be empty</span></span>                        | <span data-ttu-id="8e076-133">是</span><span class="sxs-lookup"><span data-stu-id="8e076-133">Yes</span></span>           |



 

 




