---
title: Command.Id 屬性
description: 表示命令的唯一識別碼。
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Command.Id 屬性視窗功能區
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e259e5fd74e3037afde3d4c001000b5a17a9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466589"
---
# <a name="commandid-property"></a><span data-ttu-id="c5a8c-104">Command.Id 屬性</span><span class="sxs-lookup"><span data-stu-id="c5a8c-104">Command.Id property</span></span>

<span data-ttu-id="c5a8c-105">表示命令的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5a8c-105">Represents a unique ID for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="c5a8c-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="c5a8c-106">Usage</span></span>

``` syntax
<Command.Id/>
```

## <a name="attributes"></a><span data-ttu-id="c5a8c-107">屬性</span><span class="sxs-lookup"><span data-stu-id="c5a8c-107">Attributes</span></span>

<span data-ttu-id="c5a8c-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="c5a8c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c5a8c-109">子元素</span><span class="sxs-lookup"><span data-stu-id="c5a8c-109">Child elements</span></span>

<span data-ttu-id="c5a8c-110">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="c5a8c-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c5a8c-111">父元素</span><span class="sxs-lookup"><span data-stu-id="c5a8c-111">Parent elements</span></span>



| <span data-ttu-id="c5a8c-112">元素</span><span class="sxs-lookup"><span data-stu-id="c5a8c-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="c5a8c-113">**命令**</span><span class="sxs-lookup"><span data-stu-id="c5a8c-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c5a8c-114">備註</span><span class="sxs-lookup"><span data-stu-id="c5a8c-114">Remarks</span></span>

<span data-ttu-id="c5a8c-115">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c5a8c-115">Optional.</span></span>

<span data-ttu-id="c5a8c-116">每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="c5a8c-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="c5a8c-117">此識別碼與功能區標頭檔中的命令定義相關聯，例如 `#define cmdSave 25003 /* Save */` 。</span><span class="sxs-lookup"><span data-stu-id="c5a8c-117">The ID is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="c5a8c-118">這個元素包含的值，是由類型 *xs： positiveInteger* 和 *xs： string* 的等位所限制為整數值，介於2和59999（含）之間，或0x2 與0xea5f （十六進位）（含）之間。</span><span class="sxs-lookup"><span data-stu-id="c5a8c-118">This element contains a value from the union of types *xs:positiveInteger* and *xs:string* constrained to an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="c5a8c-119">最大長度為10個字元，包括選擇性前置零。</span><span class="sxs-lookup"><span data-stu-id="c5a8c-119">The maximum length is 10 characters, including optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="c5a8c-120">範例</span><span class="sxs-lookup"><span data-stu-id="c5a8c-120">Examples</span></span>

<span data-ttu-id="c5a8c-121">下列範例示範具有 **Command.Id** 宣告之 [**Command**](windowsribbon-element-command.md)元素的標記。</span><span class="sxs-lookup"><span data-stu-id="c5a8c-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Id** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c5a8c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5a8c-122">Requirements</span></span>



| <span data-ttu-id="c5a8c-123">需求</span><span class="sxs-lookup"><span data-stu-id="c5a8c-123">Requirement</span></span> | <span data-ttu-id="c5a8c-124">值</span><span class="sxs-lookup"><span data-stu-id="c5a8c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c5a8c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5a8c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c5a8c-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5a8c-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c5a8c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5a8c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c5a8c-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5a8c-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





