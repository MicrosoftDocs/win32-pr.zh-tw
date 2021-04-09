---
title: SizeDefinitions 屬性
description: 代表功能區控制項之自訂版面配置範本的容器。
ms.assetid: 1f5fcffc-7f2e-4763-b0a7-4e8f46534da8
keywords:
- SizeDefinitions 屬性視窗功能區
topic_type:
- apiref
api_name:
- Ribbon.SizeDefinitions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8ffe5a3339b0f32e493a1f7ddc33789526695e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024678"
---
# <a name="ribbonsizedefinitions-property"></a><span data-ttu-id="7ed11-104">SizeDefinitions 屬性</span><span class="sxs-lookup"><span data-stu-id="7ed11-104">Ribbon.SizeDefinitions property</span></span>

<span data-ttu-id="7ed11-105">代表功能區控制項之自訂版面配置範本的容器。</span><span class="sxs-lookup"><span data-stu-id="7ed11-105">Represents a container for custom layout templates of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="7ed11-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="7ed11-106">Usage</span></span>

``` syntax
<Ribbon.SizeDefinitions>
  child elements
</Ribbon.SizeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="7ed11-107">屬性</span><span class="sxs-lookup"><span data-stu-id="7ed11-107">Attributes</span></span>

<span data-ttu-id="7ed11-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="7ed11-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7ed11-109">子元素</span><span class="sxs-lookup"><span data-stu-id="7ed11-109">Child elements</span></span>



| <span data-ttu-id="7ed11-110">元素</span><span class="sxs-lookup"><span data-stu-id="7ed11-110">Element</span></span>                                                                   | <span data-ttu-id="7ed11-111">描述</span><span class="sxs-lookup"><span data-stu-id="7ed11-111">Description</span></span>                                        |
|---------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="7ed11-112">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="7ed11-112">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> | <span data-ttu-id="7ed11-113">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="7ed11-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="7ed11-114">父元素</span><span class="sxs-lookup"><span data-stu-id="7ed11-114">Parent elements</span></span>



| <span data-ttu-id="7ed11-115">元素</span><span class="sxs-lookup"><span data-stu-id="7ed11-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="7ed11-116">**功能區**</span><span class="sxs-lookup"><span data-stu-id="7ed11-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7ed11-117">備註</span><span class="sxs-lookup"><span data-stu-id="7ed11-117">Remarks</span></span>

<span data-ttu-id="7ed11-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7ed11-118">Optional.</span></span>

<span data-ttu-id="7ed11-119">每個 [**功能區**](windowsribbon-element-ribbon.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="7ed11-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7ed11-120">範例</span><span class="sxs-lookup"><span data-stu-id="7ed11-120">Examples</span></span>

<span data-ttu-id="7ed11-121">下列程式碼範例說明基本的自訂範本。</span><span class="sxs-lookup"><span data-stu-id="7ed11-121">The following code example illustrates a basic custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



## <a name="requirements"></a><span data-ttu-id="7ed11-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ed11-122">Requirements</span></span>



| <span data-ttu-id="7ed11-123">需求</span><span class="sxs-lookup"><span data-stu-id="7ed11-123">Requirement</span></span> | <span data-ttu-id="7ed11-124">值</span><span class="sxs-lookup"><span data-stu-id="7ed11-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7ed11-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ed11-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7ed11-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ed11-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7ed11-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ed11-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7ed11-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ed11-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ed11-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ed11-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed11-130">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="7ed11-130">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





