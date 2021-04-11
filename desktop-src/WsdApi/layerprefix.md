---
description: 定義要在產生的程式碼中使用的前置詞，以確保產生的符號唯一性。
ms.assetid: 50cb443a-15ae-4f8f-b5f7-b8708810a6c3
title: layerPrefix 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b712edee4b33c7158280b9d310624371fd58688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115024"
---
# <a name="layerprefix-element"></a><span data-ttu-id="6ee7d-103">layerPrefix 元素</span><span class="sxs-lookup"><span data-stu-id="6ee7d-103">layerPrefix element</span></span>

<span data-ttu-id="6ee7d-104">定義要在產生的程式碼中使用的前置詞，以確保產生的符號唯一性。</span><span class="sxs-lookup"><span data-stu-id="6ee7d-104">Defines the prefix to use in the generated code to assure uniqueness of generated symbols.</span></span>

## <a name="usage"></a><span data-ttu-id="6ee7d-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="6ee7d-105">Usage</span></span>

``` syntax
<layerPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="6ee7d-106">屬性</span><span class="sxs-lookup"><span data-stu-id="6ee7d-106">Attributes</span></span>

<span data-ttu-id="6ee7d-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="6ee7d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6ee7d-108">子元素</span><span class="sxs-lookup"><span data-stu-id="6ee7d-108">Child elements</span></span>

<span data-ttu-id="6ee7d-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="6ee7d-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6ee7d-110">父元素</span><span class="sxs-lookup"><span data-stu-id="6ee7d-110">Parent elements</span></span>



| <span data-ttu-id="6ee7d-111">元素</span><span class="sxs-lookup"><span data-stu-id="6ee7d-111">Element</span></span>                                     | <span data-ttu-id="6ee7d-112">描述</span><span class="sxs-lookup"><span data-stu-id="6ee7d-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ee7d-113">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="6ee7d-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="6ee7d-114">WSDAPI 程式碼產生器 XML 腳本檔的根項目。</span><span class="sxs-lookup"><span data-stu-id="6ee7d-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6ee7d-115">備註</span><span class="sxs-lookup"><span data-stu-id="6ee7d-115">Remarks</span></span>

<span data-ttu-id="6ee7d-116">每個程式碼產生器腳本都應該為所建立的模組定義唯一的前置詞字串。</span><span class="sxs-lookup"><span data-stu-id="6ee7d-116">Each code generator script should define a unique prefix string for the modules created.</span></span> <span data-ttu-id="6ee7d-117">例如，圖片框架腳本會使用 "PFDEMO" 的前置詞。</span><span class="sxs-lookup"><span data-stu-id="6ee7d-117">For example, the Picture Frame scripts use a prefix of "PFDEMO".</span></span>

<span data-ttu-id="6ee7d-118">WSDAPI 使用 "WSD" 前置詞。</span><span class="sxs-lookup"><span data-stu-id="6ee7d-118">WSDAPI uses the prefix "WSD".</span></span>

## <a name="element-information"></a><span data-ttu-id="6ee7d-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6ee7d-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="6ee7d-120">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="6ee7d-120">Minimum supported system</span></span><br/> | <span data-ttu-id="6ee7d-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ee7d-121">Windows Vista</span></span> |
| <span data-ttu-id="6ee7d-122">可以是空的</span><span class="sxs-lookup"><span data-stu-id="6ee7d-122">Can be empty</span></span>                        | <span data-ttu-id="6ee7d-123">是</span><span class="sxs-lookup"><span data-stu-id="6ee7d-123">Yes</span></span>           |



 

 




