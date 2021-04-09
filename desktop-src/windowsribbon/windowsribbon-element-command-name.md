---
title: Command.Name 屬性
description: 表示命令的名稱。
ms.assetid: 36fb0b93-143f-4706-8c32-e6c818cce16f
keywords:
- Command.Name 屬性視窗功能區
topic_type:
- apiref
api_name:
- Command.Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d93b830e29ca271052a4693b00ba64eee94309f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025390"
---
# <a name="commandname-property"></a><span data-ttu-id="a5af0-104">Command.Name 屬性</span><span class="sxs-lookup"><span data-stu-id="a5af0-104">Command.Name property</span></span>

<span data-ttu-id="a5af0-105">表示命令的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5af0-105">Represents the name of a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="a5af0-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="a5af0-106">Usage</span></span>

``` syntax
<Command.Name/>
```

## <a name="attributes"></a><span data-ttu-id="a5af0-107">屬性</span><span class="sxs-lookup"><span data-stu-id="a5af0-107">Attributes</span></span>

<span data-ttu-id="a5af0-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="a5af0-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a5af0-109">子元素</span><span class="sxs-lookup"><span data-stu-id="a5af0-109">Child elements</span></span>

<span data-ttu-id="a5af0-110">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="a5af0-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a5af0-111">父元素</span><span class="sxs-lookup"><span data-stu-id="a5af0-111">Parent elements</span></span>



| <span data-ttu-id="a5af0-112">元素</span><span class="sxs-lookup"><span data-stu-id="a5af0-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="a5af0-113">**命令**</span><span class="sxs-lookup"><span data-stu-id="a5af0-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a5af0-114">備註</span><span class="sxs-lookup"><span data-stu-id="a5af0-114">Remarks</span></span>

<span data-ttu-id="a5af0-115">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a5af0-115">Optional.</span></span>

<span data-ttu-id="a5af0-116">每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="a5af0-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="a5af0-117">標記中會參考 **Command.Name** ，以透過控制項的 *CommandName* 屬性將命令與控制項產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a5af0-117">**Command.Name** is referenced in markup to associate a Command with a control through the *CommandName* attribute of the control.</span></span>

<span data-ttu-id="a5af0-118">這個元素包含 *xs： string* 類型的值。</span><span class="sxs-lookup"><span data-stu-id="a5af0-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="a5af0-119">此值受限於包含字母或底線的字串，後面接著字母、數位和底線的任何序列。</span><span class="sxs-lookup"><span data-stu-id="a5af0-119">The value is constrained to a string that consists of a letter or underscore followed by any sequence of letters, digits, and underscores.</span></span>

<span data-ttu-id="a5af0-120">長度上限為100個字元。</span><span class="sxs-lookup"><span data-stu-id="a5af0-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="a5af0-121">範例</span><span class="sxs-lookup"><span data-stu-id="a5af0-121">Examples</span></span>

<span data-ttu-id="a5af0-122">下列範例示範具有 **Command.Name** 宣告之 [**Command**](windowsribbon-element-command.md)元素的標記。</span><span class="sxs-lookup"><span data-stu-id="a5af0-122">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Name** declaration.</span></span>


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="a5af0-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5af0-123">Requirements</span></span>



| <span data-ttu-id="a5af0-124">需求</span><span class="sxs-lookup"><span data-stu-id="a5af0-124">Requirement</span></span> | <span data-ttu-id="a5af0-125">值</span><span class="sxs-lookup"><span data-stu-id="a5af0-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a5af0-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5af0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a5af0-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5af0-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a5af0-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5af0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a5af0-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5af0-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





