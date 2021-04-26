---
description: 產生訊息類型的 C 結構定義。
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: messageStructureDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a116658fc7ce7f985b7b717c7a7b4ce38be4637
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993665"
---
# <a name="messagestructuredefinitions-element"></a><span data-ttu-id="375bb-103">messageStructureDefinitions 元素</span><span class="sxs-lookup"><span data-stu-id="375bb-103">messageStructureDefinitions element</span></span>

<span data-ttu-id="375bb-104">產生訊息類型的 C 結構定義。</span><span class="sxs-lookup"><span data-stu-id="375bb-104">Generates C structure definitions for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="375bb-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="375bb-105">Usage</span></span>

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="375bb-106">屬性</span><span class="sxs-lookup"><span data-stu-id="375bb-106">Attributes</span></span>

<span data-ttu-id="375bb-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="375bb-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="375bb-108">子元素</span><span class="sxs-lookup"><span data-stu-id="375bb-108">Child elements</span></span>



| <span data-ttu-id="375bb-109">元素</span><span class="sxs-lookup"><span data-stu-id="375bb-109">Element</span></span>                                   | <span data-ttu-id="375bb-110">描述</span><span class="sxs-lookup"><span data-stu-id="375bb-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="375bb-111">**操作**</span><span class="sxs-lookup"><span data-stu-id="375bb-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="375bb-112">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="375bb-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="375bb-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="375bb-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="375bb-114">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="375bb-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="375bb-115">子項目順序</span><span class="sxs-lookup"><span data-stu-id="375bb-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="375bb-116">父元素</span><span class="sxs-lookup"><span data-stu-id="375bb-116">Parent elements</span></span>



| <span data-ttu-id="375bb-117">元素</span><span class="sxs-lookup"><span data-stu-id="375bb-117">Element</span></span>                         | <span data-ttu-id="375bb-118">描述</span><span class="sxs-lookup"><span data-stu-id="375bb-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="375bb-119">**檔**</span><span class="sxs-lookup"><span data-stu-id="375bb-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="375bb-120">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="375bb-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="375bb-121">備註</span><span class="sxs-lookup"><span data-stu-id="375bb-121">Remarks</span></span>

<span data-ttu-id="375bb-122">訊息結構會由產生的 proxy 和存根程式碼所參考。</span><span class="sxs-lookup"><span data-stu-id="375bb-122">Message structures are referenced by generated proxy and stub code.</span></span> <span data-ttu-id="375bb-123">此元素用來產生 include 檔案。</span><span class="sxs-lookup"><span data-stu-id="375bb-123">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="375bb-124">項目資訊</span><span class="sxs-lookup"><span data-stu-id="375bb-124">Element information</span></span>



| <span data-ttu-id="375bb-125">標籤</span><span class="sxs-lookup"><span data-stu-id="375bb-125">Label</span></span> | <span data-ttu-id="375bb-126">值</span><span class="sxs-lookup"><span data-stu-id="375bb-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="375bb-127">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="375bb-127">Minimum supported system</span></span><br/> | <span data-ttu-id="375bb-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="375bb-128">Windows Vista</span></span> |
| <span data-ttu-id="375bb-129">可以是空的</span><span class="sxs-lookup"><span data-stu-id="375bb-129">Can be empty</span></span>                        | <span data-ttu-id="375bb-130">是</span><span class="sxs-lookup"><span data-stu-id="375bb-130">Yes</span></span>           |



 

 




