---
description: 定義 include 元素要重複使用的 text 或 CDATA。
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: 宏元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8759d4afb61883b8bf41472f276882643cfa552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193054"
---
# <a name="macro-element"></a><span data-ttu-id="affb7-103">宏元素</span><span class="sxs-lookup"><span data-stu-id="affb7-103">macro element</span></span>

<span data-ttu-id="affb7-104">定義 [**include**](include.md) 元素要重複使用的 TEXT 或 CDATA。</span><span class="sxs-lookup"><span data-stu-id="affb7-104">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span>

## <a name="usage"></a><span data-ttu-id="affb7-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="affb7-105">Usage</span></span>

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="affb7-106">屬性</span><span class="sxs-lookup"><span data-stu-id="affb7-106">Attributes</span></span>



| <span data-ttu-id="affb7-107">屬性</span><span class="sxs-lookup"><span data-stu-id="affb7-107">Attribute</span></span>           | <span data-ttu-id="affb7-108">類型</span><span class="sxs-lookup"><span data-stu-id="affb7-108">Type</span></span>                         | <span data-ttu-id="affb7-109">必要</span><span class="sxs-lookup"><span data-stu-id="affb7-109">Required</span></span>       | <span data-ttu-id="affb7-110">描述</span><span class="sxs-lookup"><span data-stu-id="affb7-110">Description</span></span>                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| <span data-ttu-id="affb7-111">**name**</span><span class="sxs-lookup"><span data-stu-id="affb7-111">**name**</span></span><br/> | <span data-ttu-id="affb7-112">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="affb7-112">character\_string</span></span><br/> | <span data-ttu-id="affb7-113">Yes</span><span class="sxs-lookup"><span data-stu-id="affb7-113">Yes</span></span><br/> | <span data-ttu-id="affb7-114">宏的名稱。</span><span class="sxs-lookup"><span data-stu-id="affb7-114">The name of the macro.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="affb7-115">子元素</span><span class="sxs-lookup"><span data-stu-id="affb7-115">Child elements</span></span>

<span data-ttu-id="affb7-116">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="affb7-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="affb7-117">父元素</span><span class="sxs-lookup"><span data-stu-id="affb7-117">Parent elements</span></span>



| <span data-ttu-id="affb7-118">元素</span><span class="sxs-lookup"><span data-stu-id="affb7-118">Element</span></span>                                     | <span data-ttu-id="affb7-119">描述</span><span class="sxs-lookup"><span data-stu-id="affb7-119">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="affb7-120">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="affb7-120">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="affb7-121">WSDAPI 程式碼產生器 XML 腳本檔的根項目。</span><span class="sxs-lookup"><span data-stu-id="affb7-121">The root element of a WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="affb7-122">備註</span><span class="sxs-lookup"><span data-stu-id="affb7-122">Remarks</span></span>

<span data-ttu-id="affb7-123">WsdCodeGen 會定義名為 **DoNotModify** 的宏。</span><span class="sxs-lookup"><span data-stu-id="affb7-123">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="affb7-124">包含此宏時，產生的程式碼會包含高可見度的批註區塊，指示開發人員不修改產生的程式碼。</span><span class="sxs-lookup"><span data-stu-id="affb7-124">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

<span data-ttu-id="affb7-125">下列 XML 說明如何包含 **DoNotModify** 宏。</span><span class="sxs-lookup"><span data-stu-id="affb7-125">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="affb7-126">您可以將此 XML 新增至 XML 設定檔以進行 WsdCodeGen。</span><span class="sxs-lookup"><span data-stu-id="affb7-126">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="affb7-127">項目資訊</span><span class="sxs-lookup"><span data-stu-id="affb7-127">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="affb7-128">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="affb7-128">Minimum supported system</span></span><br/> | <span data-ttu-id="affb7-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="affb7-129">Windows Vista</span></span> |
| <span data-ttu-id="affb7-130">可以是空的</span><span class="sxs-lookup"><span data-stu-id="affb7-130">Can be empty</span></span>                        | <span data-ttu-id="affb7-131">是</span><span class="sxs-lookup"><span data-stu-id="affb7-131">Yes</span></span>           |



 

 




