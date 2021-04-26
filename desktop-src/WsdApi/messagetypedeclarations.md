---
description: 針對訊息類型產生 XML 架構資料表的 C 常數宣告。
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: messageTypeDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696cd6d30e6a791f68c152e0d0c5d0b1a7300769
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998725"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="ea15a-103">messageTypeDeclarations 元素</span><span class="sxs-lookup"><span data-stu-id="ea15a-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="ea15a-104">針對訊息類型產生 XML 架構資料表的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="ea15a-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="ea15a-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="ea15a-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="ea15a-106">屬性</span><span class="sxs-lookup"><span data-stu-id="ea15a-106">Attributes</span></span>

<span data-ttu-id="ea15a-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ea15a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ea15a-108">子元素</span><span class="sxs-lookup"><span data-stu-id="ea15a-108">Child elements</span></span>



| <span data-ttu-id="ea15a-109">元素</span><span class="sxs-lookup"><span data-stu-id="ea15a-109">Element</span></span>                                   | <span data-ttu-id="ea15a-110">描述</span><span class="sxs-lookup"><span data-stu-id="ea15a-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ea15a-111">**操作**</span><span class="sxs-lookup"><span data-stu-id="ea15a-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="ea15a-112">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="ea15a-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="ea15a-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="ea15a-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="ea15a-114">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="ea15a-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="ea15a-115">子項目順序</span><span class="sxs-lookup"><span data-stu-id="ea15a-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="ea15a-116">父元素</span><span class="sxs-lookup"><span data-stu-id="ea15a-116">Parent elements</span></span>



| <span data-ttu-id="ea15a-117">元素</span><span class="sxs-lookup"><span data-stu-id="ea15a-117">Element</span></span>                         | <span data-ttu-id="ea15a-118">描述</span><span class="sxs-lookup"><span data-stu-id="ea15a-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ea15a-119">**檔**</span><span class="sxs-lookup"><span data-stu-id="ea15a-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="ea15a-120">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="ea15a-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ea15a-121">備註</span><span class="sxs-lookup"><span data-stu-id="ea15a-121">Remarks</span></span>

<span data-ttu-id="ea15a-122">架構資料表是由埠類型定義所參考。</span><span class="sxs-lookup"><span data-stu-id="ea15a-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="ea15a-123">因此，這個元素通常會在 [**portTypeDefinitions**](porttypedefinitions.md) 元素之前使用。</span><span class="sxs-lookup"><span data-stu-id="ea15a-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="ea15a-124">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ea15a-124">Element information</span></span>



| <span data-ttu-id="ea15a-125">標籤</span><span class="sxs-lookup"><span data-stu-id="ea15a-125">Label</span></span> | <span data-ttu-id="ea15a-126">值</span><span class="sxs-lookup"><span data-stu-id="ea15a-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="ea15a-127">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="ea15a-127">Minimum supported system</span></span><br/> | <span data-ttu-id="ea15a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea15a-128">Windows Vista</span></span> |
| <span data-ttu-id="ea15a-129">可以是空的</span><span class="sxs-lookup"><span data-stu-id="ea15a-129">Can be empty</span></span>                        | <span data-ttu-id="ea15a-130">是</span><span class="sxs-lookup"><span data-stu-id="ea15a-130">Yes</span></span>           |



 

 




