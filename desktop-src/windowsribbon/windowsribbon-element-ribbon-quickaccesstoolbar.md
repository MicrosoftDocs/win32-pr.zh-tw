---
title: QuickAccessToolbar 屬性
description: 代表快速存取工具列 (QAT) 的容器。
ms.assetid: 8a873a48-4f8b-439d-acad-7da2081fbf40
keywords:
- QuickAccessToolbar 屬性視窗功能區
topic_type:
- apiref
api_name:
- Ribbon.QuickAccessToolbar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0e09b220bd60b60ccbb8ee05c2da9c4317ba78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383938"
---
# <a name="ribbonquickaccesstoolbar-property"></a><span data-ttu-id="4a5a1-104">QuickAccessToolbar 屬性</span><span class="sxs-lookup"><span data-stu-id="4a5a1-104">Ribbon.QuickAccessToolbar property</span></span>

<span data-ttu-id="4a5a1-105">代表快速存取工具列 (QAT) 的容器。</span><span class="sxs-lookup"><span data-stu-id="4a5a1-105">Represents a container for the Quick Access Toolbar (QAT).</span></span>

## <a name="usage"></a><span data-ttu-id="4a5a1-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="4a5a1-106">Usage</span></span>

``` syntax
<Ribbon.QuickAccessToolbar>
  child elements
</Ribbon.QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="4a5a1-107">屬性</span><span class="sxs-lookup"><span data-stu-id="4a5a1-107">Attributes</span></span>

<span data-ttu-id="4a5a1-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="4a5a1-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4a5a1-109">子元素</span><span class="sxs-lookup"><span data-stu-id="4a5a1-109">Child elements</span></span>



| <span data-ttu-id="4a5a1-110">元素</span><span class="sxs-lookup"><span data-stu-id="4a5a1-110">Element</span></span>                                                                           | <span data-ttu-id="4a5a1-111">描述</span><span class="sxs-lookup"><span data-stu-id="4a5a1-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="4a5a1-112">**QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="4a5a1-112">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md)<br/> | <span data-ttu-id="4a5a1-113">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="4a5a1-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="4a5a1-114">父元素</span><span class="sxs-lookup"><span data-stu-id="4a5a1-114">Parent elements</span></span>



| <span data-ttu-id="4a5a1-115">元素</span><span class="sxs-lookup"><span data-stu-id="4a5a1-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="4a5a1-116">**功能區**</span><span class="sxs-lookup"><span data-stu-id="4a5a1-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4a5a1-117">備註</span><span class="sxs-lookup"><span data-stu-id="4a5a1-117">Remarks</span></span>

<span data-ttu-id="4a5a1-118">必要。</span><span class="sxs-lookup"><span data-stu-id="4a5a1-118">Required.</span></span>

<span data-ttu-id="4a5a1-119">每個 [**功能區**](windowsribbon-element-ribbon.md)可能會出現一次或多次。</span><span class="sxs-lookup"><span data-stu-id="4a5a1-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4a5a1-120">範例</span><span class="sxs-lookup"><span data-stu-id="4a5a1-120">Examples</span></span>

<span data-ttu-id="4a5a1-121">下列範例示範 **QuickAccessToolbar** 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="4a5a1-121">The following example demonstrates the basic markup for the **Ribbon.QuickAccessToolbar** element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a><span data-ttu-id="4a5a1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a5a1-122">Requirements</span></span>



| <span data-ttu-id="4a5a1-123">需求</span><span class="sxs-lookup"><span data-stu-id="4a5a1-123">Requirement</span></span> | <span data-ttu-id="4a5a1-124">值</span><span class="sxs-lookup"><span data-stu-id="4a5a1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4a5a1-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a5a1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4a5a1-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a5a1-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4a5a1-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a5a1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4a5a1-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a5a1-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





