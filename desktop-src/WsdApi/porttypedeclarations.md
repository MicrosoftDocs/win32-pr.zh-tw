---
description: 產生埠類型的 C 常數宣告。
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: portTypeDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e202f1451d93b519bd59ea51f591c37a92957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978890"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="20b4d-103">portTypeDeclarations 元素</span><span class="sxs-lookup"><span data-stu-id="20b4d-103">portTypeDeclarations element</span></span>

<span data-ttu-id="20b4d-104">產生埠類型的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="20b4d-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="20b4d-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="20b4d-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="20b4d-106">屬性</span><span class="sxs-lookup"><span data-stu-id="20b4d-106">Attributes</span></span>

<span data-ttu-id="20b4d-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="20b4d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="20b4d-108">子元素</span><span class="sxs-lookup"><span data-stu-id="20b4d-108">Child elements</span></span>



| <span data-ttu-id="20b4d-109">元素</span><span class="sxs-lookup"><span data-stu-id="20b4d-109">Element</span></span>                                   | <span data-ttu-id="20b4d-110">描述</span><span class="sxs-lookup"><span data-stu-id="20b4d-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20b4d-111">**代號**</span><span class="sxs-lookup"><span data-stu-id="20b4d-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="20b4d-112">指定要在產生的程式碼中用於埠類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="20b4d-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="20b4d-113">根據預設，會從埠類型的限定名稱產生程式碼名稱。</span><span class="sxs-lookup"><span data-stu-id="20b4d-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="20b4d-114">**操作**</span><span class="sxs-lookup"><span data-stu-id="20b4d-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="20b4d-115">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="20b4d-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="20b4d-116">**portType**</span><span class="sxs-lookup"><span data-stu-id="20b4d-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="20b4d-117">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="20b4d-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="20b4d-118">子項目順序</span><span class="sxs-lookup"><span data-stu-id="20b4d-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="20b4d-119">父元素</span><span class="sxs-lookup"><span data-stu-id="20b4d-119">Parent elements</span></span>



| <span data-ttu-id="20b4d-120">元素</span><span class="sxs-lookup"><span data-stu-id="20b4d-120">Element</span></span>                         | <span data-ttu-id="20b4d-121">描述</span><span class="sxs-lookup"><span data-stu-id="20b4d-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="20b4d-122">**檔**</span><span class="sxs-lookup"><span data-stu-id="20b4d-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="20b4d-123">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="20b4d-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="20b4d-124">備註</span><span class="sxs-lookup"><span data-stu-id="20b4d-124">Remarks</span></span>

<span data-ttu-id="20b4d-125">應用程式會參考埠類型宣告，以及大部分產生的程式碼。</span><span class="sxs-lookup"><span data-stu-id="20b4d-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="20b4d-126">此元素用來產生 include 檔案。</span><span class="sxs-lookup"><span data-stu-id="20b4d-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="20b4d-127">項目資訊</span><span class="sxs-lookup"><span data-stu-id="20b4d-127">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="20b4d-128">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="20b4d-128">Minimum supported system</span></span><br/> | <span data-ttu-id="20b4d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20b4d-129">Windows Vista</span></span> |
| <span data-ttu-id="20b4d-130">可以是空的</span><span class="sxs-lookup"><span data-stu-id="20b4d-130">Can be empty</span></span>                        | <span data-ttu-id="20b4d-131">是</span><span class="sxs-lookup"><span data-stu-id="20b4d-131">Yes</span></span>           |



 

 




