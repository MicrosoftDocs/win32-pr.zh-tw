---
title: 命令. Comment 屬性
description: 表示命令的批註或批註。
ms.assetid: 4ac5c7d4-9627-4703-bd3c-594d9497ba24
keywords:
- 命令。 Comment 屬性視窗功能區
topic_type:
- apiref
api_name:
- Command.Comment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7df2131234623dd30fc90339634a932eca5bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385118"
---
# <a name="commandcomment-property"></a><span data-ttu-id="89e91-104">命令. Comment 屬性</span><span class="sxs-lookup"><span data-stu-id="89e91-104">Command.Comment property</span></span>

<span data-ttu-id="89e91-105">表示命令的批註或批註。</span><span class="sxs-lookup"><span data-stu-id="89e91-105">Represents a comment, or annotation, for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="89e91-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="89e91-106">Usage</span></span>

``` syntax
<Command.Comment/>
```

## <a name="attributes"></a><span data-ttu-id="89e91-107">屬性</span><span class="sxs-lookup"><span data-stu-id="89e91-107">Attributes</span></span>

<span data-ttu-id="89e91-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="89e91-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="89e91-109">子元素</span><span class="sxs-lookup"><span data-stu-id="89e91-109">Child elements</span></span>

<span data-ttu-id="89e91-110">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="89e91-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="89e91-111">父元素</span><span class="sxs-lookup"><span data-stu-id="89e91-111">Parent elements</span></span>



| <span data-ttu-id="89e91-112">元素</span><span class="sxs-lookup"><span data-stu-id="89e91-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="89e91-113">**命令**</span><span class="sxs-lookup"><span data-stu-id="89e91-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="89e91-114">備註</span><span class="sxs-lookup"><span data-stu-id="89e91-114">Remarks</span></span>

<span data-ttu-id="89e91-115">選擇性。</span><span class="sxs-lookup"><span data-stu-id="89e91-115">Optional.</span></span>

<span data-ttu-id="89e91-116">每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="89e91-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="89e91-117">批註會與功能區標頭檔中的命令定義相關聯，例如 `#define cmdSave 25003 /* Save */` 。</span><span class="sxs-lookup"><span data-stu-id="89e91-117">The comment is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="89e91-118">這個元素包含 *xs： string* 類型的值。</span><span class="sxs-lookup"><span data-stu-id="89e91-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="89e91-119">長度上限是 250 個字元。</span><span class="sxs-lookup"><span data-stu-id="89e91-119">The maximum length is 250 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="89e91-120">範例</span><span class="sxs-lookup"><span data-stu-id="89e91-120">Examples</span></span>

<span data-ttu-id="89e91-121">下列範例示範 [**命令**](windowsribbon-element-command.md) 專案的標記與 **命令。 Comment** 宣告。</span><span class="sxs-lookup"><span data-stu-id="89e91-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Comment** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="89e91-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="89e91-122">Requirements</span></span>



| <span data-ttu-id="89e91-123">需求</span><span class="sxs-lookup"><span data-stu-id="89e91-123">Requirement</span></span> | <span data-ttu-id="89e91-124">值</span><span class="sxs-lookup"><span data-stu-id="89e91-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="89e91-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89e91-125">Minimum supported client</span></span><br/> | <span data-ttu-id="89e91-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89e91-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="89e91-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89e91-127">Minimum supported server</span></span><br/> | <span data-ttu-id="89e91-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89e91-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





