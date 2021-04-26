---
description: 定義要產生的程式碼層數目。
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: layerNumber 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c33ee4468ab81f030bfd8b49dfe104bbe76248
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995485"
---
# <a name="layernumber-element"></a><span data-ttu-id="6060a-103">layerNumber 元素</span><span class="sxs-lookup"><span data-stu-id="6060a-103">layerNumber element</span></span>

<span data-ttu-id="6060a-104">定義要產生的程式碼層數目。</span><span class="sxs-lookup"><span data-stu-id="6060a-104">Defines the number of the code layer to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="6060a-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="6060a-105">Usage</span></span>

``` syntax
<layerNumber/>
```

## <a name="attributes"></a><span data-ttu-id="6060a-106">屬性</span><span class="sxs-lookup"><span data-stu-id="6060a-106">Attributes</span></span>

<span data-ttu-id="6060a-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="6060a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6060a-108">子元素</span><span class="sxs-lookup"><span data-stu-id="6060a-108">Child elements</span></span>

<span data-ttu-id="6060a-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="6060a-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6060a-110">父元素</span><span class="sxs-lookup"><span data-stu-id="6060a-110">Parent elements</span></span>



| <span data-ttu-id="6060a-111">元素</span><span class="sxs-lookup"><span data-stu-id="6060a-111">Element</span></span>                                     | <span data-ttu-id="6060a-112">描述</span><span class="sxs-lookup"><span data-stu-id="6060a-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="6060a-113">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="6060a-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="6060a-114">WSDAPI 程式碼產生器 XML 腳本檔的根項目。</span><span class="sxs-lookup"><span data-stu-id="6060a-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6060a-115">備註</span><span class="sxs-lookup"><span data-stu-id="6060a-115">Remarks</span></span>

<span data-ttu-id="6060a-116">在執行時間資料表中，會使用圖層編號來區分另一層程式碼。</span><span class="sxs-lookup"><span data-stu-id="6060a-116">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="6060a-117">WSDAPI 本身會使用產生的程式碼，其層號為0。</span><span class="sxs-lookup"><span data-stu-id="6060a-117">WSDAPI itself uses generated code that has a layer number of 0.</span></span>

<span data-ttu-id="6060a-118">通常，這個值會是1，表示產生的程式碼會分層在 WSDAPI 的上方，而不是其他圖層。</span><span class="sxs-lookup"><span data-stu-id="6060a-118">Typically, this value will be 1, indicating that the generated code is layered on top of WSDAPI and no other layer.</span></span> <span data-ttu-id="6060a-119">在某些情況下，可能會使用較高的數位。</span><span class="sxs-lookup"><span data-stu-id="6060a-119">In some cases, higher numbers may be used.</span></span> <span data-ttu-id="6060a-120">例如，如果有一家公司產生裝置類別的程式碼， (編號層 1) ，則特定硬體廠商可能會想要新增額外的圖層編號第2層。</span><span class="sxs-lookup"><span data-stu-id="6060a-120">For example, if one company produces code for a device class (numbered layer 1), a particular hardware vendor may want to add an additional layer numbered layer 2.</span></span>

<span data-ttu-id="6060a-121">合法值（除了 WSDAPI 本身的情況以外）會大於0且小於16。</span><span class="sxs-lookup"><span data-stu-id="6060a-121">Legal values, except in the case of WSDAPI itself are greater than 0 and less than 16.</span></span>

## <a name="element-information"></a><span data-ttu-id="6060a-122">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6060a-122">Element information</span></span>



| <span data-ttu-id="6060a-123">標籤</span><span class="sxs-lookup"><span data-stu-id="6060a-123">Label</span></span> | <span data-ttu-id="6060a-124">值</span><span class="sxs-lookup"><span data-stu-id="6060a-124">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="6060a-125">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="6060a-125">Minimum supported system</span></span><br/> | <span data-ttu-id="6060a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6060a-126">Windows Vista</span></span> |
| <span data-ttu-id="6060a-127">可以是空的</span><span class="sxs-lookup"><span data-stu-id="6060a-127">Can be empty</span></span>                        | <span data-ttu-id="6060a-128">是</span><span class="sxs-lookup"><span data-stu-id="6060a-128">Yes</span></span>           |



 

 




